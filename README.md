# GEOG5990M Final Project
## Health and Wealth. An investigation into the correlation between property value and access to Health Service in London 

### Project Rational
Equity of access has been a focus of the NHS since it began in 1948 (Goodard and Smith, 2001) and with most research suggesting that low income has a direct correlation with heath care utilization (Copper et al, 2012), It is clear that lower socio-economic areas require improved access to support its populations. In contrast to this, property value has been shown to increase with proximity to local services, including hospitals and other health care services (Chen et al, 2022), making areas that provide the most support less accessible to the communities that need them most. 
As a result, it is the aim of this investigation to explore how median property value of each Lower Layer Super Output Area (LSOA) in Greater London is affected by the distance to 5 different health services and in relation to a an overall weighted mean distance from health services in each LSOA. This is undertaken with the aim of assisting in regional assessment and policy making to determine if an increase in support and infrastructure may be necessary to support local communities. We will also explore this relationship at the Local Authority District (LAD) spatial scale, to provide support at the borough level where decisions are made within London. 


### Data
Four datasets are included in this report.
First, [‘ahah_v4.csv’](ahah_v4.csv) is a CSV file of open data on distance to health-related services in Great Britain (link)  Accessed July 2025 the data the data frame consists of 14 services that may affect health and an appropriate value. The variables selected for this investigation were those directly linked to health services, these include Dentists (ah4dent), Pharmacies (ah4phar) , Hospitals (ah4hosp), GPs (ah4gp), Leisure Centers (ah4leis).
The location of services was originally sourced from the ODS Access Database of NHS Digital and a local data company for Leisure centers and collated by Geographic Data service. Version 4 was used which included the most up to date data released in 2024. 
The time to service was calculated using Routino Open Source software (www.routino.org) to find the shortest path between the population weighted centroid of each postcode (Daras et al, 2019) and aggregated to the spatial scale of Lower Super Output Area (LSOA) using the mean value. 
Two points of note on this dataset is that hospitals were only included if an A&E was present to remove specialist or referral facilities and Leisure centers were included as a health service due to the direct positive effect these have on personal health (Darras et al, 2019). 

