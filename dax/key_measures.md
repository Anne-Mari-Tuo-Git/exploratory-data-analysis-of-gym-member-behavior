### :hourglass_flowing_sand: Average Time Spent per Session (H:M)

Calculates the average time members spend in the gym per session and returns the result in a readable hours‑and‑minutes format (H:M)

```DAX

Average Time Spent per Session = 
VAR AvgMinutes =
    AVERAGE(gym_membership[avg_time_in_gym])
VAR Hours =
    INT(AvgMinutes / 60)
VAR Minutes =
    ROUND(MOD(AvgMinutes, 60), 0)
RETURN
    Hours & "h " & Minutes & "m"

```


### :date: Peak Attendance Day

Determines the weekday with the highest attendance by summarizing visit counts per day, ranking them using TOPN, and returning the day with the maximum number of recorded visits.

```DAX

Peak Attendance Day = 
VAR DayCounts =
    SUMMARIZE(
        gym_membership,
        gym_membership[days_per_week_expanded],
        "CountVisits", COUNT(gym_membership[id])
    )
VAR TopDay =
    TOPN(
        1,
        DayCounts,
        [CountVisits],
        DESC
    )
RETURN
    MAXX(TopDay, gym_membership[days_per_week_expanded])


```

### :watch: Peak Attendance Hour

Determines the hour with the highest gym attendance by summarizing visit counts per hour, ranking them with TOPN, and returning the hour with the maximum number of recorded check‑ins.

```DAX

Peak Attendance Hour = 
VAR HourCounts =
    SUMMARIZE(
        gym_membership,
        gym_membership[check_in_hour],
        "CountVisits", COUNT(gym_membership[id])
    )
VAR TopHour =
    TOPN(
        1,
        HourCounts,
        [CountVisits],
        DESC
    )
RETURN
    MAXX(TopHour, gym_membership[check_in_hour])

```

### :dart: Most Common Age Group

Identifies the age group with the highest member frequency by grouping records, counting occurrences per age bin, ranking them with TOPN, and returning the category with the maximum count.

The measure operates on a pre‑defined Age Bin column that groups members into categorical age ranges.

```DAX

Most Common Age Group = 
VAR AgeGroupCounts =
    ADDCOLUMNS(
        SUMMARIZE(
            gym_membership,
            gym_membership[Age Bin]
        ),
        "CountGroup", CALCULATE(COUNTROWS(gym_membership))
    )
VAR TopGroup =
    TOPN(1, AgeGroupCounts, [CountGroup], DESC)
RETURN
    MAXX(TopGroup, [Age Bin])

```


### Gender Ratio (%)

```DAX


### Personal Training Usage (%)

```DAX

### Most Popular Group Lesson
```DAX


Trainer Popularity (Top Trainer)

Average Visits per Week

Membership Duration (Avg)

