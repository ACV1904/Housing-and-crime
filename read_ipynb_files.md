**shapeMSOA.ipynb**
This code uses the following files:
- 'MSOA_2021_EW_BFE_V7.shp' downloaded from [Open Geography Portal: MSOA 2021 boundaries] (https://geoportal.statistics.gov.uk/datasets/ons::middle-layer-super-output-areas-december-2021-boundaries-ew-bfe-v7/about)
- 'LondonMSOAs.csv' this is a list of al the MSOAs codes (and names) in London, produced in Excel from another Nomis dataset, saved as csv.
The shapefile 'London_MSOA.shp' is produced with the boundaries of the London MSOAs.
This code also explores the spatial weights in London MSOAs and number of neighbours.  


**police_msoa.ipynb**
The code uses the following files:
- 'PoliceData2021/*.csv' from https://data.police.uk/data/ as a zip file.
- 'London_MSOA.shp' produced in the file shapeMSOA.ipynb
- 'est-population-2021.csv' from [ONS, MSOA population estimates 2021] (https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates/datasets/middlesuperoutputareamidyearpopulationestimates) and cleaned in Excel as csv.
- 'total_dwellings.csv' from [Nomis RM204: Number of dwellings] (https://www.nomisweb.co.uk/datasets/c2021rm204) and cleaned in Excel as csv.
At the end this file produces the dataframe 'dcrl.csv' with the logarithms of crimes rates for: Total crime, Violence and Sexual Offences, Anti-social behaviour crimes and Burglaries.


**hpsm.ipynb**
The file was used to preprocess the house price per square metre dataset. 
The code uses the following files:
- 'la-names.csv' list of local authorities in London, produced in Excel and formatted to match the names of the files from the hpsm dataset.
- 'hpm_la_2023' decompressed folder downloaded from [House price per square metre dataset 2023] (https://data.london.gov.uk/dataset/house-price-per-square-metre-in-england-and-wales)
- 'PCD_OA21_LSOA21_MSOA21_LAD_AUG23_UK_LU.csv' downloaded from [ONS, Open geography portal: Postcode lookup (2023)] (https://open-geography-portalx-ons.hub.arcgis.com/datasets/ons::postcode-to-oa-2021-to-lsoa-to-msoa-to-lad-august-2023-best-fit-lookup-in-the-uk/about)
- 'local-authorities-names.csv' list of names of local authorities in London, produced in Excel.


**housing.ipynb** 
The file was used to process the downloaded datasets from the Nomis website, including the deprivation dataset. The cluster analysis is also here. It uses the following files:
- 'total_dwellings.csv' from [Nomis RM204: Number of dwellings] (https://www.nomisweb.co.uk/datasets/c2021rm204) and cleaned in Excel as csv.
- 'Tenure.csv' from [Nomis TS054: Tenure](https://www.nomisweb.co.uk/datasets/c2021ts054) 
- 'ts011-deprived.csv' from [Nomis TS011: Households by deprivation dimensions] (https://www.nomisweb.co.uk/datasets/c2021ts011) 
- 'accommodationtype.csv' from [Nomis TS044: Accommodation type] (https://www.nomisweb.co.uk/datasets/c2021ts044)

**Analysis.ipynb**
The file was used to do all the analyses between variables. 
It uses the following files:
- 'London_MSOA.shp' produced in shapeMSOA.ipynb
- 'dcrl.csv' produced in police_msoa.ipynb
- 'deprivation-rates.csv' produced in housing.ipynb
- 'hpsm.csv' produced in  hpsm.ipynb
- 'tenure-rates.csv' produced in housing.ipynb
- 'vacants.csv' produced in housing.ipynb
- 'accommodation-rates.csv' produced in housing.ipynb
- 'enc-vars.csv' produced in housing.ipynb
- 'Distance-Westminster018.csv' produced in QGIS using the file 'London_MSOA.shp'