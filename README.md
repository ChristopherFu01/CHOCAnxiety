# Analysis of Anxiety Trends from CDC Data: Q2 2020 to Q2 2023

## Table of Contents

1. [Abstract](#abstract)
2. [Acknowledgments](#acknowledgments)
   - [Team Acknowledgment](#team-acknowledgment)
   - [Data Acknowledgment](#data-acknowledgment)
3. [Background](#background)
4. [Data Description](#data-description)
   - [Variables](#variables)
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

This study examines demographic disparities among individuals exhibiting signs of anxiety, based on data from the Centers for Disease Control and Prevention (CDC) spanning Q2 2020 to Q2 2023. The analysis aims to provide CHOC (Children's Health of Orange County) medical staff and physicians with actionable insights into potential factors contributing to anxiety across diverse populations. Using a comprehensive dataset, the study evaluates trends in anxiety prevalence across age, gender, race/ethnicity, socioeconomic status, and geographic regions. Statistical and machine learning techniques, including multivariate regression and t-tests, were applied to identify significant disparities and correlations. Preliminary findings highlight heightened anxiety indicators among the following populations: **females**, **southern states**, **states with large urban populations**,**Hispanics** and **people of mixed race**,**those with an associate's degree** and **those with less than a high school degree**, and **ages 18-29**. These insights are intended to inform targeted interventions, resource allocation, and culturally sensitive care strategies to better address anxiety among vulnerable populations, with future plans involving unsupervised machine learning for detecting interactions among key variables. The study underscores the importance of leveraging demographic data to understand and mitigate the complex factors driving mental health disparities.

If you would like to see a presentation format of this project, click [here](August%20Monthly%20Meeting%20Mi4%20Data%20Science.pdf).

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

This dataset contains information collected by the Centers for Disease Control and Prevention (CDC) on anxiety-related indicators from April 4th, 2020 to June 30th, 2023. The data has been curated for the purpose of analyzing demographic disparities in anxiety prevalence and understanding potential contributing factors. It includes various demographic, socioeconomic, and temporal attributes to enable in-depth analysis. The following dataset was used:

- `anxiety_data.csv`

### Variables

Below is a summary of the key variables in the dataset:

**Mental Health Indicators**
- **Indicator**:Categorical (Symptoms of Anxiety Disorder, Symptoms of Depressive Disorder, Symptoms of Anxiety Disorder or Depressive Disorder)
  - labeled disorder
- **Value**: Numerical (e.g. 18.6)
   - value indicating the likelihood of a disorder; higher values mean higher correspondence
   - This is our **main response variable** for assessing anxiety likelihood
- **Low CI**: Numerical (e.g. 14.6)
  - lowerbound of the confidence interval
- **High CI**: Numerical (e.g. 23.1)
  -  upperbound of the confidence interval
- **Confidence Interval**: Numerical (e.g. 14.6 - 23.1)
  - the full range of the confidence interval
- **Quartile Range**: Numerical (e.g. 16.5 - 20.7)
  - quartile range shown as an interval (?)

**Demographic Variables**
- **Group**: Categorical (National Estimate, By Age, By Gender, By Race/Hispanic ethnicity, By Education, By State)
  - type of group
- **State**: Categorical (e.g. United States, Alabama, Alaska, etc.)
  - full state name in the United States including "United States" and "District of Columbia"
- **Subgroup**: Categorical (e.g. United States, 18-29 years, Male, Hispanic or Latino, etc.)
  - type of subgroup within a certain group

**Temporal Variables**
- **Week**: Categorical (e.g. 1, 2, 3, etc.)
  - numeric value indicating which week # it is; total of 7 observed weeks
- **Week Label**: Categorical (e.g. Apr 23 - May 5)
  - date (month and day) for a certain week
       - Week 1: Apr 23 - May 5
       - Week 2: May 7 - May 12
       - Week 3: May 14 - May 19
       - Week 4: May 21 - May 26
       - Week 5: May 28 - June 2
       - Week 6: June 4 - June 9
       - Week 7: June 11 - June 16

## Exploratory Data Analysis

## Modeling

### Model Development

### Model Evaluation

## Conclusion

### Insights

The following demographic groups experienced heightened indicators of anxiety:

- **Females**
- **Southern States**
  - Texas, Alabama
- **States with Large Urban Populations**
  - California, New York
- **Hispanics** and **people of mixed race**
- **Those with an Associate's Degree** and **Those with less than a High School Degree**
- **Ages 18-29 (Young Adults)**

### Limitations

One of the attributes that we failed to investigate into was the temporal aspects of the dataset. Looking into the weeks, especially data points originating from the COVID-19 pandemic period, would give us insight into whether certain years, seasons, months, or weeks experience increased anxiety.

Another limitation of our study was not optimizing model performance or trying other supervised machine learning models, as those models could offer greater insight into feature importance.

### Future Plans

We hope to implement an unsupervised learning approach to develop a better understanding of how these variables interact with one another. Our goals would include:
- Determining the covariance to characterize the patient population
   - Example: Higher education patterns within racial groups can contribute to lower anxiety scores
- Obtaining a higher quality data set to solidify and further our findings

We also plan to do more time series analysis in order to determine if anxiety was heightened during the COVID-19 Pandemic as well as recent trends in anxiety. 

Accomplishing these goals first would allow us to proceed with investigating data provided by CHOC directly by assisting in narrowing our focus and priorities, eventually leading to model deployment by CHOC in order to alleviate populations suffering under anxiety.

## Dependencies

- pandas
- matplotlib
- scipy
- plotly
- statsmodels
- seaborn
- numpy

## Project Folder Structure

```plaintext
CHOCAnxiety/
|
├── EDA                                                  # Folder containing photos of EDA
|   ├── Age                                              # Folder containing photos of EDA for age
|   |   ├── box.png                                      # photo of boxplot for age groups
|   |   ├── meanval.png                                  # photo of barplot for mean value split by age
|   |   ├── stats.png                                    # photo of statistics for age
|   |   └── val.png                                      # photo of different values by age
|   |
|   ├── Education                                        # Folder containing photos of EDA for education
|   |   ├── box.png                                      # photo of boxplot for education groups
|   |   ├── meanval.png                                  # photo of barplot for mean value split by education
|   |   ├── stats.png                                    # photo of statistics for education
|   |   └── val.png                                      # photo of different values by education
|   |
|   ├── Gender                                           # Folder containing photos of EDA for gender
|   |   ├── box.png                                      # photo of boxplot for gender
|   |   ├── meanval.png                                  # photo of barplot for mean value split by gender
|   |   ├── stats.png                                    # photo of statistics for gender
|   |   └── val.png                                      # photo of different values by gender
|   |
|   ├── Race                                             # Folder containing photos of EDA for race
|   |   ├── box.png                                      # photo of boxplot for race groups
|   |   ├── meanval.png                                  # photo of barplot for mean value split by race
|   |   ├── stats.png                                    # photo of statistics for race
|   |   └── val.png                                      # photo of different values by race
|   |
|   ├── States                                           # Folder containing photos of EDA for states
|   |   ├── box.png                                      # photo of boxplot for states
|   |   ├── meanval.png                                  # photo of barplot for mean value split by states
|   |   ├── stats.png                                    # photo of statistics for states
|   |   └── val.png                                      # photo of different values by states
|   |
|   ├── Week                                             # Folder containing photos of EDA for week
|   |   ├── box.png                                      # photo of boxplot for week
|   |   ├── meanval.png                                  # photo of barplot for mean value split by week
|   |   ├── stats.png                                    # photo of statistics for weeks
|   |   └── val.png                                      # photo of different values by week
|   |
|   └── Dataset.png                                      # photo of dataset in jupyter notebook using python pandas
|
├── Model Building                                       # Folder containing photos regarding models
|   ├── MLR                                              # Folder containing photos for multivariate linear regression model
|   |   ├── model_summary.png                            # model summary for multivariate regression model
|   |   ├── sig_groups.png                               # table of groups which were considered significant
|   |   ├── sig_states.png                               # table of states which were considered significant
|   |   ├── sig_subgroups.png                            # table of subgroups which were considered significant
|   |   ├── sig_weeks.png                                # table of weeks which were considered significant
|   |   
|   ├── SLR                                              # Folder containing photos for single linear regression model
|       ├── Age                                          # Folder containing photo(s) for single linear regression model for age
|       |   └── model_summary.png                        # model summary table for linear regresion model based on age
|       |
|       ├── Education                                    # Folder containing photo(s) for single linear regression model for education
|       |   └── model_summary.png                        # model summary table for linear regresion model based on education
|       |
|       ├── Gender                                       # Folder containing photo(s) for single linear regression model for gender
|       |   └── model_summary.png                        # model summary table for linear regresion model based on gender
|       |
|       ├── Race                                         # Folder containing photo(s) for single linear regression model for race
|       |   └── model_summary.png                        # model summary table for linear regresion model based on race
|       |
|       └── States                                       # Folder containing photo(s) for single linear regression model for states
|           └── model_summary.png                        # model summary table for linear regresion model based on states
|        
|
├── code/                                                # Folder containing all code related files
|   ├── (CHRIS) Anxiety Based on Age.ipynb               # Jupyter Notebook for EDA + model for Anxiety and Age
|   ├── (CHRIS) Anxiety Based on Education.ipynb         # Jupyter Notebook for EDA + model for Anxiety and Education
|   ├── (CHRIS) Anxiety Based on Race.ipynb              # Jupyter Notebook for EDA + model for Anxiety and Race
|   ├── (CHRIS) Anxiety Based on States.ipynb            # Jupyter Notebook for EDA + model for Anxiety and States
|   ├── (CHRIS) Anxiety Based on Weeks.ipynb             # Jupyter Notebook for EDA + model for Anxiety and Weeks
|   ├── (CHRIS) Anxiety Prelim Analysis + Gender.ipynb   # Jupyter Notebook for early EDA and Gender EDA + model
|   ├── (CHRIS) Depression Based on States.ipynb         # Jupyter Notebook containing EDA and model for depression geographically
|   └── (CHRIS) MLR model based on Anxiety.ipynb         # Jupyter Notebook for multivariate linear regressio model
|
├── data/                                                # Folder containing all data file(s)
|   └── anxiety_data.csv                                 # dataset from CDC containing anxiety and depressed people 
|
|
├── August Monthly Meeting Mi4 Data Science.pdf          # PDF of presentation shown at the Mi4 CHOC August Monthly Meeting
├── LICENSE                                              # License information
└── README.md                                            # Project documentation
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
