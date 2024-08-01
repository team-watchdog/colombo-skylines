# Colombo: Skylines
by Nimesha Periyapperuma and Yudhanjaya Wijeratne

This repository contains Team Watchdog's simulation of the city of Colombo. This is an accurate topographical representation of Colombo, built with detailed land use and zoning based on official city development plans centererd around 2020; over a million virtual citizens, simulating population dynamics that reflect large-scale, real-world demographics and human movement; public transport based on actual route data; and curated visual assets to better match Colombo's unique architectural style. 

![image](https://github.com/user-attachments/assets/ce65de82-8c8c-4251-b90d-90727196ba2d)

This project is built with the use of publicly available data from
- Colombo Municipal Council
- Sri Lanka Road Development Authority
- Sri Lanka Urban Development Authority
- Sri Lanka Department of Census and Statistics 
- University of Moratuwa's Department of Transport and Policy Planning 
- META's Data for Good projects, especially their population mapping work with the Center for International Earth Science Information Network (CIESIN) at the Columbia Climate School
- UN-Habitat 
- The ComTRANS reports and its associated studies and surveys 
- OpenStreetMap 
- ESA's Sentinel-2 program, from which we've gotten a lot of satellite imagery: see [https://github.com/team-watchdog/satellite2024](https://github.com/team-watchdog/satellite2024)
- Google Maps and Routemaster.lk for bus and train routes

Special thanks to Professor Amal Kumarage and Dr. Amila Jayasinghe for data, research, and contributions, especially around the commuter flow across the main arteries that connect the CMC with the rest of the country. This project would not exist without the knowledge and hard work from immensely talented modding community around Cities: Skylines: Andreas Pardeike, boformer, kian.zarrin, FireController#1847, LinuxFan, Krzychu1245, leftbehind, Bloodypenguin, algernon, Chamëleon TBN, Simon Ryr and others listed in full in the mods section.    

## Table of Contents
1. [Introduction](#introduction)
2. [Project Overview](#project-overview)
3. [Methodology](#methodology)
   - [Topography](#1-topography)
   - [Land Use and Zoning](#2-land-use-and-zoning)
   - [Administrative Divisions](#3-administrative-divisions)
   - [Citizens and Populations](#4-citizens-and-populations)
   - [Transport](#5-transport)
   - [Visuals](#6-visuals)
4. [Key Findings and Limitations](#key-findings-and-limitations)
5. [Conclusion and Future Applications](#conclusion-and-future-applications)
6. [References and Data Sources](#references-and-data-sources)

## Introduction

In early 2024, we started working on something to help the general public better understand the city of Colombo and the impacts of various urban design interventions. Our goal was to create a more accessible and visual tool for citizens to comprehend urban problems and judge the impact of different decisions. This project was inspired by our previous work at Watchdog, where we spend months of research and ultimately [wrote a monumental 13,000+ word collection on explaining Sri Lankan transport](https://watchdog.team/article/too-slow-too-furious). Ultimately, what we realized was that there had to be some visual way to bridge the gap between professional expertise (often confined to academic papers and reports) and public understanding.

Our virtual city of Colombo serves as a crude "Digital Twin," offering a platform to:

1. Visualize and understand current urban design issues
2. Test and communicate potential infrastructure changes
3. Explore the impact of policy decisions on traffic and population distribution
4. Educate students and the public about urban planning concepts

Potential applications include:

1. Simulating changes in roads, transport routes 
2. Exploring effects of changes in private transport policies
3. Visualizing impact of new infrastructure like monorails or wider pavements
4. Assessing effects of introducing more green spaces or parking areas

While not a completely accurate simulation, this "toy universe model" provides a useful tool for visualizing and communicating urban development concepts. 

## Project Overview

We chose to use Cities Skylines, a 2015 video game, as our simulation platform. This choice was driven by several factors:

- Cost-effectiveness: $19.99 for a perpetual license vs. $6,000-$8,600 for professional software like CUBE
- Ease of use for the general public
- Superior visualization capabilities
- Thriving modding community for extended functionality
- Reputation for complex and flexible urban simulation


### 1. Topography

We focused on recreating the Colombo Municipal Council (CMC) area as of 2020. Key steps included:

- Acquiring OpenStreetMap data for Colombo's road network (from Wattala to Dehiwala and from Colombo Port City to Maharagama)
- Importing road types piecemeal: motorways, trunk roads, primary, secondary, tertiary roads, and linking nodes
- Using satellite imagery to sculpt features like green spaces, water bodies, and canals
- Rebuilding each visible road using overlap maps from CMC and Google Maps

The result was a highly accurate representation:
- 7728 m long (real city: 7780m)
- 4585.6 m at its widest (reality: 4611.2m)
- Over 99% match in road layout, parks, and water bodies

![image](https://github.com/user-attachments/assets/4f8b3f0a-e96b-48eb-8d79-8c9f538e8728)


### 2. Land Use and Zoning

We extracted land-use data from the Colombo city development plan and mapped it to Cities Skylines' zoning categories:

1. Initial zoning with low-density residential and commercial buildings; government buildings were zones as commercial buildings, and religious sites were zones as parks, due to similar use patterns for virtual citizens
2. We used high-resolution population data from Meta's Data for Good program to identify high-density areas, and rezoned using Skylines' high-density commercial and residential categories
4. Added small lanes to accurately fill areas (mimicking real-world "Mawathas" or Avenues)
5. Placed major schools, hospitals, and universities based on CMC maps

### 3. Administrative Divisions

We partitioned the city into 15 districts based on Colombo Municipal Council maps, allowing for more granular statistical observation and population calibration.
![image](https://github.com/user-attachments/assets/7e945d3e-b757-4620-9f42-ee53120056b2)

### 4. Citizens and Populations

- Estimated 2020 population for the CMC area: 1,048,000 total people (555,300 night-time population, 492,700 commuters)
- Our current version sits at  1,020,775 virtual citizens, with the CMC area modelled and population centers along extended corridors to simulate commuter influx 
- Using Realistic Population 2 2.2.2.4 and Lifecycle Rebalance Revisited 1.6.8, we've adjusted settings to mimic real-world population density and demographics - citizens age, go to schools, work and die in ways closer to real-world analogues than Skyline's default assumptoins


### 5. Transport

We implemented both public and private transport systems:

Public Transport:
- Replicated three main railway lines:
  1. Main Line: Fort - Maradana - Ragama
  2. Coastal Line: Fort - Ratmalana
  3. Kelani Valley Line: Maradana - Padukka

- Implemented six key bus routes:
  1. Route 100: Dehiwala - Pettah
  2. Route 103: Pettah - Park Road via Narahenpita
  3. Route 104: Ja-Ela - Bambalapitiya
  4. Route 120: Piliyandala - Pettah 
  5. Route 138: Maharagama - Pettah
  6. Route 174: Kottawa - Borella
    
![image](https://github.com/user-attachments/assets/4eba8cee-ef5a-43cb-b0ed-b9c288fb26ed)

Private Transport:
- Set vehicle spawn criteria based on transport modality figuresd from the RDA's National Master Plan
- Modified traffic behavior using TM:PE mod to reflect Sri Lankan driving habits:
  - Buses may ignore lane arrows
  - Vehicles may enter blocked junctions
  - Vehicles may do U-turns at junctions
  - 10% of drivers are reckless
  - Vehicles may park on the sides of streets
  - Three wheelers and scooters
  
![image](https://github.com/user-attachments/assets/43fb27ed-8a11-4c0a-89dc-7f3f8b312419)

### 6. Visuals

To improve visual accuracy:

- Curated thousands of 3D assets to replace default buildings
- Built custom 3D models for iconic structures like Nelum Kuluna
- Used Google Street View to identify and replicate building types in each district
- Selected assets for trains, buses, and three-wheelers to match real-world vehicles

## Key Limitations

The Skylines engine, even when modded to the hilt, has the following limits
- 298.6 sq km maximum area
- 1,048,576 maximum citizens
- 49,152 maximum individual buildings
- 65,636 maximum vehicles in motion
- 65,636 maximum parked vehicles
- 256 maximum transport lines (bus routes, train routes)

So we have a few notable issues: 

1. The real CMC has a floating population of over 500,000 vehicles. We can only simulate a fraction of that.
2. This shows up as a vehicle-to-population ratio discrepancy: 
   - Real Colombo: 1:5 ratio (206 vehicles per 1000 people)
   - Our model: Approximately 1:10 ratio
3. Perfect adherence to schedules in public transport, unlike real-world variation
4. Transport speeds can be adjusted for each type of vehicle, but currently do not mirror real life
5. Visual assets are taken from many different mods for countries other than Sri Lanka, and despite our best efforts, do not look completely Sri Lankan.

## More Information

For detailed documentation on methodology, data sources, technical specifications and a guide on how to get this running on your own machine, please refer to our [project wiki](https://github.com/team-watchdog/colombo-skylines/wiki).

## License

We present this tool in the hope that it will facilitate better communication and understanding of urban planning issues in Colombo. This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Contact

For questions or collaborations, please open an issue or contact the project maintainers directly.




