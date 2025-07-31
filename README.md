# GEOG5990M Final Project
## Health and Wealth. An investigation into the correlation between property value and access to Health Services in London 

### Project Rational
Equity of access has been a focus of the NHS since it began in 1948 (Goodard and Smith, 2001) and with most research suggesting that low income has a direct correlation with heath care utilization (Copper et al, 2012), It is clear that lower socio-economic areas require improved access to support its populations. In contrast to this, property value has been shown to increase with proximity to local services, including hospitals and other health care services (Chen et al, 2022), making areas that provide the most support less accessible to the communities that need them most. 
As a result, it is the aim of this investigation to explore how median property value of each Lower Layer Super Output Area (LSOA) in Greater London is affected by the distance to 5 different health services and in relation to a an overall weighted mean distance from health services in each LSOA. This is undertaken with the aim of assisting in regional assessment and policy making to determine if an increase in support and infrastructure may be necessary to support local communities. We will also explore this relationship at the Local Authority District (LAD) spatial scale, to provide support at the borough level where decisions are made within London. 


### Data
Four datasets are included in this report.

First, [‘ahah_v4.csv’](ahah_v4.csv) is a CSV file of open data on distance to health-related services in Great Britain (link)  Accessed July 2025 the data the data frame consists of 14 services that may affect health and an appropriate value. The variables selected for this investigation were those directly linked to health services, these include Dentists (ah4dent), Pharmacies (ah4phar) , Hospitals (ah4hosp), GPs (ah4gp), Leisure Centers (ah4leis).
The location of services was originally sourced from the ODS Access Database of NHS Digital and a local data company for Leisure centers and collated by Geographic Data service. Version 4 was used which included the most up to date data released in 2024. 
The time to service was calculated using Routino Open Source software (www.routino.org) to find the shortest path between the population weighted centroid of each postcode (Daras et al, 2019) and aggregated to the spatial scale of Lower Super Output Area (LSOA) using the mean value. 
Two points of note on this dataset is that hospitals were only included if an A&E was present to remove specialist or referral facilities and Leisure centers were included as a health service due to the direct positive effect these have on personal health (Darras et al, 2019). 

The second data set [‘land-registry-house-price-Median-LSOA.csv’](land-registry-house-prices-Meidan-LSOA.csv) provides the median value of property in a csv format (Ref).  This was originally calculated from price paid data published on the Land Registry Website. This was then aggregated to the LSOA level by London Data Store. Median was chosen as when dealing with house price that generally exhibit extreme values it is a more recognized metric in this field (Vaidynathan, D et al, 2023) 
The dataset spans the period of 1995 to 2017, however in this investigation the year of 2016 was used as this provides the most complete data. Spatial extent is limited to only London boroughs.  The data was published in August 2018 and access July 2025.  

As the property value data was created before 2021 the data used 2011 LSOA classification codes and so the conversion csv file [‘LSOA_(2011)_to_LSOA_(2021)_to_Local_Authority_District_(2022)_Best_Fit_Lookup_for_EW_(V2).csv’](LSOA_(2011)_to_LSOA_(2021)_to_Local_Authority_District_(2022)_Best_Fit_Lookup_for_EW_(V2).csv) was used to as accurately as possible convert these to a code that could be combined across data sets. This was published August 23,2022 and accessed July 2025.

Finally, an Administrative Boundaries Geojson file ‘Local_Authority_Districts_May_2024_Boundaries_UK_BFE_2410925873296837173.geojson’ was used from the Office for National Statistics. The 2024 version of digital vector boundaries was published on July 2, 2024. This database contained Local Area District (LAD) boundaries as this spatial scale was deemed more appropriate for purpose and detail. 


(land-registry-house-prices-Meidan-LSOA.csv)
