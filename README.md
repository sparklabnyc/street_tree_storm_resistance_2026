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

1. 2025-2026 New York City Tree Census Map Data
* The NYC Parks Department uses a combination of volunteer efforts and LiDAR/machine learning technology to collect data on the species, size, location, and ecological benefits of street and park trees in New York City.
* [NYC Tree Map] (https://tree-map.nycgovparks.org/)

2. NYC Parks Department Forestry Service Requests
* Dataset of tree-related service requests submitted through 311 or Parks website. This dataset provides

3. NYC Storm History Data
* The NYC Hazard History and Consequence Tool, developed by NYC Emergency Management as part of the NYC Hazard Mitigation Plan, compiles hazard events in NYC. Filtered down to the hazards of flash flooding, coastal flooding, heavy snow, and high winds, this database will provide temporal information of storm events (e.g. heavy rainstorms, tropical cyclones, hurricanes, blizzards) in NYC that can cause damage to trees. 

### 1b_intermediate

1. Filtered/cleaned Service Request Data
* filter to SRCategory = Hazards, then clean SRType to the larger categories of Limb Down, Hanging Limb, Tree Down, and Tree Leaning

2. Temporal Service Request Data
* Further filter SR Data to requests made within 24 hours of a major storm event from 2016 to 2026, as compiled in 1a4

3. Service requests & species
* Join 1b2 with 1a1 (NYC Tree Map) using the closest address as key --> get full dataframe of trees with storm damage and their species

### 1c_support

Supporting files:

* Boundaries, lookup tables, definitions, etc.

### 1d_summary

* processed list of trees damaged by storms from 2015 to 2025, with information about species, size, and location (coordinates and closest address)

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
Barnard College, Department of Biological Sciences & Columbia University Mailman School of Public Health, Department of Environmental Health Sciences
