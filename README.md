# A Century of Variability of Heatwave-Driven Streamflow in Melt-Driven Basins and Implications Under Climate Change  

This repository contains the code and data required to reproduce the analysis in the study: Anderson, S. and Chartrand, S. "A Century of Variability of Heatwave-Driven Streamflow in Melt-Driven Basins and Implications Under Climate Change" (2024, in review).

<img src= "https://github.com/andersonsam/heatwave_century_observations/blob/main/Figures/Q_labels.png" width=100% >

___  

## Data 

**Weather station data**
  * [Metadata for all Canadian weather stations](https://collaboration.cmc.ec.gc.ca/cmc/climate/Get_More_Data_Plus_de_donnees/) (used in Step 1) 
  * [Historical weather data](https://climate.weather.gc.ca/index_e.html), downloaded in Step 2 using [command line (template)](https://collaboration.cmc.ec.gc.ca/cmc/climate/Get_More_Data_Plus_de_donnees/Command_Lines_EN.txt)  

**Streamfow data**
  * [Metadata for the Reference Hydrometric Basin Network](https://collaboration.cmc.ec.gc.ca/cmc/hydrometrics/www/RHBN/) (used in Step 1) 
  * [Metadata and streamflow data for stations in the HYDAT dataset](https://collaboration.cmc.ec.gc.ca/cmc/hydrometrics/www/) (used in Step 1, Step 3, and Step 4) 

**CMIP6 data**
  * [Tabular data for all scenarios](https://climate-scenarios.canada.ca/?page=cmip6-scenarios) (used in Step 4) 

**Topographic data** 
  * [Shuttle Radar Topography Mission](https://agupubs.onlinelibrary.wiley.com/doi/full/10.1029/2005RG000183) (used in Step 4)

**Glacier location data** 
  * [Randolph Glacier Inventory V6.0](https://www.glims.org/RGI/randolph60.html) (used in Step 4)

___ 

## Running the code  

### Step 1: Identify streamflow and weather stations 

Run the notebook 'station_selection.ipynb' to determine sets of streamflow and weather stations for analysis.

### Step 2: Download weather station data  

Use the scripts provided in 'weather_download_scripts.ipynb' to download weather station data. 

### Step 3: Download streamflow data  

Access and download streamflow data from the HYDAT database.

### Step 4: Run the main analysis  

Run the notebook 'main.ipynb' to run the analysis using the streamflow and weather station data.

___ 

## Directory structure 

heatwave_century_observations 
* main.ipynb 
* station_selection.ipynb 
* weather_download_scripts.ipynb
* Data
  * Banff
    * 05BB001_daily_20230509T1542.csv (Streamflow)
    * en_climate_daily_AB_3050520_1909_P1D.csv (Weather -- one file per year) 
  * Chilliwack
    * daily_20230518T1759.csv (Streamflow)
    * en_climate_daily_BC_1101530_1911_P1D.csv (Weather -- one file per year)
  * Columbia_Golden
    * daily_2023_0518T1900.csv (Streamflow)
    * en_climate_daily_BC_1173210_1903_P1D.csv (Weather -- one file per year)
  * Fort_St_James
    * daily_20230517T1816.csv (Streamflow)
    * en_climate_daily_BC_1092970_1895_P1D.csv (Weather -- one file per year)
  * Pemberton
    * daily_20230524T2041.csv (Streamflow)
    * en_climate_daily_BC_1086090_1912_P1D.csv (Weather -- one file per year)
  * Similkameen_Princeton
    * daily_20230518T1801.csv (Streamflow)
    * en_climate_daily_BC_1126510_1936_P1D.csv (Weather -- one file per year)
  * CMIP6
    * Individual files for variables ('pr', 'snd', 'tas'); seasons; and time periods 
  * Station Inventory EN.csv
  * HydatStations_all.csv
  * RHBN_Metadata.csv
