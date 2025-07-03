# FMD - Nationwide Vaccination Data (Rounds 1-6)

:::{admonition} Disclaimer
:class: warning

This data is sourced from the National Digital Livestock Mission (NDLM) website. The data represents nationwide vaccination statistics for Foot and Mouth Disease (FMD) across all states and union territories of India.
:::

## About
This dataset contains nationwide vaccination statistics for Foot and Mouth Disease (FMD) across all states and union territories of India. The data covers vaccination rounds 1-6 with district-level aggregation including total vaccination counts and farmer beneficiary statistics. This dataset provides a comprehensive view of FMD vaccination coverage across the entire country.

## Download

The file can be downloaded from github directly:

### Vaccination Data
- [Nationwide FMD Vaccination Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0086/fmd_vaccinations.csv)

## Source
Data is sourced from the National Digital Livestock Mission (NDLM) website. The time period for the data is unclear from the source.

## Data Dictionary

### Metadata Fields
| Column | Description | Example |
|--------|-------------|---------|
| metadata.vaccinationRound | Vaccination round number | 1 |

### Location Fields
| Column | Description | Example |
|--------|-------------|---------|
| state.ID | State ID or Union Territory ID constructed from Local Government Directory in India | ut_35 |
| state.name | State or Union Territory Name, as per Local Government Directory in India | Andaman And Nicobar Islands |
| district.ID | District ID constructed from Local Government Directory in India | district_602 |
| district.name | District Name, as per Local Government Directory in India | South Andamans |

### Vaccination Statistics Fields
| Column | Description | Example |
|--------|-------------|---------|
| totalVaccinations.count | Total number of vaccinations done in the district for the round | 8312 |
| farmersBenefited.count | Number of farmers benefitted from vaccinations in the district for the round | 2016 |

## Dataset Coverage
- **Geographic Coverage**: All states and union territories of India
- **Administrative Level**: District-level aggregation
- **Temporal Coverage**: Vaccination rounds 1-6
- **Program Focus**: Foot and Mouth Disease vaccination under national programs

## Data Quality Notes
- All location IDs follow the Local Government Directory (LGD) standards
- Vaccination counts represent total vaccinations completed per district per round
- Farmer beneficiary counts represent unique farmers who received vaccinations
- Data is aggregated at district level (no village/subdistrict breakdown)
- Data covers all states and union territories including smaller territories like Andaman & Nicobar Islands

## Comparison with Other Datasets
This nationwide dataset (0086) differs from the Karnataka-specific datasets:
- **0086**: Nationwide coverage across all states and UTs
- **0055**: Detailed daily progress for Karnataka only
- **0059**: Village-level scheduling for Karnataka only
- **0086**: District-level aggregation with focus on total coverage and farmer benefits 