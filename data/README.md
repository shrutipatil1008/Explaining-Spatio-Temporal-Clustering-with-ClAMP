# Data

The raw dataset used in this project is the **Hofer LandBus** mobility dataset  
(Landkreis Hof, Germany) and is **confidential** — it cannot be shared publicly.

## Dataset Summary

| Property | Value |
|---|---|
| Records | ~63,000 trips |
| Features | Start/end locations, timestamps, trip duration |
| Spatial reference | EPSG:3035 (ETRS-LAEA Europe) |
| Source | Hofer LandBus regional transport operator |

## Expected Schema

To reproduce this project with your own data, provide a CSV or DataFrame  
with the following columns:

| Column | Type | Description |
|---|---|---|
| `departure_time` | datetime | Timestamp of trip departure |
| `arrival_time` | datetime | Timestamp of trip arrival |
| `departure_lat` | float | Departure latitude (WGS84) |
| `departure_lon` | float | Departure longitude (WGS84) |
| `destination_lat` | float | Arrival latitude (WGS84) |
| `destination_lon` | float | Arrival longitude (WGS84) |

## Contact

For data access enquiries, contact:  
**Shruti Patil** — shrutipatil10898@gmail.com  
or reach out via the research group at **Hochschule Hof, University of Applied Sciences**.
