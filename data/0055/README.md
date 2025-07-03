# FMD - NADCP Vaccination Progress Data (Rounds 1-6)

:::{admonition} Disclaimer
:class: warning

This data is sourced from the Karnataka Animal Husbandry and Veterinary Services Department. The data represents district-level vaccination and tagging progress reports for the National Animal Disease Control Programme (NADCP) against Foot and Mouth Disease.
:::

## About
This dataset contains district-level vaccination and tagging progress reports for the National Animal Disease Control Programme (NADCP) against Foot and Mouth Disease in Karnataka. The data covers multiple vaccination rounds (1-6) with daily progress tracking including cattle and buffalo vaccination counts, calf vaccination details, booster doses, and farmer coverage statistics.

## Download

The files can be downloaded from github directly:

### Vaccination Round Data
- [Round 1 Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0055/round1.csv)
- [Round 2 Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0055/round2.csv)
- [Round 3 Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0055/round3.csv)
- [Round 4 Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0055/round4.csv)
- [Round 5 Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0055/round5.csv)
- [Round 6 Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0055/round6.csv)

## Source
Data is primarily sourced from the Karnataka Animal Husbandry and Veterinary Services Department: [Link](https://ahvs.karnataka.gov.in/info-2/NADCP)

## Data Dictionary

### Metadata Fields
| Column | Description | Example |
|--------|-------------|---------|
| metadata.recordID | Universally Unique Identifier (UUID) for each record, generated using uuid4 from python3 | 66764cea-448d-41ae-838d-4f97d60eb193 |
| metadata.diseaseName | WHO ICD-11 Disease Name | Foot And Mouth Disease |
| metadata.diseaseCode | WHO ICD-11 Disease Code | ICD11_1F05 |
| metadata.round | NADCP Vaccination Round | round1 |
| metadata.vaccinationStartDate | Start date for the Vaccination Round in ISO 8601 format | 2020-10-01T00:00:00 |
| metadata.reportDate | Date of the Daily Progress Report in ISO 8601 format | 2020-10-03T00:00:00 |

### Location Fields
| Column | Description | Example |
|--------|-------------|---------|
| country.ID | Country ID constructed using ISO 3166 alpha-2 code | country_IN |
| country.name | Country name from ISO 3166 | India |
| state.ID | State ID or Union Territory ID constructed from Local Government Directory in India | state_29 |
| state.name | State or Union Territory Name, as per Local Government Directory in India | Karnataka |
| district.ID | District ID constructed from Local Government Directory in India | district_524 |
| district.name | District Name, as per Local Government Directory | Bagalkote |

### Daily Vaccination Fields
| Column | Description | Example |
|--------|-------------|---------|
| daily.vaccinated.cattle | Number of Cattle vaccinated on the day | 690.0 |
| daily.vaccinated.buffalo | Number of Buffaloes vaccinated on the day | 390.0 |
| daily.vaccinated.total | Sum of Cattle and Buffaloes vaccinated on the day (computed) | 1080.0 |
| daily.vaccinated.cattle4to5m | Number of Cattle calves (aged 4-5 months) vaccinated on the day | 20.0 |
| daily.vaccinated.buffalo4to5m | Number of Buffalo calves (aged 4-5 months) vaccinated on the day | 30.0 |
| daily.vaccinated.total4to5m | Sum of Cattle and Buffalo calves (aged 4-5 months) vaccinated on the day (computed) | 50.0 |

### Daily Booster Fields
| Column | Description | Example |
|--------|-------------|---------|
| daily.booster.cattle4to5m | Number of Cattle calves (aged 4-5 months) provided booster dose on the day | 0.0 |
| daily.booster.buffalo4to5m | Number of Buffalo calves (aged 4-5 months) provided booster dose on the day | 0.0 |
| daily.booster.total4to5m | Sum of Cattle and Buffalo calves (aged 4-5 months) provided booster dose on the day (computed) | 0.0 |

### Daily Coverage Fields
| Column | Description | Example |
|--------|-------------|---------|
| daily.farmersCovered | Number of farmers benefited on the day | 730.0 |

### Cumulative Tagging Fields
| Column | Description | Example |
|--------|-------------|---------|
| cumulative.tagged.cattle | Cumulative number of Cattle tagged as of the day | 12345 |
| cumulative.tagged.buffalo | Cumulative number of Buffaloes tagged as of the day | 6789 |
| cumulative.tagged.total | Cumulative number of Cattle and Buffaloes tagged as of the day (from source) | 19134 |

## Dataset Coverage
- **Geographic Coverage**: All districts of Karnataka state
- **Temporal Coverage**: Multiple vaccination rounds (1-6) with daily progress tracking
- **Animal Categories**: Cattle and Buffalo (adults and calves aged 4-5 months)
- **Program Focus**: Foot and Mouth Disease vaccination under NADCP

## Data Quality Notes
- All location IDs follow the Local Government Directory (LGD) standards
- Vaccination counts represent actual numbers from daily progress reports
- Some records may have missing data for certain fields