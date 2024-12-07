# Analysis of geographical changes of small retail businesses in the U.S. 

The analysis of Census Bureau data shows the changes in the number of small retail businesses, often called mom-and-pop shops, annually from 2018 to 2022. It also breaks down changes in the number of small retail businesses by three geographical factors:
- by county 
- by population of county (urban, suburban, rural)
- by state 

You can see a story resulting from the population of county here: [Mom-and-Pop Retailers Thrive in Rural Areas While Folding Elsewhere](https://coveringcompanies.journalism.cuny.edu/2024/12/06/mom-pop-retailers-thrive-in-rural-areas-while-folding-elsewhere/)

I hope to do further reporting using the statewide data in the future. 

## Data

This analysis uses two sources of data: 

- County Business Pattern data from the U.S. Census Bureau for five years, from 2022 through 2018. **Note these files are compressed to be hosted on GitHub.**
  - 'cbp22.co.csv.zip': County Business Patterns in 2022
  - 'cbp21.co.csv.zip': County Business Patterns in 2021
  - 'cbp20.co.csv.zip': County Business Patterns in 2020
  - 'cbp19.co.csv.zip': County Business Patterns in 2019
  - 'cbp18.co.csv.zip': County Business Patterns in 2018
- 2023 Rural-Urban Continuum Code from the Economic Research Service of the U.S. Department of Agriculture
    - 'County_population.csv': County populations and 2023 Rural-Urban Continuum Code

## Source

  The data was downloaded from the [Census County Business Patterns](https://www.census.gov/programs-surveys/cbp.html) and [USDA Rural-Urban Continuum Code](https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/documentation/) respectively. 

## Methodology 

The notebook [small_retail_biz_counties.ipynb](notebooks/small_retail_biz_counties.ipynb) performs the following analysis:

#### Part 1: Clean the business data

- Read csv files for each year and interpret fips as strings
- Make new column of naics sector code (first two digits) 
- Make a new column of FIPS that is fipstate + fipscty
- Make dataframe  of only NAICS retail code (44, 45) 


#### Part 2: Merge county population data with small business data 

- Import population data 
- Merge population info with small retail dataframes for each year 


#### Part 3: Count number of small retail businesses in each county, type of county, and state 

- Groupby counties (Number of small retail businesses in each county)
- Groupby rural/urban codes (number of small retail businesses in each population type)
- Groupby state (number of small retail businesses per state) 


## Outputs

The results of "Part 3" above are saved as:
  [`output/county_counts22.csv`](output/county_counts22.csv).
  [`output/county_counts21.csv`](output/county_counts21.csv).
  [`output/county_counts20.csv`](output/county_counts20.csv).
  [`output/county_counts19.csv`](output/county_counts19.csv).
  [`output/county_counts18.csv`](output/county_counts18.csv).
  [`output/rural_sub_urban22.csv`](output/rural_sub_urban22.csv).
  [`output/rural_sub_urban21.csv`](output/rural_sub_urban21.csv).
  [`output/rural_sub_urban20.csv`](output/rural_sub_urban20.csv).
  [`output/rural_sub_urban19.csv`](output/rural_sub_urban19.csv).
  [`output/rural_sub_urban18.csv`](output/rural_sub_urban18.csv).
  [`output/state_counts22.csv`](output/state_counts22.csv).
  [`output/state_counts21.csv`](output/state_counts21.csv).
  [`output/state_counts20.csv`](output/state_counts20.csv).
  [`output/state_counts19.csv`](output/state_counts19.csv).  
  [`output/state_counts18.csv`](output/state_counts18.csv).

  
## Google Sheet Analysis

-The outputs were imported into [Google Sheets](https://docs.google.com/spreadsheets/d/1YxHu60qwivQvLwmKJlBXo6i-vKKmBbSIG96tPz15660/edit?usp=sharing) for comparison and to determine percent change by year and by five years. 
-The results of that analysis can be found in the outputs folder: 
  -['output/Google_Sheets_county_counts.csv.zip'](output/Google_Sheets_county_counts.csv.zip)
  -['output/Google_Sheets_state_counts.csv'](output/Google_Sheets_state_counts.csv)
  -['output/Google_Sheets_rural_sub_urban22.csv'](output/Google_Sheets_rural_sub_urban22.csv)

## Re-using the analysis

You are welcome to use this analysis.

## About me

Coralie Carlson is a data journalism student at the Craig Newmark CUNY School of Journalism. She can be reached at coralie.carlson24@journalism.cuny.edu. 

