# 20th Livestock Census Data (2019)

:::{admonition} Disclaimer
:class: warning

This data is sourced from various state government departments and the Department of Animal Husbandry and Dairying, Government of India. The data represents the 20th Livestock Census conducted in 2019.
:::

## About
This dataset contains comprehensive livestock and poultry population data from the 20th Livestock Census (2019) conducted across India. The data includes district-level, village-level, and state-level statistics for various livestock categories including cattle, buffalo, sheep, goat, pig, and poultry.

## Download

The files can be downloaded from github directly:

### Main Dataset Files
- [All India Livestock Census Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/all-india-20th-livestock-census.csv)
- [Karnataka District Level Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/ka-district-livestock-pop-2019.csv)
- [Karnataka Village Level Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/ka-village-livestock-pop-2019.csv)
- [Maharashtra District Level Data](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/mh-district-livestock-poultry-pop-2019.csv)

### State Level Summary Files
- [State-wise Bovine Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_bovine.csv)
- [State-wise Buffalo Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_buffalo.csv)
- [State-wise Cattle (Exotic/Crossbred) Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_cattle_exotic_crossbred.csv)
- [State-wise Cattle (Indigenous) Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_cattle_indigenous_non_descript.csv)
- [State-wise Goat Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_goat.csv)
- [State-wise Pig (Exotic/Crossbred) Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_pig_exotic_crossbred.csv)
- [State-wise Pig (Indigenous) Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_pig_indigenous.csv)
- [State-wise Sheep (Exotic/Crossbred) Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_sheep_exotic_crossbred.csv)
- [State-wise Sheep (Indigenous) Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_sheep_indigenous.csv)
- [State-wise Stray Animals Details](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/statewise_details_of_stray_animals.csv)
- [Total Livestock and Poultry Summary](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0041/state_level_data/total_number_of_livestock_and_poultry.csv)

## Source
Data is primarily sourced from:
- Department of Animal Husbandry and Dairying, Government of India: [Link](https://dahd.gov.in/taxonomy/term/410)
- Karnataka Animal Husbandry and Veterinary Services: [Link](https://www.ahvs.kar.nic.in/en-reportsstat.html)
- Pune Knowledge Cluster (PKC) for Maharashtra data

## Data Dictionary

### Common Metadata Fields
| Column | Description | Example |
|--------|-------------|---------|
| metadata.recordID | Universally Unique Identifier (UUID) for each record, generated using uuid4 from python3 | 8ecd56d3-dc48-48b3-8f3c-0456ea758df3 |
| country.ID | Country ID constructed using ISO 3166 alpha-2 code | country_IN |
| country.name | Country name from ISO 3166 | INDIA |
| location.admin.hierarchy | Administrative hierarchy for the record - Revenue (if sub-district), ULB (if urban local body) or admin_0 (if unknown) | REVENUE |

### Location Fields
| Column | Description | Example |
|--------|-------------|---------|
| state.ID | State ID or Union Territory ID constructed from Local Government Directory in India | state_29 |
| state.name | State or Union Territory Name, as per Local Government Directory in India | KARNATAKA |
| district.ID | District ID constructed from Local Government Directory in India | district_524 |
| district.name | District Name, as per Local Government Directory | BAGALKOTE |
| subdistrict.ID | Subdistrict or ULB ID, constructed from Local Government Directory in India | subdistrict_5587 |
| subdistrict.name | Subdistrict or ULB Name, as per Local Government Directory | BBMP |
| village.ID | Village (for Revenue) or Ward ID (for ULB), constructed from Local Government Directory | village_12345 |
| village.name | Village or Ward Name, as per Local Government Directory | Example Village |
| block.name | Block/Tehsil Name as given in the raw dataset | Example Block |
| town.name | Town Name as given in the raw dataset | Example Town |
| ward.name | Ward Name as given in the raw dataset | Example Ward |
| location.type | Type of location (Rural/Urban) | RURAL |

### Livestock Population Fields
| Column | Description | Example |
|--------|-------------|---------|
| population.cattle | Total cattle population | 222823 |
| population.buffalo | Total buffalo population | 234340 |
| population.sheep | Total sheep population | 622856 |
| population.goat | Total goat population | 383926 |
| population.pig | Total pig population | 20458 |
| population.poultry | Total poultry population | 1703285 |

### Gender-specific Population Fields (All India Data)
| Column | Description | Example |
|--------|-------------|---------|
| population.cattle.male | Male cattle population | 12345 |
| population.cattle.female | Female cattle population | 23456 |
| population.buffalo.male | Male buffalo population | 12345 |
| population.buffalo.female | Female buffalo population | 23456 |
| population.sheep.male | Male sheep population | 12345 |
| population.sheep.female | Female sheep population | 23456 |
| population.goat.male | Male goat population | 12345 |
| population.goat.female | Female goat population | 23456 |
| population.pig.male | Male pig population | 12345 |
| population.pig.female | Female pig population | 23456 |

### Poultry-specific Fields (Maharashtra Data)
| Column | Description | Example |
|--------|-------------|---------|
| metadata.category | Whether Commercial or Backyard | Commercial |
| metadata.type | Whether Indigenous, Improved or Other | Indigenous |
| population.cocks | Cocks population | 12345 |
| population.hens | Hens population | 23456 |
| population.chickens | Chickens population | 34567 |
| population.drakes | Drakes population | 1234 |
| population.ducks | Ducks population | 2345 |
| population.ducklings | Ducklings population | 3456 |
| population.turkey | Turkey population | 123 |
| population.quails | Quails population | 456 |
| population.poultyBirds | Poultry birds (Gini Fowl, Ostrich, Emu, Geese) population | 789 |

## Dataset Coverage
- **All India Data**: Village/ward level livestock population across all states and union territories
- **Karnataka Data**: District and village-level detailed livestock statistics
- **Maharashtra Data**: District-level livestock and poultry statistics with breed categorization
- **State-level Summaries**: Comprehensive state-wise breakdowns by livestock type and breed

## Data Quality Notes
- All location IDs follow the Local Government Directory (LGD) standards
- Population figures represent actual counts from the 2019 census
- Some records may have missing location information (marked as admin_0)
- Poultry data includes both commercial and backyard categories where available