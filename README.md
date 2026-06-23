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

* 1a_servicerequest_data: processed data on service requests called into NYC Parks & Recreation Department

* 1a_treemap_data: processed street tree data from NYC Parks & Recreation Department

* 1a_hazardhistory_data: processed dated storm data from NYC Emergency Management

### 1b_intermediate

* 1b_stormservicerequests_data: only service requests called in within 24 hours of a severe storm event

### 1c_support

* 1c_citree_species_characteristics: characteristics of different urban tree species compiled in the Citree database (TU Dresden)

* 1c_approved_street_trees: list of approved street trees for planting in New York City

### 1d_summary

* 1d_servicedtrees_data: list of trees damaged after severe weather events in NYC, including species, size, and location

---

## 2. Code

* **2a_[script_name]**: Description
* **2b_[script_name]**: Description
* **2c_[script_name]**: Description
* **2d_[script_name]**: Description
* **2e_[script_name]**: Description

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
│   ├── 1b_intermediate
│   ├── 1c_support
│   ├── 1d_summary
├── 02_code
│   ├── setup
│   ├── scripts
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
