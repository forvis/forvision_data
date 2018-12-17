# Data for forvision package

## 1. TSTS -  Time series table schema 
In time series table schema each observation is stored in a table as a separate record (line):

| Field name (column name)| Description| Examples |
| --- | --- | ---- |
|series_id*| Time series identifier - a unique name that identifies a time series  | “Y1” |
|timestamp*|Any representation of the period to which the observation relates. We recommend the use of [the ISO 8601 standard](https://en.wikipedia.org/wiki/ISO_8601)|"1997" in case of yearly data, "1997-01-20" in case of daily data, "1997-11" in case of monthly data, "1997-W03" in case of weekly data, "2018-Q2" in case of quarterly data|
|value|The value observed |1000|

*the key (the unique value that should not duplicated) for this table schema is series_id, timestamp. In other words, we cannot have two (or more) records in a table relating to the same time series and the same period of observation (timestamp)

#### Example:
```
  series_id   value   timestamp
1         Y1 3103.96      1984
2         Y1 3360.27      1985
3         Y1 3807.63      1986
4         Y1 4387.88      1987
5         Y1 4936.99      1988
6         Y1 5379.75      1989
7         Y1 6158.68      1990
8         Y1 6876.58      1991
9         Y2 5389.80      1984
10        Y2 5384.40      1985
```

## 2. FTS - Forecast table schema
Forecast Table Schema is needed to store forecasting results.

Each table line corresponds to all the forecasting results obtained for a given time series series using a given method for a given horizon for a given origin:


| Field name (column name)| Description| Examples |
| --- | ---| ---- |
|series_id* | Time series ID for which the forecast was calculated| "Y1" |
|timestamp*|Any representation of the period to which the observation relates. We recommend the use of the [ISO 8601 standard](https://en.wikipedia.org/wiki/ISO_8601)|"1997" in case of yearly data, "1997-01-20" in case of daily data, "1997-11" in case of monthly data, "1997-W03" in case of weekly data, "2018-Q2" in case of quarterly data|
|origin_timestamp*|Origin of the forecast (provided in a timestamp format)|"1996-12-29"|
|horizon*| Forecast horizon| 3 |
|method*| Method identifier - a unique name that identifies a method by which the forecasting result was calculated| "ARIMA"|
|forecast| Point forecast| 234|
|lo95| The lower limit for the 95% prediction interval|178|
|hi95| The upper limit for the 95% prediction interval|273|

*the key (the unique value that should not duplicated) for this table schema is series_id, method, timestamp, origin_timestamp, horizon. 

#### Example:

```
   series_id   method  timestamp       origin_timestamp  forecast  horizon   lo90     hi90
1         Y1      A       1989              1988          5406.43      1    5183.349 5629.511
2         Y1      A       1990              1988          5875.96      2    5652.879 6099.041
3         Y1      A       1991              1988          6345.48      3    6122.399 6568.561
4         Y1      B       1989              1988          5473.87      1    5250.789 5696.951
5         Y1      B       1990              1988          6010.43      2    5787.349 6233.511
6         Y1      B       1991              1988          6546.63      3    6323.549 6769.711
7         Y1      C       1989              1988          5406.43      1    5183.349 5629.511
8         Y1      C       1990              1988          5875.96      2    5652.879 6099.041
9         Y1      C       1991              1988          6345.48      3    6122.399 6568.561
10        Y2      A       1989              1988          4142.60      1    3919.519 4365.681
```

## 3. M3-Competition data

## 4. M3 prediction intervals


