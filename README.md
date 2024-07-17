# UNEMPLOYMENT CAUSES
## PROJECT OVER VIEW
This data analysis project aims to provide insight into the causes of unemployment in various countries . By analysing this data we seek to identify trends, correlations, make data-driven decisions and recommendations and gain a deeper understanding of the country(s) that is greatly affected by unemployment due to some factors like migration, population rate, education levels, poverty ratios among others. This is to help us to be able to make clear decions and set possible data driven decisions on how we can improve on the unemployment rate.
## Data Source
Subscription data: The primary dataset used for this analysis is the "unemployment_data.cvs" file, containing deatailed factors about country's unemployment factors.
## Tools Used
-Excel - Data cleaning, Data analysis [Downlaod_here](https://microsoft.com)

-SQL - Further data cleaning, Data analysis, Removing Nulls  [Downlaod_here](https://sql/ssms.com)

-PowerBi - Data visualization and reports  [Downlaod_here](https://sql/ssms.com)

## Data Cleaning/ Preparation
In the initial data preparation phase, the following tasks were prformed:
1. The data was loaded and inspected.
2. Data Cleaning and formatting was paritially done.
3. Handling missing values.
4.  Further cleaning and analysis.

## Exploratory Data Analysis
EDA Involved the training data to answer key questions, such as:
- What is the poverty ratio?
- What is sum of migration?
- What is the different school enrollment by country?
- What is te count of GDP by country on scale of 10?
- What is population by year?

  ## Data analysis
```Excel
 =IFS(D3:D66<=15,10,D3:D66<=20,15,D3:D66<=25,20,D3:D66<=25,20,D3:D66<=30,25,D3:D66<=35,30) 
=IFS(F6:F69<=15,10,F6:F69<=20,15,F6:F69<=25,20,F6:F69<=25,20,F6:F69<=30,25,F6:F69<=35,30,,F6:F69<=40,35,,F6:F69<=45,40,F6:F69<=50,50)
=IFS(Q6:Q71<75,70,Q6:Q71<80,75,Q6:Q71<85,80,Q6:Q71<90,85,Q6:Q71<95,90,Q6:Q71<100,95,Q6:Q71<105,100,Q6:Q71<110,105,Q6:Q71<115,110,Q6:Q71<120,115,Q6:Q71<125,120)
=IFS(M7:M72<0,0,M7:M72<20,10,M7:M72<30,20,M7:M72<40,30,M7:M72<40,30,M7:M72<50,40,M7:M72<60,50,M7:M72<70,60,M7:M72<80,70,M7:M72<90,80,M7:M72<100,90,M7:M72<110,100,M7:M72<121,110,M7:M72<135,120)
For grouping

SQL
SELECT Country, Year,PGDP,SE_SEC_ENRR,Net_migration,Population_total,PPrimarycompletionrate,SE_ENR_PRSC_FM_ZS,SI_POV_NAHC,SE_SEC_ENRR,CAST(SI_POV_NAHC AS INT) ASSI_POV_NAHC_No_Decimals
    FROM Work
	Where SE_SEC_ENRR IS NOT NULL AND SI_POV_NAHC IS NOT NULL

	UPDATE Work SET SE_ENR_PRSC_FM_ZS = 0 WHERE SE_ENR_PRSC_FM_ZS IS NULL;

	DELETE FROM Work WHERE Country IS NULL;

PowerBi
Changing from decimals to whole Numbers and Report Making.

```
##REPORTS AND VISUALIZATION

![UNE](https://github.com/user-attachments/assets/7ec4a12b-b362-41f3-9626-51b205846b04)


![UNEEEE](https://github.com/user-attachments/assets/0c3b6209-2d96-4503-bf05-025b0c02ab71)

###RESULTS AND FINDING
The analysis results are sumarised as follows:

1. France has the highest number of active memebers to the training  with a total number of 47627 active members while Geramany has the least number of active subscribers to the training.
2. The youth are more of the training active members in france.
3. Male youth are more of the active members in the training.

