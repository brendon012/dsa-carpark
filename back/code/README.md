This directory contains code for data cleaning, data visualisation and data transformation. The following table summarises the function of scripts:


| script                           | function                                                                                                                            | input                           | output                                                         |
| :------------------------------- | :---------------------------------------------------------------------------------------------------------------------------------- | ------------------------------- | :------------------------------------------------------------- |
| data_cleaning.py                 | clean raw data for subsequent process                                                                                               | raw datas stored in data folder | `cleaned_data.csv`<br> `cleaned_data_short_duration.csv`       |
| data_transformation.py           | transform data to focus on max occupancy                                                                                            | cleaned_data.csv                | `occupancy_minute_final.csv`<br> `max_occupancy_day_final.csv` |
| bootstrap_data_transformation.py | transform data for prediction of car park occupancy using bootstrap                                                                 | max_occupancy_hour_final.csv    | bootstrap_occupancy_data.csv                                   |
| find_arrival_prediction.py       | find arrival distribution w.r.t.:<br> 1. lot type:{red, white}<br> 2. carparks<br> 3. semester, semester break<br> 4. days of week  | cleaned_data.csv                | gmm_arrival_info.csv                                           |
| find_duration_prediction.py      | find duration distribution w.r.t.:<br> 1. lot type:{red, white}<br> 2. carparks<br> 3. semester, semester break<br> 4. days of week | cleaned_data.csv                | gmm_info.csv                                                   |
| occupancy_visualisation.py       | visualise occupation trend of lots for all carparks                                                                                | max_occupancy_day_final.csv     | `red_occupancy_plot.png`<br> `white_occupancy_plot.png`        |