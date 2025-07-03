 # FMD - Nationwide Seromonitoring Data

:::{admonition} Disclaimer
:class: warning

This data is sourced from ICAR Annual Reports. The data represents state-level seromonitoring results for Foot and Mouth Disease (FMD) vaccination programs (FMDCP and NADCP) across India.
:::

## About
This dataset contains state-level seromonitoring results for Foot and Mouth Disease (FMD) vaccination programs (FMDCP and NADCP) across India. The data covers multiple years, rounds, and both pre- and post-vaccination antibody prevalence for three FMD virus types (O, A, Asia1). It provides a view of the effectiveness of FMD vaccination programs at the state level.

## Download

The file can be downloaded from github directly:

### Seromonitoring Data
- [Nationwide FMD Seromonitoring Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0087/seromonitoring.csv)

## Source
Data is sourced from ICAR Annual Reports. State-level data is compiled from annual reports; round numbering and years may not be fully consistent across states.

## Data Dictionary

### Metadata Fields
| Column | Description | Example |
|--------|-------------|---------|
| metadata.year | Year reported | 2011 |
| metadata.diseaseName | WHO ICD-11 disease name | FOOT AND MOUTH DISEASE |
| metadata.round | Round number of the program | 12.0 |
| metadata.program | Vaccination Program name (FMDCP or NADCP) | FMDCP |

### Location Fields
| Column | Description | Example |
|--------|-------------|---------|
| state.ID | State ID or Union Territory ID constructed from Local Government Directory in India | state_27 |
| state.name | State or Union Territory Name, as per Local Government Directory in India | Maharashtra |

### Seromonitoring Fields
| Column | Description | Example |
|--------|-------------|---------|
| prevac.sample | Number of samples tested pre-vaccination | 5988.0 |
| prevac.positive.O.pct | % of pre-vaccination samples with antibodies against O-type virus | 28.2 |
| prevac.positive.A.pct | % of pre-vaccination samples with antibodies against A-type virus | 15.7 |
| prevac.positive.asia1.pct | % of pre-vaccination samples with antibodies against Asia1-type virus | 6.4 |
| postvac.sample | Number of samples tested post-vaccination | 6018.0 |
| postvac.positive.O.pct | % of post-vaccination samples with antibodies against O-type virus | 72.9 |
| postvac.positive.A.pct | % of post-vaccination samples with antibodies against A-type virus | 51.2 |
| postvac.positive.asia1.pct | % of post-vaccination samples with antibodies against Asia1-type virus | 38.4 |

## Dataset Coverage
- **Geographic Coverage**: All states and union territories of India (state-level)
- **Temporal Coverage**: Multiple years (e.g., 2011–2022)
- **Program Coverage**: Both FMDCP and NADCP vaccination programs
- **Serotype Coverage**: O, A, and Asia1 FMD virus types

## Data Quality Notes
- State and round numbering may not be fully consistent across years and programs
- Some states may have missing years or rounds
- Pre- and post-vaccination sample sizes may differ
- Percentages are calculated as (positive count/sample size) * 100
- Data is aggregated at the state level (no district/village breakdown)

## Comparison with Other Datasets
This seromonitoring dataset (0087) complements the vaccination datasets:
- **0086**: Nationwide FMD vaccination counts and farmer beneficiaries (district-level)
- **0087**: Nationwide FMD seromonitoring results (state-level, antibody prevalence)
- **0055/0059**: Karnataka-specific vaccination progress and scheduling
- **0087**: Focuses on immunological outcomes, not just vaccination counts
