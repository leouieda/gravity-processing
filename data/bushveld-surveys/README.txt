# Bushveld Complex Gravity Surveys

This archive contains gravity readings for a ground-based survey 
of the Bushveld Complex in South Africa. The survey was conducted
over 15 days using the same gravimeter (L&R Model G).

## Survey information

Gravimeter: All surveys were carried out with the same gravimeter. 
The file gravimeter-scaling.csv contains the scaling table for this
particular instrument.

Coordinates: Longitude and latitude are referenced to the WGS84 
ellipsoid. Easting and northing are UTM Zone 34H projected 
coordinates in meters. Elevation is geometric height above the 
WGS84 ellipsoid in meters.

Base stations: Each individual survey was tied to the closest base
station available. All surveys begin and end at the base station. 
The time elapsed since the first reading at the base station is 
recorded in minutes. The absolute gravity values at each base 
station are provided in the bushveld-gravity-base-stations.csv file.

## Contents

bushveld-surveys/
├── data
│   ├── bushveld-gravity-day-1.csv
│   ├── bushveld-gravity-day-2.csv
│   ├── bushveld-gravity-day-3.csv
│   ├── bushveld-gravity-day-4.csv
│   ├── bushveld-gravity-day-5.csv
│   ├── bushveld-gravity-day-6.csv
│   ├── bushveld-gravity-day-7.csv
│   ├── bushveld-gravity-day-8.csv
│   ├── bushveld-gravity-day-9.csv
│   ├── bushveld-gravity-day-10.csv
│   ├── bushveld-gravity-day-11.csv
│   ├── bushveld-gravity-day-12.csv
│   ├── bushveld-gravity-day-13.csv
│   ├── bushveld-gravity-day-14.csv
│   └── bushveld-gravity-day-15.csv
├── bushveld-gravity-base-stations.csv
├── gravimeter-scaling.csv
└── README.txt

## License

This dataset is made available under the Creative Commons
Attribution International 4.0 License.