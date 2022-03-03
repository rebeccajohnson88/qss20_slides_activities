# PHA attributes: Section 8 study

Code related to spatial analysis for Sec 8 preferences study with [Simone Zhang](https://github.com/sxzh)


# Order to run

1. [0_loadPHApolygons_loadTractpolygons.Rmd](https://github.com/rebeccajohnson88/spatialanalysis_sec8study/blob/master/code/0_loadPHApolygons_loadTractpolygons.Rmd)

- Takes in:
  - Shapefiles from HUD's Estimated Housing Authority Service Area data: https://hudgis-hud.opendata.arcgis.com/datasets/estimated-housing-authority-service-areas
  - Tract shapefiles created by the script that uses `tigris` package to pull tracts for all state codes represented in the PHA data, and row bind them into a single file: [0helper_pull_tract_shapefiles.R](https://github.com/rebeccajohnson88/spatialanalysis_sec8study/blob/master/code/0helper_pull_tract_shapefiles.R)
  
- What it does:
  - Converts each to format usable by `sf` package and reconciles projections
  - Adds state fips code so that only PHAs and tracts within the same state are compared (helps with spatial overlap runtime)
  - Tests different overlap logics (intersect versus within) with one PHA and one state's tracts to build intuition
  - Tests plotting
  
- Outputs:
  - Two .RDS files, each containing `sf` format spatial polygon data for all US census tracts and all PHAs respectively
    1. tracts_foroverlap.RDS
    2. phas_foroverlap.RDS
  
2. [1_spatialmerge_loopcode.R](https://github.com/rebeccajohnson88/spatialanalysis_sec8study/blob/master/code/1_spatialmerge_loopcode.R)

- Takes in:
  - .RDS files created in step 1
  
- What it does:
  - Iterates through states and subsets to PHAs in that state
  - Uses `st_intersection` logic to find the overlap between tract polygons and PHA service area polygons
  
- Outputs:
  - One .RDS file per state that contains: 1) metadata on tracts and PHAs; 2) geometrys for the PHAs only. Named with naming convention: `stateabbrev_intersects.RDS`
  
3. [2_pull_census_tractlevel.Rmd](https://github.com/rebeccajohnson88/spatialanalysis_sec8study/blob/master/code/2_pull_census_tractlevel.Rmd)

- Takes in:
  - .RDS files created by previous step
  - API key for census

- What it does:
  - Reads in RDS files and pulls their GEOIDs (identifier for tracts)
  - Connects to census API via `tidycensus` and pulls education, housing, race/ethnicity, and poverty-related vars for all states from the 2016 5-year ACS (2012-2016)
  - Left joins that census info with the long-form data from the .RDS files, where each PHA is repeated for all the tracts it intersects with (varies a lot across PHAs; for some, contains 2000+ tracts like the state-level PHAs of `TX901` and `NY904`; mean is 55 tracts that intersect with the PHA)
  
- Outputs:
  - phas_wrawACScounts.RDS
  
4. [3_add_all_attributes_tobaseHUD_df.Rmd](https://github.com/rebeccajohnson88/spatialanalysis_sec8study/blob/master/code/3_add_all_attributes_tobaseHUD_df.Rmd)

- Takes in:
  - RDS file created in previous steps
  - County-level data on housing affordability compiled by Urban Institute 
  - County-level data on 2012 and 2016 national election returns compiled by researchers here: https://dataverse.harvard.edu/dataset.xhtml?persistentId=doi:10.7910/DVN/VOQCHQ.
  - Tract-level data on RUCA classifications from here: https://www.ers.usda.gov/data-products/rural-urban-commuting-area-codes.aspx
  - Tract-level data on registered nonprofits (NCCS core data files from here: https://nccs-data.urban.org/index.php)
  - Base file on PHA universe and attributes (shared by HUD spatial data coordinator)

- What it does:
  - Aggregates tract-level census characteristics to PHA level characteristics. Aggregation logic for count variables is to: 1) sum numerator across tracts; 2) sum relevant denom across tracts; 3) calculate percentage at the PHA level. Aggregation logic for continuous vars is mean. 
  - Left joins those to base data
  - Left joins above to housing affordability data
  - Left joins above to election returns data
  
- Coding notes (see code for more details):

  - Urbanicity classification: following other articles (e.g., https://journals.sagepub.com/doi/full/10.1177/0890117116689488?casa_token=U_sy2_vuNhcAAAAA%3AMGbxPDj44_4Mo5ETpBZwkNzvmOp4zBtPLNx65GrreH0JCPOyVes24Usg95N_3RBQvIxX2mWFBKk), we create two dummy indicators for each tract: urban (ruca codes 1-3); rural (ruca codes 4-10).
 
  
- Outputs:
  - .csv file where each row is a PHA and vars correspond to contextual information; with data source marked with a prefix (e.g. HUD v ACS): [pha_wlocalattributes.csv](https://github.com/rebeccajohnson88/spatialanalysis_sec8study/blob/master/output/pha_wlocalattributes.csv)
  

