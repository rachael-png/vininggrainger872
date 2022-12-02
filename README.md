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


Animal Operations: This dataset contains the active animal permits for North Carolina animal farming operations. This data is from 2018 and has not been updated. 

- X: X coordinate (num)
- Y: Y coordinate (num)
- FID: Number in the dataset. (chr)
- Permit: The farm permit number. (chr)
- Permittee: The name of the person who applied and received a permit. (chr)
- Facility: The name of the farm facility. 
- Type: The type of animal operation facility. This can be Swine (hog farms), Cattle, Poultry, or Animal Individual State. (chr)
- Region: Larger category than county, that encompasses a specific region in North Carolina. (chr)
- County: The county where the farm is located. (chr)
- FirstIssue: When the very first permit was issued. (chr)
- Issued: When the permit was issued/renewed. (chr)
- Expires: When the permit expires. (chr)
- Status: Active or inactive farm. (chr)
- Latitude: Latitude of the farm. (num)
- Longitude: Longitude of the farm. (num)

Counties_Percent: This datafile contains spatial information for North Carolina counties as well as poverty and minority estimates for each county. 

- STATEFP: (chr) State-level FIPS code.
- COUNTYFP: (chr) County-level FIPS code
- COUNTYNS: (chr) Unknown number associated with counties.
- AFFGEOID: (chr) For creating shapes if converted to a shape file.
- GEOID: (chr) For creating shapes if converted to a shape file.
- NAME: (chr) Name of county. 
- LSAD: (chr) Unknown number.
- ALAND: (num) Area of land.
- AWATER: (num) Area of water.
- COUNTY: (chr) County name.
- LOCATION: (chr) Text description of tract, county, state.
- E_TOTPOP: (num) Estimate of the total population by county.
- E_POV: (num) Estimate of the total population in poverty by county.
- E_MINRTY: (num) Estimate of the total population that is nonwhite by county.
- geometry: (list) Spatial coordinates. 
- PovertyPerc: (num) Estimate of the total percent population in poverty by county.
- MinorityPerc: (num) Estimate of the total percent population that is nonwhite by county.

Solar_Plants_NC: this file was combined with all plant data and solar data file for the useable data needed for the project. It contains the following column variables:

- Utility ID: (num) identifying number that is associated with the utility the solar farm is connected to 
- Utility Name: (chr): name of the utility that the solar farm is connected to
- Plant Code: (num) numeric code that the EIA gives an individual energy plant
- Plant Name: (chr) Name of the energy plant/solar farm
- State:(chr) state where the energy plant/solar farm is located
- County: (chr) county in which the energy plant/solar farm is located in
- Generator ID: (chr) numeric identifier for the company/org that generates the energy 
- Status: (chr) labels the operating status of the energy plant
- Technology: (chr) describes the technology used to generate energy
- Nameplate Capacity (MW): (num) value associated with the energy generating capacity
- Summer Capacity (MW): (num) value associated with the energy generating capacity for the summer months
- Winter Capacity (MW): (num) value associated with the energy generating capacity for the winter months
- Street Address: (chr) Address where the facility is located
- City: (chr) city in which the facility is located
- Zip: (num) zip code in which the facility is located
- Latitude: (num) latittude coordinates for location of facility
- Longitude: (num) longitude coordinates for location of facility



## Scripts and code

Packages used:
dplyr - Tools for Splitting, Applying and Combining Data
plyr - Tools for Splitting, Applying and Combining Data
lubridate - For changing and assigning dates, if needed.
tidyverse - For data manipulation.
sf - For changing data into spatial formats for spatial analysis and mapping.
mapview - For quickly viewing maps/spatial data, if needed.
RColorBrewer - for creating color palettes
readxl - for reading excel data formats.
leaflet - for creating our maps.
viridis - for assigning map colors.


## Quality assurance/quality control
To ensure quality of data, data files were downloaded from government or academic based sources only. All of our data was either census or government department based and published on a safe and secure network. Whend data was loaded into R, each file was looked at to ensure the class of data was correct, numeric vs character. When converting data to a shapefile or using coordinates, we also made sure to align coordinate systems for data from different sources to ensure they were being mapped correctly. 

<describe any relevant QA/QC procedures taken with your data. Some ideas can be found here:>
<https://www.dataone.org/best-practices/develop-quality-assurance-and-quality-control-plan>
<https://www.dataone.org/best-practices/ensure-basic-quality-control>
<https://www.dataone.org/best-practices/communicate-data-quality>
<https://www.dataone.org/best-practices/identify-outliers>
<https://www.dataone.org/best-practices/identify-values-are-estimated>