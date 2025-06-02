| **Variable Name**        | **Type**      | **Description**                                                                 | **Example**                       |
|--------------------------|---------------|---------------------------------------------------------------------------------|-----------------------------------|
| `sensor_name`            | `string`      | Name or identifier of the sensor that recorded the measurement.                 | `parautarin02`                    |
| `measure_date`           | `datetime64`  | Date and time when the measurement was recorded.                                | `2020-04-30 11:38:04+00:00`       |
| `id`                     | `string`      | Unique identifier measurement entry.                                            | `5eafbba6bc37446f22a8adfa`        |
| `geo_type`               | `string`      | Type of geographical location ("Point", "LineString").                          | `Point`                           |
| `geo_coords`             | `list`        | Geographical coordinates (longitude, latitude) of the sensor location.          | `[-1.578112267, 48.115225974]`    |
| `start_date`             | `datetime64`  | Start date and time of the measurement.                                         | `2020-04-30 11:38:04+00:00`       |
| `sensor_type`            | `string`      | Type of the sensor used to measure the air quality.                             | `mobileGps`                       |
| `p`                      | `float64`     |Time precision of the measurement, in seconds                                    | `76.583`                          |
| `PM_2.5`                 | `float64`     | Fine particulate matter concentration (PM₂.₅) in µg/m³.                         | `2.32`                            |
| `bn`                     | `string`      | Base Name of the sensor                                                         | `OPC_N3:12`                       |
| `longitude`              | `float64`     | Longitude of the measurement location.                                          | `-1.578112`                       |
| `latitude`               | `float64`     | Latitude of the measurement location.                                           | `48.115226`                       |
| `day_week`               | `string`      | Day of the week when the measurement was taken ( Monday, Tuesday, etc.).        | `Monday`                          |
| `day`                    | `int64`       | Day of the month when the measurement was taken.                                | `30`                              |
| `hour`                   | `int64`       | Hour of the day when the measurement was taken (24-hour format).                | `11`                              |
| `month`                  | `int64`       | Month of the year when the measurement was taken (1 to 12).                     | `4`                               |
| `year`                   | `int64`       | Year when the measurement was taken.                                            | `2020`                            |
| `hour_minute_second`     | `string`      | Time in HH:MM:SS format when the measurement was taken.                         | `11:38:04`                        |

