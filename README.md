# Crime Data from 2020 to Present
![image of crime scene](crimeu.jpg)

### Overview of the dataset
 
This dataset reflects incidents of crime (except for murder where data exist for each victim) in the City of Los Angeles dating back to 2020. This data is transcribed from original crime reports that are typed on paper; therefore, there may be some inaccuracies. Some location fields with missing data are noted as (0°, 0°). Address fields are only provided to the nearest hundred blocks to maintain privacy. This data is as accurate as the data in the database. 
The dataset was downloaded in CSV form from the website [Data.Gov](https://catalog.data.gov/dataset/crime-data-from-2020-to-present). It is quite a large one; if not, I would have uploaded it here, but you can click on the link to visit the webpage to download it. It consists of  28 columns and 986501 rows.

### Challenges

1. One of the challenges faced was understanding what each column represented as they were not written in full.
2. There were a lot of errors in the input of data in some specific rows and columns, hence making it difficult to carry out analyses e.g. the vict Descent column. Vict sex etc

Columns present in the dataset include:
DR_NO, Date Rptd,	DATE OCC,	TIME OCC,	AREA,	AREA NAME,	Rpt Dist No,	Part 1-2,	Crm Cd,	Crm Cd Desc,	Mocodes,	Vict Age,	Vict Sex,	Vict Descent,	Premis Cd,	Premis Desc,	Weapon Used Cd,	Weapon Desc,	Status,	Status Desc,	Crm Cd 1,	Crm Cd 2,	Crm Cd 3,	Crm Cd 4,	LOCATION,	Cross Street,	LAT,	LON.
For clarity, I will give meaning to a few columns but not all as some columns are easy to understand.

* Dr_No represents the input record Number for each crime reported.
* Date rptd mean date reported.
* Date OCC and Time OCC mean the date and time the crime occurred.
* Rpt Dist No mean report distress number.
* Crm cd mean crime code
* vict age, sex and descent mean victims Age, sex and race (Black, white, Asian etc)
* Premis cd mean Premises Code.
* weapon desc represents the type of weapons that was used in carrying out the crime.


## Processing the Dataset

The dataset was downloaded onto my local device from the website DATA.GOV and was imported into PowerBI using the "GET DATA" Function, which loads the dataset into power-Query machine for cleaning and further processing.
As said Earlier, the dataset contains a lot of errors and missing rows which needed to be cleaned and replaced with the correct values.

* Cleaning the dataset
The first step of cleaning the dataset was to remove duplicates using the "Remove Duplicate" Function in the power query. The DR_N0 column was selected in using to remove duplicate values because the column contains unique numbers for each crime that was reported.

* Replaced Missing Values and incorrect Values
  Some columns in the dataset such as Vict age, vict sex, weapon used, etc contain inconsistent values and missing errors.
  The Vict Age Column contains inconsistent values which were replaced by finding the average mean of all ages.
  The vict sex Column contains inconsistent values which were replaced with "unspecified"
  The weapon used and weapon used code column contains null and blank values, the null values were replaced with "Zeros" while the blank was replaced with "None".

*Conversion of data type
 Some columns
  
  



