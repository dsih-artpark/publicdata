# FMD - NADCP Vaccination Schedule Data (Rounds 3-6)

:::{admonition} Disclaimer
:class: warning

This data is sourced from the Karnataka Animal Husbandry and Veterinary Services Department. The data represents village-level vaccination schedules for the National Animal Disease Control Programme (NADCP) against Foot and Mouth Disease.
:::

## About
This dataset contains village-level vaccination schedules for the National Animal Disease Control Programme (NADCP) against Foot and Mouth Disease in Karnataka. The data covers vaccination rounds 3-6 with detailed scheduling information including planned vaccination dates, target animal counts, and administrative hierarchy from state down to village level.

## Download

The files can be downloaded from github directly:

### Vaccination Schedule Data
- [Round 3 Schedule](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0059/round3.csv)
- [Round 4 Schedule](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0059/round4.csv)
- [Round 5 Schedule](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0059/round5.csv)
- [Round 6 Schedule](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0059/round6.csv)

## Source
Data is primarily sourced from the Karnataka Animal Husbandry and Veterinary Services Department: [Link](https://ahvs.karnataka.gov.in/info-2/NADCP)

## Data Dictionary

### Metadata Fields
| Column | Description | Example |
|--------|-------------|---------|
| metadata.recordID | Universally Unique Identifier (UUID) for each record, generated using uuid4 from python3 | 7b82c5ae-14cf-40e9-9796-a8e80dcf0b84 |
| metadata.diseaseName | WHO ICD-11 Disease Name | Foot And Mouth Disease |
| metadata.diseaseCode | WHO ICD-11 Disease Code | ICD11_1F05 |
| metadata.round | NADCP Vaccination Schedule Round | 3 |
| metadata.vaccinationSchedule | Date on which vaccinations are scheduled in ISO 8601 format | 2022-07-11T00:00:00Z |
| metadata.vaccinationSchedule.endDate | End date of vaccination schedule in ISO 8601 format (optional) | 2022-07-15T00:00:00Z |

### Location Fields
| Column | Description | Example |
|--------|-------------|---------|
| country.ID | Country ID constructed using ISO 3166 alpha-2 code | country_IN |
| country.name | Country name from ISO 3166 | India |
| location.admin.hierarchy | Administrative hierarchy for the record - Revenue (if sub-district), ULB (if urban local body) or admin_0 (if unknown) | Revenue |
| state.ID | State ID or Union Territory ID constructed from Local Government Directory in India | state_29 |
| state.name | State or Union Territory Name, as per Local Government Directory in India | Karnataka |
| district.ID | District ID constructed from Local Government Directory in India | district_540 |
| district.name | District Name, as per Local Government Directory | Haveri |
| subdistrict.ID | Subdistrict/ULB ID constructed from Local Government Directory in India | subdistrict_5489 |
| subdistrict.name | Subdistrict/ULB Name, as per Local Government Directory | Shiggaon |
| location.admin4.name | Zone Name (if Urban Local Body) or Hobli name, provided by the ULB/State | Shiggaon Tmc |
| village.ID | Village/ward ID constructed from Local Government Directory in India | admin_0 |
| village.name | Village/ward Name, as per Local Government Directory | Shiggaon Tmc |

### Scheduled Vaccination Fields
| Column | Description | Example |
|--------|-------------|---------|
| daily.vaccinated.cattle | Number of cattle scheduled to be vaccinated on the scheduled dates | 150 |
| daily.vaccinated.buffalo | Number of buffalo scheduled to be vaccinated on the scheduled dates | 75 |
| daily.vaccinated.total | Total number of animals scheduled to be vaccinated on the scheduled dates | 225 |

## Dataset Coverage
- **Geographic Coverage**: All districts of Karnataka state with village-level granularity
- **Temporal Coverage**: Vaccination rounds 3-6 with scheduled dates
- **Administrative Hierarchy**: State → District → Subdistrict → Village/Ward level
- **Program Focus**: Foot and Mouth Disease vaccination scheduling under NADCP

## Data Quality Notes
- All location IDs follow the Local Government Directory (LGD) standards
- Scheduled vaccination counts represent planned targets, not actual vaccinations
- Some records may have missing location information (marked as admin_0)
- Multiple scheduled dates for the same location are split into separate rows
- Scheduled counts may not match actual vaccination report numbers

## Relationship to Other Datasets
This vaccination schedule dataset (0059) complements the vaccination progress dataset (0055):
- **0055**: Actual vaccination progress reports with daily counts
- **0059**: Planned vaccination schedules with target dates and numbers
- Together they enable comparison of planned vs. actual vaccination coverage 