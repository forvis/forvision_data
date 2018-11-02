# data for forvision package

## 1. TSTS -  Time series table schema 
| File name (column name)| Description | Examples|
|-----|-----|-----|
|series_id| Time series identifier -a unique name that identifies a time series| "Y1"|
|timestamp| Any representation of the period to which the observation relates. | "“01.01.1997” in case of daily data "|
|value| The value observed| 1000|

#### Example:
![1](https://user-images.githubusercontent.com/44469540/47648065-e55ed500-db89-11e8-921b-4df7060ed7a6.PNG)

## 2. FDTS - Forecast dynamic table schema
#### Example:
![2](https://user-images.githubusercontent.com/44469540/47647953-a2046680-db89-11e8-9ae3-fefc56cb5372.PNG)

## 3. FTS - Forecast table schema

#### Example:
![3](https://user-images.githubusercontent.com/44469540/47648076-ee4fa680-db89-11e8-93c4-39c5382315fa.PNG)


# M3Data
The 3003 time series from the IJF-M3 competition (Makridakis and Hibon, 2000) and M3 Data with Rolling-Origin and Interval Forecasts saved as csv files

The 3003 time series of the M3-Competition are distributed as follows:
![m3data](https://user-images.githubusercontent.com/31816408/36041667-54a869fe-0dda-11e8-839a-1310ba94e60c.JPG)

The 3003 time series of M3-Competition (the historical data + the future data) are saved as follows:

![m3series](https://user-images.githubusercontent.com/31816408/36041980-64f984cc-0ddb-11e8-86d1-21e00b10dccf.JPG)

The 3003 time series (only the future data - test data - actual) with forecasts from difference methods of M3-Competition 
are saved as follows:




![m3forecast](https://user-images.githubusercontent.com/31816408/36041987-69d74cfe-0ddb-11e8-8c70-45254db00406.JPG)

Forecasts of 3003 time series of M3-Competition using ARIMA model with Rolling-Origin and Interval Forecasts 
are saved as follows:




![m3ci](https://user-images.githubusercontent.com/31816408/36041990-6db75170-0ddb-11e8-9660-484902fb7a5e.JPG)


Time series + Forecasts of 3003 time series of M3-Competition using ARIMA model with Rolling-Origin and Interval Forecasts 
are saved as follows:
![capture](https://user-images.githubusercontent.com/31816408/36153240-a848ce26-10de-11e8-9967-a1683f0b489a.JPG)
