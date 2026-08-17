# Analysis of Electric Vehicle Adoption in the UK

## MSc Data Science Dissertation Artefact

This repository contains the computational artefact developed for the MSc Data Science dissertation **"Analysis of Electric Vehicle Adoption in the UK"** at Coventry University.

The project investigates historical trends, regional differences and future patterns in electric vehicle (EV) adoption in the UK using official secondary datasets and quantitative analysis in Python.

The analytical workflow includes data collection, data cleaning, data integration, exploratory analysis, regional comparison, population-standardised analysis, charging infrastructure analysis and time-series forecasting.

---

## Research Aim

The aim of this research is to analyse the development of electric vehicle adoption in the UK using historical and regional data and to investigate potential future trends using time-series forecasting.

---

## Research Questions

The project addresses the following research questions:

1. How has electric vehicle adoption in the UK changed over time?
2. What regional differences exist in electric vehicle adoption across the UK?
3. What future trends in UK electric vehicle adoption can be identified using time-series forecasting?

---

## Research Objectives

The objectives of the project are:

- To analyse historical trends in UK electric vehicle registrations.
- To investigate regional differences in EV adoption.
- To examine EV adoption relative to population and charging infrastructure.
- To apply time-series forecasting to historical EV registration data.
- To provide evidence-based findings relevant to future EV infrastructure and policy planning.

---

## Data Sources

The research uses publicly available secondary datasets obtained from official UK government sources.

### Vehicle Registration Data

Electric vehicle registration data were obtained from the UK Department for Transport (DfT) and Driver and Vehicle Licensing Agency (DVLA) vehicle licensing statistics.

The main dataset used was **VEH0145**, containing licensed vehicle information by Lower Layer Super Output Area (LSOA), fuel type and keepership.

The data used in the project cover quarterly observations from **2011 Q4 to 2026 Q1**.

Source:  
https://www.gov.uk/government/statistical-data-sets/vehicle-licensing-statistics-data-tables

### Electric Vehicle Charging Infrastructure

Public electric vehicle charging-device statistics were obtained from the Department for Transport and Office for Zero Emission Vehicles (OZEV).

The data provide information on publicly available charging devices at local-authority level.

Source:  
https://www.gov.uk/government/collections/electric-vehicle-charging-infrastructure-statistics

### Population Data

Mid-2024 population estimates were obtained from the Office for National Statistics (ONS).

Population data were incorporated into the analysis to calculate population-standardised EV adoption indicators.

Source:  
https://www.ons.gov.uk/peoplepopulationandcommunity/populationandmigration/populationestimates

### Geographic Lookup Data

Official geographic lookup data were used to connect LSOA-level EV registration records with Local Authority Districts (LADs).

This enabled EV registrations to be aggregated and compared geographically.

---

## Repository Structure

The repository is organised as follows:

    UK-Electric-Vehicle-Adoption-Analysis/
    │
    ├── Python/
    │   ├── 01_Data_Collection.ipynb
    │   ├── 02_Data_Cleaning.ipynb
    │   ├── 03_Data_Integration.ipynb
    │   ├── 04_Exploratory_Analysis.ipynb
    │   ├── 05_Forecasting.ipynb
    │   └── 06_Final_Visualisations.ipynb
    │
    ├── Figures/
    │
    ├── Tables/
    │
    └── README.md

---

## Analytical Workflow

The project follows the analytical workflow below:

    Official UK Government Data
                ↓
          Data Collection
                ↓
           Data Cleaning
                ↓
          Data Integration
                ↓
       Exploratory Analysis
                ↓
        Regional Analysis
                ↓
    Population-Standardised Analysis
                ↓
    Charging Infrastructure Analysis
                ↓
       Time-Series Forecasting
                ↓
       Results and Evaluation

---

## Python Notebooks

### 01 - Data Collection

`Python/01_Data_Collection.ipynb`

This notebook imports and examines the datasets used in the project.

The initial assessment includes:

- dataset dimensions;
- column names;
- data types;
- quarterly coverage;
- missing-value checks;
- duplicate checks; and
- preliminary data-quality assessment.

---

### 02 - Data Cleaning

`Python/02_Data_Cleaning.ipynb`

This notebook prepares the datasets for subsequent analysis.

The principal data-cleaning procedures include:

- identification of disclosure-controlled entries;
- replacement of `[c]` and `[x]` entries with missing values;
- conversion of quarterly registration columns to numeric format;
- missing-value assessment;
- duplicate-record checks; and
- validation of the cleaned datasets.

Disclosure-controlled entries are treated as missing values rather than genuine vehicle-registration observations.

---

### 03 - Data Integration

`Python/03_Data_Integration.ipynb`

This notebook integrates the datasets required for geographical and population-standardised analysis.

EV registration records are linked with geographical lookup information using LSOA codes. Mid-2024 population estimates are subsequently integrated to support population-adjusted comparisons.

Validation checks are performed after merging to confirm record retention and identify missing geographical or population matches.

---

### 04 - Exploratory Analysis

`Python/04_Exploratory_Analysis.ipynb`

This notebook investigates historical and geographical patterns in UK EV adoption.

The analysis includes:

- quarterly EV registration trends;
- long-term changes in EV adoption;
- moving-average analysis;
- Local Authority District comparisons;
- population-standardised EV adoption measures; and
- comparison of EV adoption with charging infrastructure.

---

### 05 - Forecasting

`Python/05_Forecasting.ipynb`

This notebook contains the time-series forecasting component of the research.

An ARIMA-based approach is applied to quarterly EV registration data. The historical series is divided into training and testing periods to evaluate forecasting performance before producing future estimates.

The analysis includes:

- time-series preparation;
- Augmented Dickey-Fuller testing;
- ARIMA model fitting;
- forecast-versus-actual comparison;
- Mean Absolute Error (MAE);
- Root Mean Squared Error (RMSE);
- Mean Absolute Percentage Error (MAPE); and
- residual diagnostic analysis.

---

### 06 - Final Visualisations

`Python/06_Final_Visualisations.ipynb`

This notebook produces the final visualisations used to communicate the principal findings of the research.

The visualisations include historical EV trends, regional comparisons, population-standardised indicators, charging infrastructure comparisons and forecasting results.

---

## Methods

The study follows a **quantitative secondary-data research design**.

The main analytical components are:

### Historical Trend Analysis

Quarterly EV registration data from 2011 Q4 to 2026 Q1 are analysed to examine the development of EV adoption over time.

### Regional Analysis

EV registrations are aggregated geographically to investigate differences between Local Authority Districts.

### Population-Standardised Analysis

Population estimates are incorporated to account for differences in population size when comparing EV adoption between geographical areas.

### Charging Infrastructure Analysis

Public charging-device statistics are examined alongside EV adoption patterns to provide additional context regarding regional charging provision.

### Time-Series Forecasting

ARIMA modelling is applied to the historical quarterly EV registration series to evaluate temporal patterns and investigate possible future trends.

---

## Software

The analysis was conducted using **Python** within **Jupyter Notebook**.

The principal Python packages used for data processing, statistical analysis and visualisation include:

- pandas
- NumPy
- Matplotlib
- statsmodels

---

## Reproducibility

The notebooks are numbered according to the sequence of the analytical workflow and should be reviewed in the following order:

1. `01_Data_Collection.ipynb`
2. `02_Data_Cleaning.ipynb`
3. `03_Data_Integration.ipynb`
4. `04_Exploratory_Analysis.ipynb`
5. `05_Forecasting.ipynb`
6. `06_Final_Visualisations.ipynb`

The original datasets are **not stored in this repository**. They can be obtained from the official UK government sources listed in the **Data Sources** section above.

The notebooks document the data-processing and analytical procedures used to transform the original datasets and produce the results reported in the dissertation.

Because the datasets are not included in the repository, the appropriate source files must be downloaded and placed in the required local data directories before reproducing the complete workflow.

---

## Repository Outputs

### Figures

The `Figures` directory contains visual outputs generated during the analysis and used to support the interpretation of the results.

### Tables

The `Tables` directory contains tabular outputs generated from the analytical stages of the project.

---

## Data and Research Ethics

This research uses publicly available secondary datasets from official UK government sources.

No primary data were collected, no research participants were recruited, and no personally identifiable participant information was collected as part of this study.

The project was undertaken as part of the MSc Data Science Individual Research Project at Coventry University.

---

## Author

**Aditya Kumar**  
MSc Data Science  
Coventry University  

Student ID: **16448702**

---

## Academic Project

This repository is the computational artefact accompanying the MSc Data Science dissertation:

**Analysis of Electric Vehicle Adoption in the UK**

It contains the Python notebooks and analytical outputs supporting the data preparation, analysis, forecasting and results presented in the dissertation.

The repository is maintained for academic assessment and reproducibility of the computational work.
