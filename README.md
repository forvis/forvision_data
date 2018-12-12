# data for forvision package

## 1. TSTS -  Time series table schema 
In time series table schema each observation is stored in a table as a separate record (line):

| Field name (column name)| Description| Examples |
| --- | --- | ---- |
|series_id*| Time series identifier - a unique name that identifies a time series  | “Y1” |
|timestamp*|Any representation of the period to which the observation relates. We recommend the use of [the ISO 8601 standard](https://en.wikipedia.org/wiki/ISO_8601)|"1997" in case of yearly data, "1997-01-20" in case of daily data, "1997-11" in case of monthly data, "1997-W03" in case of weekly data, "2018-Q2" in case of quarterly data|
|value|The value observed |1000|

*the key (the unique value that should not duplicated) for this table schema is series_id, timestamp. In other words, we cannot have two (or more) records in a table relating to the same time series and the same period of observation (timestamp)

#### Example:
![1](https://user-images.githubusercontent.com/44469540/47648065-e55ed500-db89-11e8-921b-4df7060ed7a6.PNG)

