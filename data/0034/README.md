# Local Government Directory (LGD)

## Why LGD?
LGD (Local Government Directory) is used to avoid confusion with names that persists across data. There are cases of 2 or more villages in the same Taluka having the same name. While some confusion is unavoidable, the intent of this dataset is to reduce the confusion.

## Download
The files can be downloaded from github directly:

- [All India Local Government Directory](https://raw.githubusercontent.com/dsih-artpark/publicdata/refs/heads/main/data/0034/regionids.csv)

## Data Dictionary

| Column | Description | Example |
|--------|-------------|---------|
| regionID | Unique identifier for the region | state_29 |
| regionName | Name of the region | Karnataka |
| parentID | ID of the parent region | country_IN |



## What are regions
The way regions are defined in our data - there are two primary hierarchies: revenue, and urban local bodies.

1. Revenue: Hierarchy used by the government of India for revenue purposes. This hierarchy is unlikely to change. The hierarchy is: Country -> States and Union Territories -> Districts -> Subdistricts (aka Talukas) -> Villages
2. Urban Local Bodies (ULB's): ULB's exist outside the revenue hierarchy, and are incorporated local governments that perform their own duties. This is crucial because a lot of public health decision making, especiall in human health and climate response, is all handled by incorporated local governments that recieve support from the state and central/federal governments.


## How regionIDs are constructed

For districts, subdistricts, and states - the LGD Code is combined with the region type, so, for e.g.

If the state of Karnataka has an LGD code of 29
So the regionID is state_29

For Zones, Wards, Prabhags, and any other municipal areas, we rely on the Municipal Corporation for the names of the regions. The regionID is then constructed based on the parent ULB (Urban Local Body)

For e.g., if Pimpri Chinchwad Municipal Corporation of Pune District (Maharashtra State) has a ULB code of 251528, and has a zone "zone A" and zone A has a ward "Ward No 10". This will appear as:

regionID	regionName	parentID
state_27	MAHARASHTRA	country_IN
district_490	PUNE	state_27
ulb_251528	PIMPRI CHINCHWAD	district_490
zone_251528-1	ZONE A	ulb_251528
ward_251528-10	PIMPRI CHINCHWAD WARD NO. 10	zone_251528-1

If a ward name was provided, this would substitute the existing "PIMPRI CHINCHWAD WARD NO. 10"

Additionally, all region names are capitalised.

The data was last updated in April 2024.

BBMP uses the older ward system.


## Changelog
** * Effective 19th June 2024, four subdistricts were added to regionids.csv under state = Karnataka'subdistrict_7407', 'subdistrict_7398', 'subdistrict_7404', 'subdistrict_7403'