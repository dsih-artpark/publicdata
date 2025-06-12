# Karnataka Dengue Daily Summary Data (2017-2024)

:::{admonition} Disclaimer
:class: warning

Some of this data is sourced from the Commissionerate of Health and Family Welfare Services, Government of Karnataka, and some of it is sourced from the Karnataka State Health Department. Discrepancies in the data are expected.
:::

:::{admonition} Data Updation
:class: info

This data is currently only available for the years 2017-2024. Daily updates are expected to be available for the years 2025 and onwards by June 25th.
:::

## About
This dataset contains day-wise summaries of dengue tests, suspected cases, confirmed cases and deaths by district in Karnataka. 

## Download

The file can be downloaded from github directly here: [Link](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0015/ka-dengue-daily-summary.csv).

## Source
Data is primarily sourced from the Commissionerate of Health and Family Welfare Services, Government of Karnataka: [Link](https://hfwcom.karnataka.gov.in/info-4/Dengue+&+Chikungunya+-+-Malaria+&+H1N1-Reports/en). 

## Data Dictionary

### Metadata Fields
| Column | Description | Example |
|--------|-------------|---------|
| metadata.recordID | Universally Unique Identifier (UUID) for each district, generated using uuid4 from python3 | cc36713a-b762-40ae-8c18-ce9f600d062f |
| metadata.recordDate | Date of daily summary report. Compliant with ISO 8601 format (YYYY-MM-DD or %Y-%m-%d on python3) | 2022-04-18T00:00:00Z |
| metadata.ISOWeek | ISO week generated from the recordDate | 16 |
| metadata.diseaseName | WHO ICD-11 Disease Name | DENGUE |
| metadata.diseaseCode | WHO ICD-11 Disease Code | ICD11_1D2Z |

### Location Fields
| Column | Description | Example |
|--------|-------------|---------|
| location.country.ID | Country ID constructed using ISO 3166 alpha-2 code. e.g. country_IN for India | country_IN |
| location.country.name | Country name from ISO 3166 | INDIA |
| location.admin.hierarchy | Administrative hierarchy for the record - Revenue (if sub-district), ULB (if urban local body) or admin_0 (if unknown) | REVENUE |
| location.admin1.ID | State ID or Union Territory ID constructed from Local Government Directory in India. Unique across the country. | state_29 |
| location.admin1.name | State or Union Territory Name, as per Local Government Directory in India | KARNATAKA |
| location.admin2.ID | District ID constructed from Local Government Directory in India. Unique across the country. | district_525 |
| location.admin2.name | District Name, as per Local Government Directory | BENGALURU URBAN |
| location.admin3.ID | Subdistrict or ULB ID, constructed from Local Government Directory in India. Unique across the country. | ulb_276600 |
| location.admin3.name | Subdistrict or ULB Name, as per Local Government Directory | BBMP |

### Daily Statistics Fields
| Column | Description | Example |
|--------|-------------|---------|
| daily.suspected | Number of suspected cases, reported on the day | 168.0 |
| daily.tested | Number of tests conducted, reported on the day | 78 |
| daily.positive.igm | Number of IgM tests positive, reported on the day | 10.0 |
| daily.positive.ns1 | Number of NS1 tests positive, reported on the day | 0.0 |
| daily.positive.other | Number of other tests positive, reported on the day | 0.0 |
| daily.positive.total | Total tests positive, reported on the day | 10.0 |
| daily.deaths | Number of deaths, reported on the day | 0.0 |

### Cumulative Statistics Fields
| Column | Description | Example |
|--------|-------------|---------|
| cumulative.suspected | Cumulative number of suspected cases, reported as of the day | 168 |
| cumulative.tested | Cumulative number of tests conducted, reported as of the day | 78.0 |
| cumulative.positive.igm | Cumulative number of positive IgM tests, reported as of the day | 10 |
| cumulative.positive.ns1 | Cumulative number of positive NS1 tests, reported as of the day | 0 |
| cumulative.positive.other | Cumulative number of other tests positive, reported as of the day | 0 |
| cumulative.positive.total | Cumulative number of positives from all tests, reported as of the day | 10 |
| cumulative.deaths | Cumulative number of deaths, reported as of the day | 0 |

