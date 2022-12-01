# vininggrainger872
872 Project (Matthew V and Rachael G)

# <Environmental Benefits and Costs in North Carolina>

## Summary

Project Central Question:
How do communities in North Carolina experience varying levels of environmental factors and energy access, with a particular lens on environmental justice communities?

Potential Hypothesis:
As the birthplace of the environmental justice movement, North Carolina is no stranger to environmental injustices. We expect that today Hog farms will still be correlated/concentrated in communities of higher social vulnerability (i.e., lower SES, predominantly nonwhite) across North Carolina. We also predict that energy systems, such as solar farms, will be concentrated in communities of lower social vulnerability (i.e., higher SES, predominately white) areas in North Carolina or have no correlation .

## Investigators

Rachael Grainger - Master's of Public Policy at Duke's Sanford School of Public Policy

Matthew Vining - Master's of Public Policy, Concentration in Energy & Environment at Duke's Sanford School of Public Policy

## Keywords

Environmental Justice - Environmental justice is the fair treatment and meaningful involvement of all people regardless of race, color, national origin, or income, with respect to the development, implementation, and enforcement of environmental laws, regulations, and policies.

Utility-scale - large scale energy generation of atleast 1 MW in power generation capacity.

Social Vulnerability Index - refers to the potential negative effects on communities caused by external stresses on human health. Such stresses include natural or human-caused disasters, or disease outbreaks. Reducing social vulnerability can decrease both human suffering and economic loss. 


## Database Information
Data was gatherered from multiple online sources.

Data for solar plants was gathered from the EIA Database for the year 2021. We accessed the data from EIA on 11/19/2022. Two datasets were downloaded: 

All plant data (xlsx): https://www.eia.gov/electricity/data/eia923/ 

Renewable level data (xlsx): https://www.eia.gov/electricity/data/eia860/

Data for hog farms was gathered from the NC Department of Environmental Quality data set on animal operations permitting for the year 2018. This data was accessed on 11/18/2022. The dataset that was downloaded is:

Animal Operation Permits (csv): https://data-ncdenr.opendata.arcgis.com/datasets/b4b0eb98084f4260acc3224970443f5c_0/explore?location=35.014194%2C-77.930084%2C9.32 


The third and final set of data downloaded for the project was the CDC/ATSDR (Census) Social Vulnerability Index for the year 2018. This data was first accessed on 11/18/2022. The dataset that was downloaded is below. It includes data on social vulnerability by county, as well as information for the boundaries of NC counties.

SVI county-level data (csv): https://svi.cdc.gov/Documents/Data/2018_SVI_Data/CSV/States_Counties/NorthCarolina_COUNTY.csv


## Folder structure, file formats, and naming conventions 

File organization for the project focused on separating the project file and ReadMe file from the data and template files. The main repository contains the Rmd file, knitted project file, ReadME file (this one) and folder containing project files used to create the code structure and analyze data. Within the project folder is the raw and spatial data analyzed. The README template that this document is based off of is also located in that folder. The Raw Data folder contains the original three datafiles downloaded, csv and xlsx format. When the raw data files were manipulated to become shapefiles or other spatial category file, they were stored in the Spatial folder. Our naming convention was simple, labeling all files contained in the Rmd file as project folder, anything relevant to executing this project. The two data folder within were categorized based on the type of data that was produced or downloaded - spatial and raw.

## Metadata

<For each data file in the repository, describe the data contained in each column. Include the column name, a description of the information, the class of data, and any units associated with the data. Create a list or table for each data file.> 

## Scripts and code

<list any software scripts/code contained in the repository and a description of their purpose.>
#what does this mean??

## Quality assurance/quality control
To ensure quality of data, data files were downloaded from government or academic based sources only. All of our data was either census or government department based and published on a safe and secure network. Whend data was loaded into R, each file was looked at to ensure the class of data was correct, numeric vs character. When converting data to a shapefile or using coordinates, we also made sure to align coordinate systems for data from different sources to ensure they were being mapped correctly. 

<describe any relevant QA/QC procedures taken with your data. Some ideas can be found here:>
<https://www.dataone.org/best-practices/develop-quality-assurance-and-quality-control-plan>
<https://www.dataone.org/best-practices/ensure-basic-quality-control>
<https://www.dataone.org/best-practices/communicate-data-quality>
<https://www.dataone.org/best-practices/identify-outliers>
<https://www.dataone.org/best-practices/identify-values-are-estimated>