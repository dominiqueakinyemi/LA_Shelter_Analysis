# LA Shelter Analysis: Improving Outcomes for High-Risk Dog Breeds

Click here to download the full project documentation as a PDF file: [ShelterAnalysisDocumentation.pdf](https://github.com/user-attachments/files/17963021/ShelterAnalysisDocumentation.pdf)


## Table of Contents

- [Project Overview](#project-overview)
- [Data Sources](#data-sources)
- [Data Cleaning and Preparation](#data-cleaning-and-preparation)
- [Analysis Methods](#analysis-methods)
- [Key Findings](#key-findings)
- [Key Visualizations](#key-visualizations)
- [Recommendations](#recommendations)
- [Conclusion](#conclusion)
- [Limitations](#limitations)
- [References](#references)

## Project Overview

Los Angeles County animal shelters are over capacity. At the time of this project, they are 180% over capacity. This project will analyze shelter data to identify which dog breeds contribute most to overpopulation and have the lowest adoption rates, longest stays, or highest risk of euthanasia. The goal is to use this analysis to develop actionable strategies for increasing adoption rates and reducing shelter overpopulation.

**This overview provides summaries for each project stage. To view the full analysis steps, download the PDF version of ShelterAnalysisDocumentation. To replicate the analysis yourself, download the ShelterAnalysisDocumentation.Rmd project file and the cleaned "shelter_dogs" data set from this repository.**

### Skills
- Data cleaning
- Exploratory data analysis
- Data filtering
- Trend analysis
- Data visualization

### Tools
- R

## Data Sources

For this project, I used the "Animal Care PawStats Data" provided by Los Angeles County on their open data website. The data set can be accessed [here](https://data.lacounty.gov/datasets/lacounty::animal-care-pawstats-data/). The data is frequently updated and maintained, with the most recent update being September 3, 2024 (as of the project date). It includes over 300,000 records (including all animal types).

## Data Cleaning and Preparation

I performed the following tasks:
1. Filtered other animals from data to isolate dogs
2. Standardized capitalization and formatting
3. Removed redundant columns
4. Resolved missing values
5. Standardized intake and outcome types
6. Removed deceased and transient intakes
7. Removed obvious error entries
8. Standardized breed names through mapping

## Analysis Methods
- EDA: performed in-depth analysis of the entire dataset to examine intake and outcome trends for all shelters and breeds.

- Filtering: isolated the six high-risk breeds based on overrepresentation in data, based on high euthanasia rates, low adoption rates, and long stays.

- Trend Analysis: compared monthly and yearly trends for high-risk breeds with overall shelter populations.

## Key Findings

Overall Shelter Trends
- Intakes peaked in 2019, then decreased in 2020-2021 (COVID-19 Pandemic).
- Intakes and euthanasia have increased in 2022-2023 (adoption increasing, though less steeply).

High Risk Breeds
- **Bull Terriers, German shepherds, Chihuahuas, Siberian huskies, Boxers, and Rottweilers.**
- These breeds either make up more than 10% of the overall data set (extreme outliers causing over-population) OR
- Have an adoption rate higher than the average of 42% (which is already less than half of all dogs), a euthanasia rate higher than the average of 14% (some breeds as high as 25%), or stays longer than the average of 15 days.
- While the overall population saw an increase in adoptions from 2022 to 2023, high-risk dogs saw a decrease in adoptions.
- Rescue involvement has decreased for both the overall population and high-risk population.
  
## Key Visualizations
![breed_histogram_full](https://github.com/user-attachments/assets/6924e2d6-7a53-47c9-a9ae-1164586a6a44)
![yearly_intake_bar](https://github.com/user-attachments/assets/d347698b-d873-4945-b0bf-f4cd706ab5e0)
![monthly_comparison_charts](https://github.com/user-attachments/assets/a3ced479-2ed3-41fe-8a16-6a3f1c5ec771)
![yearly_comparison_charts](https://github.com/user-attachments/assets/95ea8607-0b35-49a0-af41-b188b0e194ed)

## Recommendations

Based on this analysis, I recommend the following actions:
- Targeted adoption campaigns for high-risk breeds.
- Strengthen relationships with breed-specific rescue groups.
- Manage shelter populations by reducing intakes.

## Conclusion
The ultimate goal is to increase positive outcomes (adoptions and rescues) while decreasing negative outcomes (euthanasia and long shelter stays) for the high-risk breeds identified in this project. By specifically dealing with the breeds that are prevalent and vulnerable, LA County shelters can better manage overpopulation and improve outcomes for all dogs in their care.

## Limitations

- Scope: This project will limit its focus to dogs (excluding cats from the original data) in the Los Angeles area only. The data set used contains animal intake records for LA County Shelters only and is provided by the city's open data website. This analysis will not include data from City of LA animal shelters. While the City of LA does have some adoption data available publicly, it is not comprehensive and lacks data on breeds. LA County's database is cleaner, more complete, and covers a larger time period/area, so it was the sole focus of this analysis.

- No age or gender data included in data set

## References

1. [PawStats Data Source Info](https://data.lacounty.gov/datasets/lacounty::animal-care-pawstats-data/about)
2. [AKC Offical Dog Breed List](https://www.akc.org/dog-breed)
