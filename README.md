# AIR-POLLUTION-on-Frankfurter-Allee
**benned nedben**  
**IronHack, Berlin 23 Mar 2023**

## Overview

* Analysis of different types of air pollution based on data from measuring station number 174 on Frankfurter Allee in Berlin Friedrichshain since the start of measurements.

Programs used:

	* Python
	* Excel
	* LibreOffice
	* Jupyter Notebook
	* Tableau
    * MYSQL Workbench
	* Power Point
    * Adobe Photoshop

Frameworks used

    * pandas
    * numpy
    * matplotlib
    * seaborn
    * datetime
    * calendar
    * pymysql
    * sqlalchemy
    * getpass
  
## Data Preparation

### Overview: 
Various data sets are available for download on the berlin.de website.

The following website could be used to download datasets about all measuring stations in Berlin

	* [Luftgütemessdaten](https://daten.berlin.de/datensaetze/luftgütemessdaten)


On the website it says:

For Berlin, current and historical measurement data from the Berlin air quality measurement network are available, especially for air pollutants relevant to limit values in accordance with the 39th BImSchV. Available data includes measurements of gaseous air pollutants (nitrogen oxides, ozone, carbon monoxide, benzene, toluene and sulfur dioxide) and particulate air pollutants (particulate matter PM10, particulate matter PM2.5). Furthermore, overviews of the current air quality index, the daily measured values and the annual number of limit value violations are available. [...] The data can be downloaded directly in CSV format from the luftdaten.berlin.de website. Depending on the air pollutant, four to eight variants of aggregated data are available. For the automatically measured components, these are at least hourly values, daily values, monthly values and annual values. All information subject to change. The measured values are still subject to quality control and can - if necessary - be corrected.

## Used records

- particulate matter (PM10) (4 datasets)
- particulate matter (PM2,5) (4 datasets)
- nitrogen dioxide (NO₂) (4 datasets)
- nitrogen monoxide (NO) (4 datasets)
- sum of nitrogen oxides (NOₓ) (4 datasets)
- ozone (O₃) (4 datasets)
- carbon monoxide (CO) (4 datasets)
- sulfur dioxide (SO₂) (2 datasets)


### aggregated data

- hourly values
- daily values
- monthly values
- annual values

### Restrictions

- In most cases, one dataset each was downloaded for hourly, daily, monthly and yearly measurement intervals.
- Recording started January 1994
- A total number of 30 records were downloaded and then used for analysis.
- hourly records only go back one year
- daily annual rates only go back 10 years
- monthly and yearly records go back to the beginning of the recording
- Hourly and daily data sets were missing for sulfur dioxide


## Data Wrangling and Cleaning

- View the data in LibreOffice
- Delete the data of other measuring stations
- Translation of column names
- read the formatted records into Jupyter Notebook
- NaN values were deliberately not deleted because they were part of the analysis
- Formatting the time column into a usable format
- Generation of columns for year, month, day of the week and hour of the day


## Methods for data analysis in Jupiter Notebook (Python) 

- Visual analysis by displaying the corresponding dataset as a line chart
- subsequent determination of threshold values
- Value counts the records above a threshold within a specified time period and then plots them as a bar chart
- Repeating this process for different time periods (year, month, day of the week and hour of the day)

### Data Storage

* Storage of corresponding data in csv format (the data is not contained in the repository)
* Storage of corresponding data in sql format (the data is not contained in the repository)
* Aggregate hourly data for all gases and particles for analysis in Tableau in one dataset (ber_all_20220318-20230318 stundenwerte_new columns2.csv) using LibreOffice (the data is not contained in the repository)

## Methods for data analysis in Tableau

Using Tableau and dataset (ber_all_20220318-20230318 stundenwerte_new columns2.csv) to create interactive sheets. (the Tableau file is contained in the repository)

## Power Point

A summary of the measurement results can be found in the Power Point presentation. For clarity, it also contains slides that were not part of the original presentation due to time constraints.

# Conclusion

	* The following statements have not been scientifically tested and represent the opinion of the author, which is based solely on the measurement data given for the location on Frankfurter Allee. Considering other locations and additional data may lead to different conclusions.

	* It was found that (with the exception of ozone) the measured values in winter are significantly higher than in summer due to the central and decentralized heating of the buildings.
	* The data also showed that readings are lower on weekends than on other days due to less traffic.
	* With one exception, there has been a positive trend in the decrease in measured values over the past few years.
	* Political and individual measures to reduce CO2 and air pollution are obviously successful.
	* The levels of ozone in the air are stagnating or rising slightly, which is related to global warming.

To further reduce air pollution, it is recommended to reduce traffic and modernize the heating systems, which are largely based on fossil fuels and thus have a significant impact on the readings.