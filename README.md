# Analysis of geographical changes of small retail businesses in the U.S. 

## Data

This analysis uses two sources of data: 

- County Business Pattern data from the U.S. Census Bureau for five years, from 2022 through 2018. 
  - 'cbp22.co.csv': County Business Patterns in 2022
  - 'cbp21.co.csv': County Business Patterns in 2021
  - 'cbp20.co.csv': County Business Patterns in 2020
  - 'cbp19.co.csv': County Business Patterns in 2019
  - 'cbp18.co.csv': County Business Patterns in 2018
- 2023 Rural-Urban Continuum Code from the Economic Research Service of the U.S. Department of Agriculture
    - 'County_population.csv': County populations and 2023 Rural-Urban Continuum Code 

## Source

  The data was downloaded from the [Census County Business Patterns](https://www.census.gov/programs-surveys/cbp.html) and [USDA Rural-Urban Continuum Code](https://www.ers.usda.gov/data-products/rural-urban-continuum-codes/documentation/) respectively. 

## Methodology 

The notebook [small_retail_biz_counties.ipynb] (notebooks/small_retail_biz_counties.ipynb) performs the following analysis:

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

## Re-using the analysis

You are welcome to use this analysis

## About me

Coralie Carlson is a data journalism student at the Craig Newmark CUNY School of Journalism. She can be reached at coralie.carlson24@journalism.cuny.edu. 

