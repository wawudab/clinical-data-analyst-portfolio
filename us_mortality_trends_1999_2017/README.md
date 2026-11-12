# NCHS Leading Causes of Death Analysis (1999–2017)

## Overview
This project explores U.S. mortality data from the National Center for Health Statistics (NCHS) covering the years **1999 to 2017**. The analysis specifically isolates and examines trends for **Cancer** (`Malignant neoplasms`) and **Influenza and pneumonia**.

## Folder Structure
* `sql_queries/` – Contains the SQLite queries used to filter and extract the 1,976 target records from the full dataset.
* `results/` – Contains the exported CSV output summarising annual total deaths and average age-adjusted mortality rates for Cancer and Influenza/pneumonia (1999–2017).

## Tools Used
* **DB Browser for SQLite** (Data querying and filtering)
* **Microsoft Excel** (Initial data validation and row verification)

## Data Source & Reproducibility
* **Original Dataset:** [(https://www.kaggle.com/datasets/cdc/nchs-death-rates-and-causes-of-death/data)].
* **SQLite Table Name:** `nchs_leading_causes_of_death_united_states`
* **How to Reproduce:** Download the CSV from the CDC link above, import it into SQLite using the exact table name listed, and run the `.sql` script located in `sql_queries/`.

