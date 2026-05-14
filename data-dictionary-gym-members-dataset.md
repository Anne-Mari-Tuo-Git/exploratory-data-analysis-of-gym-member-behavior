| Variable | Type | Description | Example | Notes |
| --- | --- | --- | --- | --- |
| **[id](ca://s?q=explain_id_variable)** | Integer | Unique identifier for each member. | ``1`` | Primary key. |
| **[gender](ca://s?q=explain_gender_variable)** | Categorical (string) | Member’s gender. | ``Female`` | Values: Male / Female. |
| **[birthday](ca://s?q=explain_birthday_variable)** | Date | Member’s date of birth. | ``1997-04-18`` | ISO format ``YYYY-MM-DD``. |
| **[Age](ca://s?q=explain_age_variable)** | Integer | Member’s age. | ``27`` | Derived from *birthday*. |
| **[abonoment_type](ca://s?q=explain_abonoment_type)** | Categorical (string) | Type of membership subscription. | ``Premium`` | Values: Premium / Standard. |
| **[visit_per_week](ca://s?q=explain_visit_per_week)** | Integer | Number of weekly gym visits. | ``4`` | Useful for segmentation. |
| **[days_per_week](ca://s?q=explain_days_per_week)** | List (string) | Days of the week the member attends. | ``"Mon, ``Sat, ``Tue, ``Wed"`` | Comma‑separated list. |
| **[attend_group_lesson](ca://s?q=explain_attend_group_lesson)** | Boolean | Indicates if the member attends group lessons. | ``True`` | True / False. |
| **[fav_group_lesson](ca://s?q=explain_fav_group_lesson)** | List (string) | Favorite group lessons. | ``"Kickboxen, ``BodyPump, ``Zumba"`` | Empty if not attending group lessons. |
| **[avg_time_check_in](ca://s?q=explain_avg_time_check_in)** | Time | Average check‑in time. | ``19:31:00`` | Format ``HH:MM:SS``. |
| **[avg_time_check_out](ca://s?q=explain_avg_time_check_out)** | Time | Average check‑out time. | ``21:27:00`` | Format ``HH:MM:SS``. |
| **[avg_time_in_gym](ca://s?q=explain_avg_time_in_gym)** | Integer (minutes) | Average time spent in the gym. | ``116`` | In minutes. |
| **[drink_abo](ca://s?q=explain_drink_abo)** | Boolean | Indicates if the member has a drink subscription. | ``False`` | True / False. |
| **[fav_drink](ca://s?q=explain_fav_drink)** | List (string) | Favorite drinks. | ``"berry_boost, ``lemon"`` | Empty if *drink_abo* is False. |
| **[personal_training](ca://s?q=explain_personal_training)** | Boolean | Indicates if the member uses personal training services. | ``True`` | True / False. |
| **[name_personal_trainer](ca://s?q=explain_name_personal_trainer)** | Categorical (string) | Assigned personal trainer. | ``Mike`` | Empty if no personal training. |
| **[uses_sauna](ca://s?q=explain_uses_sauna)** | Boolean | Indicates if the member uses the sauna. | ``True`` | True / False. |