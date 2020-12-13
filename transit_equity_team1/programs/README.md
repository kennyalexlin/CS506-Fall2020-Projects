### Output description

1. `./output/stops.csv`

| Column Name    | Description                                                  |
| -------------- | ------------------------------------------------------------ |
| STOP_ID        | ID for this stop                                             |
| STOP_NAME      | Name for this stop                                           |
| TOWN           | Name of the town this stop is located in                     |
| TRACT_ID       | ID for the tract this stop is located in                     |
| income         | Median income for this tract                                 |
| income_level   | income level for this tract, from 0-4, and -1 means missing value |
| route_ids      | IDs for the routes that go through this stop                 |
| ridership      | Average ridership for this stop for routes, in the order of `route_ids` |
| revenues       | Annual revenues for this stop for routes, in the order of `route_ids` |
| revenue_annual | Total annual revenue for this stop (sum of values in `revenues`) |

2. `./output/stops_weighed.csv` (`./output/stops.shp` is the shapefile version of it)

| Column Name        | Description                                                  |
| ------------------ | ------------------------------------------------------------ |
| STOP_ID            | ID for this stop                                             |
| geometry           | geometry Point of this stop                                  |
| impacted_geoid     | GeoID for tracts that intercept the circle                   |
| proportion_2tract  | proportion of intercepted area over tract area               |
| proportion_2circle | proportion of intercepted area over circle area              |
| income             | weighed income based on proportion                           |
| income_level       | income level for this tract, from 0-4, and -1 means missing value |
| impacted_pop       | weighted population impacted based on proportion             |

