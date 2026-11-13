# NCHS Leading Causes of Death Analysis (1999–2017)

## Overview
This project explores U.S. mortality data from the National Center for Health Statistics (NCHS) covering the years **1999 to 2017**. The analysis specifically isolates and examines trends for **Cancer** (`Malignant neoplasms`) and **Influenza and pneumonia**.

## Folder Structure
* `sql_queries/` – Contains the SQLite queries used to filter and extract the 1,976 target records from the full dataset.
* `results/` – Contains the exported CSV output summarising annual total deaths and average age-adjusted mortality rates for Cancer and Influenza/pneumonia (1999–2017),
  the packaged Tableau workbook (`.twbx`),
  and the exported PNG image of the dual-axis trend chart.
  
## Tools Used
* **DB Browser for SQLite** (Data querying and filtering)
* **Microsoft Excel** (Initial data validation and row verification)
* **Tableau** (Data Visualisaton)

## Data Source & Reproducibility
* **Original Dataset:** [(https://www.kaggle.com/datasets/cdc/nchs-death-rates-and-causes-of-death/data)].
* **SQLite Table Name:** `nchs_leading_causes_of_death_united_states`
* **How to Reproduce:** Download the CSV from the CDC link above, import it into SQLite using the exact table name listed, and run the `.sql` script located in `sql_queries/`.

## Findings
### Research Question
How did age-adjusted death rates for influenza/pneumonia and cancer change in the United States from 1999 to 2017, and what factors might explain the difference in their trends?

### Interactive Visualisation 
(https://public.tableau.com/views/U_S_Age-AdjustedDeathRatesInfluenzaPneumoniavs_Cancer19992017/U_S_DeathRatesFluPneumoniavs_Cancer19992017?:language=en-GB&publish=yes&:sid=&:redirect=auth&:display_count=n&:origin=viz_share_link)

### Observations
**Cancer:** Total deaths rose consistently from 1,099,676 (1999) to 1,198,216 (2017) - a 9% increase over 18 years. Yet the age-adjusted death rate fell from 201.45 to 154.96 per 100,000 - a 23% decline. This inverse movement reflects demographic shifts outpacing risk reduction: the population aged and grew, so absolute deaths rose, even as the standardized risk per person improved significantly.

**Influenza & Pneumonia:** Total deaths fluctuated between 100,194 (2010, lowest) and 131,362 (2002, highest), reflecting seasonal and epidemic variation year to year. The age-adjusted rate trended downward from 24.28 (1999) to 14.89 (2017) per 100,000 - a 39% decline - demonstrating a sustained drop in baseline mortality risk despite annual seasonal spikes.

### Why this pattern is possible
Age-adjusted rates account for population structure; total deaths do not. The U.S. population grew by roughly 50 million people and aged significantly between 1999 and 2017. More older people means more total deaths from age-related causes - cancer especially - even when medical progress reduces the risk for any given person. For cancer, better screening (earlier detection), improved treatments, and lifestyle factors pushed the age-adjusted rate down despite rising absolute numbers. For flu and pneumonia, the age-adjusted decline reflects public health gains (vaccination, antivirals, infection control), while year-to-year swings in total deaths track flu season severity and pandemic years.

### Recommendations
* Plan capacity using both metrics. Total deaths indicate the demand on hospital beds and staff. Age-adjusted rates indicate how well treatment is working. Cancer's rising counts suggest oncology and geriatric capacity will need to grow even as individual risk falls.
* Target flu vaccination at high-risk groups. Older adults carry most of the flu and pneumonia death burden, so vaccination outreach should prioritise them. The data cannot confirm this will flatten seasonal peaks.



