# finalproject
Creatd by Alicia Zhao, Spring 2020.

## Summary
This is a final project for the course Environmental Data Analytics at Duke University in Spring 2020. 

This project will examine the association between air quality and asthma in California over the period 2013-2016 through a time series and a multiple linear regression. 

## Investigators
Data was assembled and analyzed by *Alicia Zhao* from the Nicholas School of the Environment, Duke University. 
For more information, please contact asz13@duke.edu

## Keywords
Air quality, PM2.5, ozone, nitrogen dioxide, asthma, California, environmental justice, time series, multiple linear regression

## Database Information
### Air quality data
Air quality data were collected using EPA's Download Daily Data tool (https://www.epa.gov/outdoor-air-quality-data/download-daily-data).

The following selections were made: 
* PM2.5, Ozone, and NO2 (Pollurant)
* 2013 - 2016 (Year)
* California (Geographic Area)
* Download CSV (spreadsheet)

csv files were saved as `EPAair_O3_CA_2017_raw.csv`, `EPAair_O3_CA_2016_raw.csv`, `EPAair_O3_CA_2015_raw.csv`, `EPAair_O3_CA_2014_raw.csv`, `EPAair_O3_CA_2013_raw.csv`,
`EPAair_NO2_CA_2017_raw.csv`, `EPAair_NO2_CA_2016_raw.csv`, `EPAair_NO2_CA_2015_raw.csv`,
`EPAair_NO2_CA_2014_raw.csv`, `EPAair_NO2_CA_2013_raw.csv`, `EPAair_PM25_CA_2017_raw.csv`,
`EPAair_PM25_CA_2016_raw.csv`, `EPAair_PM25_CA_2015_raw.csv`, `EPAair_PM25_CA_2014_raw.csv`,
`EPAair_PM25_CA_2013_raw.csv`

Data were accessed 2020-04-11.

### Asthma data
Asthma data were collected using Tracking California's Asthma Data Query tool (https://trackingcalifornia.org/asthma/query).

The following selections were made: 
* Emergency department visits due to asthma (Type of Event)
* Age 0-17, Age 18 & over (Age sub-group)
* 2013 - 2017 (Year)
* Age-adjusted rates per 10,000 (How event is measured)
* All Races/Ethnicities, Black/African-American (Race/ethnicity)
* Both Sexes (Gender/sex)
* Conventional (Type of information)
* Zip Codes (Type of geography)

csv files were saved as `TrackingCA_Asthma_ERVisits_Adults_2013_raw.csv`, `TrackingCA_Asthma_ERVisits_Adults_2014_raw.csv`, `TrackingCA_Asthma_ERVisits_Adults_2015_raw.csv`,
`TrackingCA_Asthma_ERVisits_Adults_2016_raw.csv`,
`TrackingCA_Asthma_ERVisits_Adults_2017_raw.csv`,
`TrackingCA_Asthma_ERVisits_Children_2013_raw.csv`,
`TrackingCA_Asthma_ERVisits_Children_2014_raw.csv`,
`TrackingCA_Asthma_ERVisits_Children_2015_raw.csv`,
`TrackingCA_Asthma_ERVisits_Children_2016_raw.csv`,
`TrackingCA_Asthma_ERVisits_Children_2017_raw.csv`,
`TrackingCA_Asthma_ERVisits_Black_2013_raw.csv`,
`TrackingCA_Asthma_ERVisits_Black_2014_raw.csv`,
`TrackingCA_Asthma_ERVisits_Black_2015_raw.csv`,
`TrackingCA_Asthma_ERVisits_Black_2016_raw.csv`,
`TrackingCA_Asthma_ERVisits_Black_2017_raw.csv`

Data were accessed 2020-04-12.

### Demographics data
Demographic data were collected from County Health Rankings & Roadmaps
(https://www.countyhealthrankings.org/app/california/2019/downloads)
* 2017 California Data was chosen.

The xls file was saved as `CountyHealthRankings_CA_2019_raw.xls`

Since there multiple tabs in the xls file, 
relevant information from the file was taken and converted into a csv file.
The csv file was saved as `CountyHealthRankings_CA_2019_filtered_raw.csv`

Data were accessed 2020-04-12.

## Folder structure, file formats, and naming conventions 
The repository contains 3 folders. 
* The `Code` folder contains all code input files used for the project in the format of Rmds files. There are separate code files for data processing/wrangling, data exploration, and data analysis.
* The `Data` folder contains `Processed` and `Raw` data folders, which contain data in the format of csv files. Within the `Raw` folder are separate folders for `Air quality`, `Asthma`, and `Demographics`.
* The `Output` folder contains key visualizations created as a part of the project in the form of pdfs as well as the final pdf document for the project. 

Files are named according to the following naming convention: `databasename_datatype_details_stage.format`, where: 

**databasename** refers to the database from where the data originated

**datatype** is a description of data 

**details** are additional descriptive details, particularly important for processed data 

**stage**refers to the stage in data management pipelines (e.g., raw, cleaned, or processed)

**format** is a non-proprietary file format (e.g., .csv, .txt)


## Metadata
### Air quality metadata
Information gathered from: https://www.epa.gov/outdoor-air-quality-data/air-data-basic-information and https://aqs.epa.gov/aqsweb/documents/AQS_Format.html

Column names without descriptors are self-explanatory.

* Date: month/day/year
* Source: AQS (Air Quality System) or AirNow
* Site ID: A unique number within the county identifying the site.
* POC: “Parameter Occurrence Code” used to distinguish different instruments that measure the same parameter at the same site.
* Daily Mean PM2.5 Concentration: numeric value
* Daily Max 8-hour Ozone Concentration: numeric value
* Daily Max 1-hour NO2 Concentration: numeric value
* Units: units for concentration

* Daily_AQI_VALUE: Air quality index (range 0-500). Levels: 
0-50: Good (green)
51-100: Moderate (yellow)
101-150: Unhealthy for sensitive groups (orange)
151-200: Unhealthy (red)
201-300: Very unhealthy (purple)
301-500: Hazardous (maroon)

* Site Name
* DAILY_OBS_COUNT: number of observations per day
* PERCENT_COMPLETE
* AQS_PARAMETER_CODE
* AQS_PARAMETER_DESC
* CBSA_CODE
* CBSA_NAME
* STATE_CODE
* STATE
* COUNTY_CODE
* COUNTY
* SITE_LATITUDE
* SITE_LONGITUDE

### Asthma metadata
Information gathered from: https://trackingcalifornia.org/asthma/query

Column names without descriptors are self-explanatory.

* Zip Code
* County
* Incidence: Age-adjusted rate of emergency department (ER) visits due to asthma per 10,000 California residents. 

### Demographics metadata
Column names without descriptors are self-explanatory.

* FIPS
* State
* County
* Median Household Income
* Population
* % African American
* % Rural
* % Smokers
* % Uninsured

## Scripts and code
The `Code` folder contains all code input files used for the project in the format of Rmds.There are separate code files for data processing/wrangling, data exploration, and data analysis. 

The `Data Processing` file is intended for all code related to processing and wrangling the raw datasets. The `Data Exploration` file is intended for code that examine the structure and distributions of the processed datasets. The `Data Analysis` file is intended for code related to visualizations and statistical tests associated with my resaerch questions. 

## Quality assurance/quality control
Data types for each column will be checked to ensure that they are read as the correct type. Additionally, values for each column will be checked so that they are consistent with the data type.

For data that seem questionable, I will identify them by including a flagging_column next to the column of data values. If these data are used in the model, I will include the percent flagged data and percent missing data. 