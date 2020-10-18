# US-Wildfire-Analysis

## Introduction
**Wildfires** are a common problem for America. Every year wildfire is one of the most destructive disasters across the US. These wildfires result in fire-cloud-forming, megafires, burning about 4-5 million acres of land, mobilizing tens of thousands of firefighters, razing thousands of buildings, and sometimes killing people.

This project aims at providing insights on wildfires like causes of fire, geographical locations most prone for wildfire. These details could be used to define recommendations to increase public safety and minimize economic damage from future wildfires.

## Targeted Problems:
* Did the number of wildfires per year increase over a period of time? 
* Average destruction caused per year, and has it increased over the years?
* Analyse the wildfire occurrences based on fire size class.
* Find out the number of fires for each class per year.
* What states are more and less susceptible for wildfire?
* Analyse the different causes of wildfires.


## Data Dictionary
This data is collected from [https://www.kaggle.com/rtatman/188-million-us-wildfires?]. This data publication contains a spatial database of wildfires that occurred in the United States from 1992 to 2015.
Below is the data dictionary for Fires table.
| **Field** | **Description** |
| :--- | :--- |
| FOD_ID | Global unique identifier |
| FPA_ID | Unique identifier that contains information necessary to track back to the original record in the source dataset |
| SOURCE_SYSTEM_TYPE | Type of source database or system that the record was drawn from (federal, nonfederal, or interagency) |
| SOURCE_SYSTEM | Name of or other identifier for source database or system that the record was drawn from. See Table 1 in Short (2014), or \Supplements\FPAFODsourcelist.pdf, for a list of sources and their identifier. |
| NWCG_REPORTING_AGENCY | Active National Wildlife Coordinating Group (NWCG) Unit Identifier for the agency preparing the fire report (BIA = Bureau of Indian Affairs, BLM = Bureau of Land Management, BOR = Bureau of Reclamation, DOD = Department of Defense, DOE = Department of Energy, FS = Forest Service, FWS = Fish and Wildlife Service, IA = Interagency Organization, NPS = National Park Service, ST/C&L = State, County, or Local Organization, and TRIBE = Tribal Organization). |
| NWCG_REPORTING_UNIT_ID | Active NWCG Unit Identifier for the unit preparing the fire report. |
| NWCG_REPORTING_UNIT_NAME | Active NWCG Unit Name for the unit preparing the fire report. |
| SOURCE_REPORTING_UNIT | Code for the agency unit preparing the fire report, based on code/name in the source dataset. |
| SOURCE_REPORTING_UNIT_NAME | Name of reporting agency unit preparing the fire report, based on code/name in the source dataset. |
| LOCAL_FIRE_REPORT_ID | Number or code that uniquely identifies an incident report for a particular reporting unit and a particular calendar year. |
| LOCAL_INCIDENT_ID |  Number or code that uniquely identifies an incident for a particular local fire management organization within a particular calendar year. |
| FIRE_CODE | Code used within the interagency wildland fire community to track and compile cost information for emergency fire suppression ([https://www.firecode.gov/]). |
| FIRE_NAME | Name of the incident, from the fire report (primary) or ICS-209 report (secondary). |
| ICS_209_INCIDENT_NUMBER | Incident (event) identifier, from the ICS-209 report. |
| ICS_209_NAME | Name of the incident, from the ICS-209 report. |
| MTBS_ID | Incident identifier, from the MTBS perimeter dataset. |
| MTBS_FIRE_NAME | Name of the incident, from the MTBS perimeter dataset. |
| COMPLEX_NAME | Name of the complex under which the fire was ultimately managed, when discernible. |
| FIRE_YEAR | Calendar year in which the fire was discovered or confirmed to exist. |
| DISCOVERY_DATE | Date on which the fire was discovered or confirmed to exist. |
| DISCOVERY_DOY | Day of year on which the fire was discovered or confirmed to exist. |
| DISCOVERY_TIME | Time of day that the fire was discovered or confirmed to exist. |
| STAT_CAUSE_CODE | Code for the (statistical) cause of the fire. |
| STAT_CAUSE_DESCR | Description of the (statistical) cause of the fire. |
| CONT_DATE | Date on which the fire was declared contained or otherwise controlled (mm/dd/yyyy where mm=month, dd=day, and yyyy=year) |
| CONT_DOY | Day of year on which the fire was declared contained or otherwise controlled. |
| CONT_TIME | Time of day that the fire was declared contained or otherwise controlled (hhmm where hh=hour, mm=minutes). |
| FIRE_SIZE | Estimate of acres within the final perimeter of the fire. |
| FIRE_SIZE_CLASS | Code for fire size based on the number of acres within the final fire perimeter expenditures (A=greater than 0 but less than or equal to 0.25 acres, B=0.26-9.9 acres, C=10.0-99.9 acres, D=100-299 acres, E=300 to 999 acres, F=1000 to 4999 acres, and G=5000+ acres). |
| LATITUDE | Latitude (NAD83) for point location of the fire (decimal degrees). |
| LONGITUDE | Longitude (NAD83) for point location of the fire (decimal degrees). |
| OWNER_CODE | Code for primary owner or entity responsible for managing the land at the point of origin of the fire at the time of the incident. |
| OWNER_DESCR | Name of primary owner or entity responsible for managing the land at the point of origin of the fire at the time of the incident. |
| STATE | Two-letter alphabetic code for the state in which the fire burned (or originated), based on the nominal designation in the fire report. |
| COUNTY | County, or equivalent, in which the fire burned (or originated), based on nominal designation in the fire report. |
| FIPS_CODE | Three-digit code from the Federal Information Process Standards (FIPS) publication 6-4 for representation of counties and equivalent entities. |
| FIPS_NAME | County name from the FIPS publication 6-4 for representation of counties and equivalent entities. |
| SHAPE | :---- |

## Structure of project:
### Data Preparation:
Basic error-checking was performed and redundant records were identified and removed, to the degree possible.
Ignored data with fire class A and B (A=greater than 0 but less than or equal to 0.25 acres, B=0.26-9.9 acres) in order to optimize the data size.

Acknowledgements:
This data was collected using funding from the U.S. Government and can be used without additional permissions or fees. If you use these data in a publication, presentation, or other research product please use the following citation:
Short, Karen C. 2017. Spatial wildfire occurrence data for the United States, 1992-2015 [FPAFOD20170508]. 4th Edition. Fort Collins, CO: Forest Service Research Data Archive. https://doi.org/10.2737/RDS-2013-0009.4

### Exploratory Data Analysis
As part of EDA, statistical analysis on historical data is conducted to answer the inspiration.

### Conclusion
* After every 4-5 years the number of wildfires and area of destruction increases.
* Most of the wildfires are initiated by some or the other human activity. So we probably need more strict guidelines tobe followed in the forest zones

## Important Links

* [Final Report Notebook](report.ipynb)
* [EDA Notebook](eda.ipynb)
* [https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.isin.html](isin())
* [https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.replace.html](replace())
* [https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.pivot.html](pivot())
* [https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.DataFrame.plot.pie.html](pie plot)
