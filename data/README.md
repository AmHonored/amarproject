# Dataset Documentation (NHANES 2021-2023)

## 1. Data Origin & Collection Mechanism
The data for this project is extracted from the National Health and Nutrition Examination Survey (NHANES) for the August 2021 – August 2023 cycle. This survey is conducted by the National Center for Health Statistics (NCHS/CDC).

The dataset represents an **observational, cross-sectional study**, meaning no randomized interventions or experiments were performed on the participants. Data was collected through two primary phases:
-   **Home Interviews:** For demographic information, sleep patterns, and physical activity questionnaires.
-   **Mobile Examination Centers (MEC):** For precise physical and physiological measurements (e.g., height, weight, and BMI calculations).

## 2. Unit of Observation & Data Structure
The unit of observation in this dataset is a **single independent individual (one row per person)**. The data does not have a hierarchical or repeated-measures structure (each participant is examined only once). 

The various component files (demographics, examinations, and questionnaires) all share a unique sequence number (`SEQN`). This identifier is used to perform a one-to-one merge, consolidating a single participant's information across multiple files into a unified analytical dataset.

## 3. Sampling, Selection & Generalizability
Participants were not selected via simple random sampling. NHANES utilizes a **complex, multistage probability sampling** design to ensure the final sample accurately represents the civilian, non-institutionalized US population. 

Because this is an observational study, we can generalize the correlations and statistical findings to the broader adult population (by rigorously applying survey weights), but we **cannot** use this data to definitively prove causal relationships.

## 4. Instructions to Download Data
Download the following `.XPT` files from the [CDC NHANES 2021-2023 Portal](https://wwwn.cdc.gov/nchs/nhanes/continuousnhanes/default.aspx?Cycle=2021-2023) and place them in this folder.

- `DEMO_L.xpt` (Demographics)
- `BMX_L.xpt` (Body Measures)
- `SLQ_L.xpt` (Sleep Disorders)
- `PAQ_L.xpt` (Physical Activity)