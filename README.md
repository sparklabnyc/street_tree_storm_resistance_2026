# Identification and Spatial Distribution of Storm-Resilient Street Tree Species in New York City

**Authors:**
Ann Zhao Dai, mentored by Dr. Robbie M. Parks and Dr. Anna Palmer, 2026

---

## Project Description

As climate change leads to increased storm hazard severity, the health and structural integrity of street trees are compromised due to damage from high winds and waterlogging from flooding. This project uses a logistic regression model to investigate the relationship between an individual tree's species and intensity of storm damage based on work order data compiled in the NYC Department Parks & Recreation's Forestry Management System. The spatial distribution of the most and least resilient tree species will then be compared to currently identified high-risk flooding areas and Environmental Justice (EJ) Areas in New York City.

* Paper: [Insert link]
* Repository: https://github.com/sparklabnyc/street_tree_storm_resistance_2026

---

## 1. Data

### 1a_raw

* Raw service request data (NYC Forestry Services/NYC Open Data), storm history (NYC Office of Emergency Management Hazard History & Consequence tool), and tree map data (NYC Department of Parks & Recreation)

### 1b_processed

* hazard_history.csv: high wind, coastal flooding, flash flooding, heavy snow, freezing precipitation storm events from 2015-2026 w/ intensity data and duration
* service_requests.csv: tree-related service requests from 2015 to June 2026 w/ location information
* tree_map.csv: all street trees in New York City w/ species, location, and diameter at breast height (DBH)

### 1c_intermediate

* storm_service_requests.csv: service requests reported during and within 24 hours of a storm event

### 1d_support

* 2020_Neighborhood_Tabulation_Areas_(NTAs)_20260624.geojson: shapefile of NYC neighborhood tabulation areas
* crown_equations.csv: list of equations used to estimate crown width of trees based on order/genus/species and DBH (i-Tree Tools)
* height_equations.csv: list of equations used to estimate height of trees based on order/genus/species and DBH (i-Tree Tools)
* nyc_approved_species.csv: list of trees approved for street planting (NYC Dept. of Parks and Recreation)
* selected_species.csv: list of 20 trees selected for further analysis based on prevalence and known storm resilience

### 1e_summary

* tree_map_metrics.csv: all street trees in NYC with location, species, DBH, estimated height + crown diameters, storm intensity PCA1, serviced/nonserviced

---

## 2. Code

### 2a_dataprep
* **2a_00_process_datasets**: filtering/cleaning raw data; in particular: making addresses consistent for readability, reformatting datetimes and geometry variables for joining
* **2a_01_prep_servicedtrees**: join service requests & hazard history by datetime to get 1b_stormservicerequests_data --> join with tree map data by geometry

### 2b_treemetrics

* **2b_tree_metrics**: estimate crown width and height of serviced trees with i-Tree tools equations
* **2b_full_treemap**: estimate crown width and height of non-serviced trees; create combined dataset of all street trees w/ metrics

### 2c_expanalysis

* **2c_exp_analysis**: exploratory analysis and graphs to characterize full tree map data
* **2c_neighborhood_311_requests**: create heatmap of service request to total tree ratio for all NYC neighborhoods
* **2c_regression_model**: exploratory regression model with all approved tree species

### 2d_selectedanalysis
* **2d_selected_analysis**: graphs characterizing 20 selected tree species
* **2d_selected_regression**: regression model of 20 selected tree species + associated visualizations of results

### Setup

* Data preparation scripts
* Helper functions

---

## 3. Output

* **3a_[output_name]**: Description
* **3b_[output_name]**: Description
* **3c_[output_name]**: Description
* **3d_[output_name]**: Description

---

## 4. Sensitivity Analysis

* Description of robustness checks
* Alternative assumptions

---

## Directory Structure

├── 01_data
│   ├── 1a_raw
│   │   ├── Forestry_Service_Requests_20260609.csv
│   │   ├── NYCStormHazards.csv
│   │   ├── nyc_trees_all.csv
│   ├── 1b_processed
│   │   ├── hazard_history.csv
│   │   ├── service_requests.csv
│   │   ├── tree_map.csv
│   ├── 1c_intermediate
│   │   ├── storm_service_requests.csv
│   ├── 1d_support
│   │   ├── 2020_Neighborhood_Tabulation_Areas_(NTAs)_20260624.geojson
│   │   ├── crown_equations.csv
│   │   ├── height_equations.csv
│   │   ├── nyc_approved_species.csv
│   │   ├── selected_species.csv
│   ├── 1e_summary
│   │   ├── serviced_trees.csv
├── 02_code
│   ├── 2a_dataprep
│   │   ├── 2a_00_process_datasets.Rmd
│   │   ├── 2a_01_prep_servicedtrees.Rmd
│   ├── 2b_treemetrics
│   │   ├── 2b_01_tree_metrics.Rmd
│   │   ├── 2b_02_full_treemap.Rmd
│   ├── 2c_expanalysis
│   │   ├── 2c_exp_analysis.Rmd
│   │   ├── 2c_neighborhood_311_requests.Rmd
│   │   ├── 2c_regression_model.Rmd
│   ├── 2d_selectedanalysis
│   │   ├── 2d_selected_analysis.Rmd
│   │   ├── 2d_selected_regression.Rmd
├── 03_output
│   ├── figures
│   ├── tables
├── 04_sensitivity
├── shiny_app (optional)
├── README.md
---

## How to Run

git clone <repo_url>
cd <repo_name>

# Run setup scripts

# Run analysis scripts

---

## Dependencies

* R 4.5.2
* Key packages:

  * tidyverse
  * readr
  * fuzzyjoin
  * sf
  * ggplot2

---

## Data Availability

* Forestry service request data are freely available though [NYC Open Data](https://data.cityofnewyork.us/Environment/Forestry-Service-Requests/mu46-p9is)
* New York City severe weather history is freely available and filterable through the [NYC Hazard History and Consequence Tool](https://nychazardhistory.com/)
* Street tree data is freely available through the [NYC Department of Parks & Recreation](https://tree-map.nycgovparks.org/)


---

## Citation

[Authors]. (Year). Title. Journal/Repository.

---

## Contact

Ann Zhao Dai | azd2104@barnard.edu

Barnard College, Department of Biological Sciences

Columbia University Mailman School of Public Health, Department of Environmental Health Sciences
