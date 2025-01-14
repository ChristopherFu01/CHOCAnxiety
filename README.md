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

The [data](https://data.cdc.gov/NCHS/Indicators-of-Anxiety-or-Depression-Based-on-Repor/8pt5-q6wp/about_data) used in this project was provided by the National Center for Health Statistics and CDC.

Note that the dataset has been updated since October 4, 2024, whereas the project itself focuses on data the Summer of 2023 and before. The most notable changes in the updated dataset that are NOT present in this dataset include:

- Columns including Phase, Time Period (as opposed to Week), Time Period Label (as opposed to Week Label), Time Period Start Date, and Time Period End Date

## Background

Anxiety disorders are among the most prevalent mental health conditions, affecting millions of individuals across various demographic groups; the Anxiety and Depression Association of America (ADAA) reports that 19.1% of US adults and 31.9% of adolescents annually are diagnosed with anxiety disorders<sup>[1]</sup>. Psych Central has also reported that approximately 50% of people have Generalized Anxiety Disorder symptoms for 2+ years before being diagnosed<sup>[2]</sup>. 

Understanding the contributing factors and disparities in anxiety prevalence is crucial for developing targeted interventions and providing effective care. Although there are screening tools that exist for depression (PHQ-2) based on various risk factors<sup>[3]</sup>, it is unknown if there are tools of equal capabilities for screening anxiety disorders. The COVID-19 pandemic, which began in early 2020, significantly disrupted lives worldwide, amplifying stressors such as health concerns, economic instability, and social isolation. These factors have contributed to a marked increase in anxiety symptoms across diverse populations.

The Centers for Disease Control and Prevention (CDC) has collected extensive data on mental health trends, offering a valuable resource for analyzing patterns of anxiety over time. This project leverages CDC data spanning April 4th, 2020 to June 30th, 2023 to explore demographic disparities in individuals exhibiting signs of anxiety. By examining variables such as age, gender, race/ethnicity, socioeconomic status (e.g. degree level), and geographic region, this analysis aims to uncover underlying trends and potential contributing factors.

The findings will be tailored to support CHOC (Children's Health of Orange County) medical staff and physicians in their efforts to address anxiety within their patient populations. By identifying at-risk groups and understanding the demographic factors influencing anxiety, this project seeks to enable evidence-based decision-making, inform resource allocation, and promote equitable care practices. This work is part of a broader commitment to advancing mental health outcomes through data-driven approaches, and its insights can benefit future data analyses for CHOC-specific data.

## Methodology

Our approach consists of the following steps:
1. Using the public dataset provided by the CDC, we can begin investigating potential factors of anxiety.
2. After an exploratory search of these variables, we can deploy models for further insight findings. We will start with supervised machine learning such as the multivariate regression model, then deploy an unsupervised learning techniques such as clustering and covariance in order to find hidden patterns within these groups.
3. Developing these findings will enable us to apply their value to further data analyses when CHOC provides their data, accelerating our search into anxiety within pediatric patients.

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

1. Anxiety Disorders - Facts & Statistics (https://adaa.org/understanding-anxiety/facts-statistics)
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
