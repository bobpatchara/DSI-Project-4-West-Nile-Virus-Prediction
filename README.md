# ![](https://ga-dash.s3.amazonaws.com/production/assets/logo-9f88ae6c9c3871690e33280fcf557f33.png) West Nile Virus Prediction

### Predict West Nile virus in mosquitoes across the city of Chicago
---

### Problem Statement

West Nile virus (WNV) is mosquito-borne disease. It is most commonly spread to people by the bite of an infected mosquito. As data scientists hired by CDC, We want to understand the factors driving the spread of WNV and suggest a cost-efficient method to handle with it.

---
### Executive Summary and Conclusion

| Model | Best Score | AOC/RUC |
| --- | --- | --- |
|Logistic Regression| 88.86% | 88.89% |
|Decision Tree Classifier| 90.34% | 90.08% |
|Random Forest Classifier| 90.83% | 90.63% |
|XGBoost Classifier| 96.65% | 97.20% |

Out of all model, XGboost is the best performing model with a score at 96.65%  and ROC/AUC at 97.2% 

<img width="327" alt="confusion_matrix" src="https://user-images.githubusercontent.com/76549565/113515336-13884080-959e-11eb-89ad-da95e1f752cb.png">

Since we are concern about the prevention of the West Nile virus, it is acceptable that we lean heavily towards predicting that the Virus is presence even in places where there are no viruses. This is because those places have some possibilities of the virus being presence.

<img width="803" alt="virus_indicators" src="https://user-images.githubusercontent.com/76549565/113515338-15ea9a80-959e-11eb-8627-bb444d414ea4.png">

In conclusion, the main factors driving the spread of the West Nile virus (WNV) are the species of the mosquitos, the number of mosquitos, weather conditions, and the amount of daylight with in a certain period of time. Through our findings, we can conclude that the West Nile Virus is highly seasonal, becoming most prominent in July and August. This is due to the increase in the heat and mosquitos count. 

Because our goal is to prevent the spread of the virus, it is recommended to spay in places that have any indications of the virus. As from our model, some places can have the possibility of the virus being presence when there isn’t at the time. From a cost standpoint, spraying in these places will be beneficial in the long run due to how the virus can impact a patient.

---
### Data Dictionary

|Feature|Type|Dataset|Description|
|---|---|---|---|
|Id            |int      |train.csv/test.csv |ID number of the record
|Date           |datetime      |train.csv/test.csv |date the WNV test is performed
|Address      |datetime |train.csv/test.csv| approximate trap address; sent to GeoCoder
|Species         |str      |train.csv/test.csv| mosquito species in trap
|Block         |str      |train.csv/test.csv| block number of address
|Street        |str      |train.csv/test.csv| street of address
|Trap          |str    |train.csv/test.csv| ID number of the trap
|AddressNumberAndStreet|str|train.csv/test.csv| approximate address retrieved from GeoCoder
|Latitude            |float|train.csv/test.csv| latitude retrieved from GeoCoder
|Longitude            |float|train.csv/test.csv| longitude retrieved from GeoCoder
|AddressAccuracy      |int|train.csv/test.csv| accuracy of information returned from GeoCoder
|NumMosquitos        |int      |train.csv/test.csv| number of mosquitoes in a sample
|WnvPresent           |int      |train.csv/test.csv| whether or not WNV is present in a sample (1 = present; 0 = absent)
|Date |datetime |spray.csv| date of spray
|Time         |datetime      |spray.csv| time of spray
|Latitude|float|spray.csv| latitude of spray
|Longitude        |float|spray.csv| longitude of spray
|Station  |int|weather.csv| weather station (1 or 2)
|Date     |datetime|weather.csv| date of measurement
|Tmax     |int|weather.csv| maximum daily temperature (F)
|Tmin     |int|weather.csv| minimum daily temperature (F)
|Tavg  |int|weather.csv| average daily temperature (F)
|Depart     |int|weather.csv| departure from normal temperature (F)
|Dewpoint    |int|weather.csv| average dewpoint (F)
|WetBulb  |int|weather.csv| average wet bulb
|Heat     |int|weather.csv| heating degree days
|Cool  |int|weather.csv| cooling degree days
|Sunrise     |int|weather.csv| time of sunrise (calculated)
|Sunset     |int|weather.csv| time of sunset (calculated)
|CodeSum     |str|weather.csv| code of weather phenomena 
|Depth     |int|weather.csv| unknown
|Water1  |int|weather.csv| unknown
|SnowFall     |int|weather.csv| snowfall (inch)
|PrecipTotal     |str|intweather.csv| total daily rainfall (inch)
|StnPressure     |int|weather.csv| average atmospheric pressure (inch Hg)
|SeaLevel     |int|weather.csv| average sea level pressure (inch Hg)
|ResultSpeed  |float|weather.csv| resultant wind speed (mph)
|ResultDir     |int|weather.csv| resultant wind direction (degrees)
|AvgSpeed     |int|weather.csv| average wind speed (mph)

The dataset, along with full description, can be found here: [https://www.kaggle.com/c/predict-west-nile-virus/](https://www.kaggle.com/c/predict-west-nile-virus/).

---




