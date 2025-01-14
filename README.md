# Analysis of Anxiety Trends from CDC Data: Q2 2020 to Q2 2023

## Table of Contents

1. [Abstract](#abstract)
2. [Acknowledgments](#acknowledgments)
   - [Team Acknowledgment](#team-acknowledgment)
   - [Data Acknowledgment](#data-acknowledgment)
3. [Background](#background)
4. [Data Description](#data-description)
5. [Exploratory Data Analysis](#exploratory-data-analysis)
6. [Modeling](#modeling)
   - [Model Development](#model-development)
   - [Model Evaluation](#model-evaluation)
7. [Conclusion](#conclusion)
   - [Insights](#insights)
   - [Limitations](#limitations)
   - [Future Plans](#future-plans)
8. [Dependencies](#dependencies)
9. [Project Folder Structure](#project-folder-structure)
10. [References](#references)
11. [Contact Information](#contact-information)

## Abstract

This study examines demographic disparities among individuals exhibiting signs of anxiety, based on data from the Centers for Disease Control and Prevention (CDC) spanning Q2 2020 to Q2 2023. The analysis aims to provide CHOC (Children's Health of Orange County) medical staff and physicians with actionable insights into potential factors contributing to anxiety across diverse populations. Using a comprehensive dataset, the study evaluates trends in anxiety prevalence across age, gender, race/ethnicity, socioeconomic status, and geographic regions. Statistical and machine learning techniques, including multivariate regression and t-tests, were applied to identify significant disparities and correlations. Preliminary findings highlight heightened anxiety indicators among the following populations: **females**, **southern states**, **states with large urban populations**,**Hispanics** and **people of mixed race**,**those with an associate's degree** and **those with less than a high school degree**, and **ages 18-29**,. These insights are intended to inform targeted interventions, resource allocation, and culturally sensitive care strategies to better address anxiety among vulnerable populations, with future plans involving unsupervised machine learning for detecting interactions among key variables. The study underscores the importance of leveraging demographic data to understand and mitigate the complex factors driving mental health disparities.

## Acknowledgments

### Team Acknowledgment

I would like to extend my gratitude towards the following members of the Data Science Intern Mi4 Group at CHOC for their contributions:

- Maximilian Waller
- Minjue Wu
- Nick Yousefi

### Data Acknowledgment

The data used in this project was provided by the National Center for Health Statistics and CDC at the following address: [https://data.cdc.gov/NCHS/Indicators-of-Anxiety-or-Depression-Based-on-Repor/8pt5-q6wp/about_data](url)

Note that the dataset has been updated since October 4, 2024, whereas the project itself focuses on data the Summer of 2023 and before. The most notable changes in the updated dataset that are NOT present in this dataset include:

- Columns including Phase, Time Period (as opposed to Week), Time Period Label (as opposed to Week Label), Time Period Start Date, and Time Period End Date

## Background

## Data Description

## Exploratory Data Analysis


## Modeling

### Model Development

### Model Evaluation

## Conclusion

### Insights

### Limitations

### Future Plans

We hope to implement an unsupervised learning approach to develop a better understanding of how these variables interact with one another. Our goals would include:
- Determining the covariance to characterize the patient population
   - Example: Higher education patterns within racial groups can contribute to lower anxiety scores
- Obtaining a higher quality data set to solidify and further our findings

We also plan to do more time series analysis in order to determine if anxiety was heightened during the COVID-19 Pandemic as well as recent trends in anxiety. 

Accomplishing these goals first would allow us to proceed with investigating data provided by CHOC directly by assisting in narrowing our focus and priorities, eventually leading to model deployment by CHOC in order to alleviate populations suffering under anxiety.

## Dependencies

## Project Folder Structure

```plaintext

```

## References

Anxiety Disorders - Facts & Statistics (https://adaa.org/understanding-anxiety/facts-statistics)
2. Anxiety Facts: All You Need to Know (https://psychcentral.com/anxiety/anxiety-facts)
3. Unequal depression for equal work? How the wage gap explains gendered disparities in mood disorders (https://www.sciencedirect.com/science/article/pii/S0277953615302616)
4. US National and State-Level PRevalence of Mental Health Disorders and Disparities of Mental Health Care Use in Children (https://jamanetwork.com/journals/jamapediatrics/fullarticle/2724377)
5. A Cross-Ethnic Comparison of Lifetime Prevalence Rates of Anxiety Disorders (https://www.ncbi.nlm.nih.gov/pmc/articles/PMC2931265)
6. Does a higher educational level protect against anxiety and depression? The HUNT study (https://pubmed.ncbi.nlm.nih.gov/18234406/)
7. Age differences in psychological distress during the COVID-19 pandemic: March 2020 – June 2021 (https://www.frontiersin.org/articles/10.3389/fpsyg.2023.1101353/full)

## Contact Information

For any questions, please contact:

- Name: Christopher Fu
- Email: christopherfuwas@gmail.com
