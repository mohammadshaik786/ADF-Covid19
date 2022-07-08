# ADF-Covid19
A project on covid19 Prediction/Reporting for Azure Data Engineer


---------------------------------------------------------------------

Project Overview: 

Prediction: Data Platform in which Data Scientists can run ML models to predict the spread of virus and find insights from the data. 

Data Lake to be built with the following data to aid Data Scientists to predict the spread of 	the virus/ mortality 						 

*Confirmed cases 

*Mortality 

*Hospitalization/ ICU Cases  

*Testing Numbers 						 

*Country’s population by age group  

	 

Reporting: Data Platform in which Data Analysts can easily generate reports on Covid19 trends by using reporting tool. 

Data Warehouse to be built with the following data to aid Reporting on Trends	 

*Confirmed cases 

*Mortality 

*Hospitalization/ ICU Cases  

*Testing Numbers  


Data Sources: 

ECDC (European Center for Disease Control & Prevention) Data contains Confirmed Cases, Mortality, Hospitalization/ICU cases, Testing numbers 

Eurostat Data for Population Data 

 

Population Data: This contains info about population of each country and % of population as per age group. 

Cases & Death Data : The data contains indicator col which contains confirmed cases & deaths.This should be pivoted for 2 col. Also it conains 3 digit Country code, but required 2 digit country code and it is retrieved by creating lookup table. 

Hospital & Admissions Data: The data contains indicator col having both daily and weekly cases. Hence it is split into daily and weekly, then for both daily and weekly data, it contains hospital occupancy and icu occupancy count for each splitted data in 1 col, it is pivoted to 2 cols. For weekly data, genereated start& end date by using lookup table etc.. 

Testing Data : This contains data about how many tests done,positive rate and new cases raised on the week basis. So tranformed into start date ad end date, 3 digit country code by using lookup tables. 

Population data: In Databricks activity, only 2019 data is reatined, split the 1st col and genrated 2digit country code by using lookup table and finally pivot the splitted data of age_grp into cols. 
