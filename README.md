# Colombo: Skylines

This project aims to create a virtual representation of Colombo, Sri Lanka using the Cities: Skylines game engine. The goal is to provide a visual and interactive tool for understanding urban design interventions and their potential impacts on the city.

## Table of Contents

1. [Project Overview](#project-overview)
2. [Data Sources](#data-sources)
3. [Methodology](#methodology)
   - [Topography](#topography)
   - [Land Use and Zoning](#land-use-and-zoning)
   - [Administrative Divisions](#administrative-divisions)
   - [Population and Citizens](#population-and-citizens)
   - [Transport](#transport)
   - [Visuals](#visuals)
4. [Limitations](#limitations)
5. [Usage](#usage)
6. [Conclusion](#conclusion)

## Project Overview

The Colombo City Skylines Project uses the Cities: Skylines video game as a platform to create a detailed, agent-based simulation of Colombo. This virtual city serves as a "Digital Twin" to help visualize and understand urban design interventions and their potential impacts.

Key features:
- 1:1 scale representation of Colombo's geography and road network
- Accurate land use and zoning based on official development plans
- Simulated population with commuting patterns
- Representation of public and private transport systems
- Visually customized to resemble Colombo's architecture and streetscapes

## Data Sources

The project relies on various data sources to ensure accuracy:

- UN State of Sri Lankan Cities report (2018)
- CoMTrans report and Home Visit Survey
- Urban Development Authority city development plans (2021-2030)
- Colombo Municipal Council maps and data
- Satellite imagery (Google Earth Pro, Sentinel-2)
- OpenStreetMap data
- Road Development Authority (RDA) data
- Asian Development Bank sector assessments
- Meta's Data for Good program (high-resolution population data)
- Expert consultations (e.g., Prof. Amal S. Kumarage, University of Moratuwa)

## Methodology

### Topography

1. Imported OpenStreetMap data for Colombo's road network
2. Mapped RDA road classifications to Cities: Skylines road types
3. Used satellite imagery to refine geographical features
4. Manually rebuilt roads to achieve 99% accuracy in city dimensions

### Land Use and Zoning

1. Extracted land-use map from Colombo city development plan
2. Mapped UDA categories to Cities: Skylines zoning types
3. Used Meta's high-resolution population data to determine density
4. Manually placed major institutions (schools, hospitals, universities)

### Administrative Divisions

- Partitioned the city into 15 districts based on Colombo Municipal Council maps

### Population and Citizens

1. Estimated 2020 population:
   - Total: 1,048,000
   - Residents: 555,300
   - Commuters: 492,700
2. Distributed commuter population based on seven major entry corridors
3. Used mods to customize population characteristics:
   - Realistic Population 2 (2.2.2.4)
   - Lifecycle Rebalance Revisited (1.6.8)

### Transport

1. Public Transport:
   - Replicated three main railway lines
   - Implemented three key bus routes
2. Private Transport:
   - Set vehicle spawn criteria based on RDA data
   - Modified traffic behavior using TM:PE mod
   - Adjusted vehicle-to-population ratios

### Visuals

1. Curated and created custom 3D assets to match Colombo's architecture
2. Used Google Street View to identify building types
3. Manually placed landmark buildings

## Modlist

## Limitations

- Population and vehicle ratios may not perfectly match real-world data due to game engine constraints
- Public transport runs on exact schedules without real-world variations
- Maximum of 135,000 total vehicles (moving and parked) at any given time

## Usage

This virtual Colombo can be used to:

1. Visualize and understand current urban design issues
2. Test and communicate potential infrastructure changes
3. Explore the impact of policy decisions on traffic and population distribution
4. Educate students and the public about urban planning concepts

## Conclusion

While not a perfect representation, this Cities: Skylines model of Colombo serves as a valuable tool for visualizing and communicating urban design concepts. It bridges the gap between complex urban planning data and public understanding, potentially improving discourse around city development projects.
