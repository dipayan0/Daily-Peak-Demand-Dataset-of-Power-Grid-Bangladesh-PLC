# Daily-Peak-Demand-Dataset-of-Power-Grid-Bangladesh-PLC
Daily day and evening peak electricity demands time series compiled from PGCB monthly operational reports.

# Bangladesh National Grid Daily Peak Electricity Demand Dataset (2016–2024)

## Overview
This repository contains a curated time-series dataset of **daily peak electricity demand** for the **Bangladesh national power grid**, compiled from official monthly operational reports published by **Power Grid Bangladesh PLC (PGCB)**.

The dataset is intended to support **electricity demand forecasting**, **time-series analysis**, and **energy systems research**, particularly at the **national grid level**. It has been used to evaluate statistical, deep learning, and hybrid forecasting models in peer-reviewed research.

---

## Dataset Description

### File
Daily_Peak_Electricity_Demand_Bangladesh.csv

### Temporal Coverage
- **Start date:** 2016-01-01  
- **End date:** 2024-09-30  
- **Frequency:** Daily  
- **Timezone:** Bangladesh Standard Time (BST, UTC+6)

### Variables

| Column | Type | Unit | Description |
|------|------|------|-------------|
| `Date_(DD/MM/YYYY)` | string (ISO-8601) | — | Calendar date (`DD-MM-YYYY`) |
| `Day_Peak_Demand_MW` | numeric | MW | Daily maximum electricity demand during the day peak period |
| `Evening_Peak_Demand_MW` | numeric | MW | Daily maximum electricity demand during the evening peak period |

---

## Definition of Day Peak Demand
The **day peak demand** represents the **maximum system demand observed during the day peak hours** of each day, as reported in PGCB operational summaries.  
Values correspond to **system-level demand (generation end)** and are expressed in **megawatts (MW)**.


## Definition of Evening Peak Demand
The **evening peak demand** represents the **maximum system demand observed during the evening peak hours** of each day, as reported in PGCB operational summaries.  
Values correspond to **system-level demand (generation end)** and are expressed in **megawatts (MW)**.

---

## Data Source and Compilation Process
- Original data were obtained from **monthly operational spreadsheets** published on the official website of **Power Grid Bangladesh PLC (PGCB)**.
- Each monthly file contains daily records of day peak and evening peak demand.
- The published dataset was created by:
  1. Downloading monthly operational files
  2. Extracting daily day and evening peak demand values
  3. Merging all months into two continuous time series
  4. Standardizing date format to ISO-8601


---

## Data Quality Notes
- The dataset contains **3196 daily observations**.
- All values in `Evening_Peak_Demand_MW` are complete (no missing entries).
- Extreme values reflect real operational conditions (e.g., seasonal peaks, rapid demand growth).
- Users are encouraged to apply their own preprocessing (e.g., deseasonalization, normalization) depending on modeling requirements.

---

## Intended Use
This dataset is suitable for:
- Short-term and medium-term load forecasting
- Peak demand prediction
- Benchmarking forecasting algorithms
- Non-stationary time-series modeling
- Energy system planning and reliability studies

---

## Limitations
- The dataset does **not include exogenous variables** such as temperature, humidity, holidays, or economic indicators.
- It represents **aggregate national demand only**; regional or feeder-level analysis is not possible.
- Users should account for **structural changes** in demand due to policy, industrial growth, and electrification.

---

## Paper

The research work for which this dataset has been created and utilized is:

> https://doi.org/10.21203/rs.3.rs-8706187/v1

## Citation
If you use this dataset in academic work, please cite it as:

> Bhadra, D. (2026). *Bangladesh National Grid Daily Evening Peak Electricity Demand Dataset (2016–2024)*.

You can also cite the paper as:

> Dipayan Bhadra, Rumana Rois. CNN-ResLSTM-ConNet: A Novel Hybrid Deep Learning Model for Peak Electricity Demand Forecasting of National Grid, 27 January 2026, PREPRINT (Version 1) available at Research Square [https://doi.org/10.21203/rs.3.rs-8706187/v1]

A machine-readable citation is provided in `CITATION.cff`.

---

## License
This dataset is released under the **Creative Commons Zero v1.0 Universal (CC0 1.0)** license, unless otherwise stated.

---

## Acknowledgment
The authors acknowledge **Power Grid Bangladesh PLC (PGCB)** for making national grid operational data publicly available, which enabled the compilation of this dataset.

---

## Contact
For questions, corrections, or collaboration inquiries:

**Dipayan Bhadra**  
Email: dipu_dipayan@outlook.com
