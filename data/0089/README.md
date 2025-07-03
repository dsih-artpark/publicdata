# FMD - Nationwide Serosurveillance Data

:::{admonition} Disclaimer
:class: warning

This data is sourced from ICAR Annual Reports. The data represents state-level serosurveillance results for Foot and Mouth Disease (FMD) across India, with both combined bovine and species-specific (cattle, buffalo) results for some years.
:::

## About
This dataset contains state-level serosurveillance results for Foot and Mouth Disease (FMD) across India. The data covers multiple years, with both combined bovine and species-specific (cattle, buffalo) antibody prevalence, as well as the type of ELISA test used. It provides a view of FMD antibody prevalence and surveillance outcomes at the state level.

## Download

The file can be downloaded from github directly:

### Serosurveillance Data
- [Nationwide FMD Serosurveillance Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0089/serosurveillance.csv)

## Source
Data is sourced from ICAR Annual Reports. For 2022, cattle and buffalo are reported separately; for other years, results are combined as bovine.

## Data Dictionary

### Metadata Fields
| Column | Description | Example |
|--------|-------------|---------|
| metadata.diseaseName | WHO ICD-11 disease name | FOOT AND MOUTH DISEASE |
| metadata.year | Year reported | 2013 |
| metadata.lastVaccinationDate | Last date of vaccination in ISO 8601 format (if available) | 2022-06-30 |

### Location Fields
| Column | Description | Example |
|--------|-------------|---------|
| state.ID | State ID or Union Territory ID constructed from Local Government Directory in India | state_29 |
| state.name | State or Union Territory Name, as per Local Government Directory in India | Karnataka |

### Serosurveillance Fields
| Column | Description | Example |
|--------|-------------|---------|
| sero.sample | Number of bovine sampled (cattle + buffalo) | 2991.0 |
| sero.positive.pct | Percentage of bovine that tested positive | 21.1 |
| sero.test | Type of ELISA test | DIVA |
| sero.cattle.sample | Number of cattle sampled (2022 only) | 3729.0 |
| sero.cattle.positive.pct | Percentage of cattle that tested positive (2022 only) | 9.3 |
| sero.buffalo.sample | Number of buffalo sampled (2022 only) | 3911.0 |
| sero.buffalo.positive.pct | Percentage of buffalo that tested positive (2022 only) | 5.5 |

## Dataset Coverage
- **Geographic Coverage**: All states and union territories of India (state-level)
- **Temporal Coverage**: Multiple years (e.g., 2013–2022)
- **Species Coverage**: Bovine (cattle + buffalo), and for 2022, cattle and buffalo separately
- **Test Coverage**: ELISA test types (e.g., DIVA)

## Data Quality Notes
- 2022 data separates cattle and buffalo; other years report only combined bovine
- Some states may have missing years or incomplete data
- Data is aggregated at the state level (no district/village breakdown)
- Last vaccination date is only available for some records

## Comparison with Other Datasets
This serosurveillance dataset (0089) complements the vaccination and seromonitoring datasets:
- **0086**: Nationwide FMD vaccination counts and farmer beneficiaries (district-level)
- **0087**: Nationwide FMD seromonitoring results (state-level, antibody prevalence by serotype)
- **0089**: Nationwide FMD serosurveillance results (state-level, bovine/cattle/buffalo antibody prevalence)
- **0055/0059**: Karnataka-specific vaccination progress and scheduling 