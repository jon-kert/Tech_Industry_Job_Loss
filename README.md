# Job Loss Metrics in the Tech Industry
**Created By**: Jonathan Kertawidjaja, Philip Hadiwidjaja

**Website Link**: https://jon-kert.github.io/Tech_Industry_Job_Loss/

**Original Dataset Link**: https://layoffs.fyi/

## Introduction
We wanted to tailor our project with the industries we are interested in pursuing in our careers. Given recent downward trends in tech-related jobs, we thought that it would be interesting to center our final project on the issue of tech layoffs. We hope to gain a **deeper understanding** of the current state of the tech industry while gaining valuable experience and practice with the skills learned throughout this semester.

The dataset we will be using for this project comes from kaggle and can be accessed through [this link](https://www.kaggle.com/datasets/ulrikeherold/tech-layoffs-2020-2024/data). The original dataset is from [layoffs.fyi](https://layoffs.fyi/). The data set captures layoff events in the tech sector from **2020** to **2024**, including both large-scale and smaller workforce reductions across a variety of companies and industries. The data set only contains one CSV file with 16 columns and 1672 observations.

## Research Question
Our main research question is: **Is the number of workeforce reductions related to the year of the layoffs as well as geographical and company-level characteristics?**. Additionally, we aim to **predict the number of layoffs a company faces given the year, location, and company-level characterisitics**. These are the features that we will focus on in our investigation:

Features:

- "Stage" — Funding stage (e.g., private, public, growth-stage)
- "Industry" — Sector or type of tech company (e.g., fintech, SaaS)
- "Money_Raised_in_$_mil" – Total funding raised in millions of USD.
- "Company_Size_before_Layoffs" - The amount of employees before workforce reduction
- "Country" – Country of company headquarters.
- "Continent" – Broader regional classification.
- "Location_HQ" – City or specific area of the headquarters, useful for identifying clusters or local economic patterns.
- "Percentage" - This is the target variable that we are trying to predict. Given the features above, what is the severity of the layoffs?
- "Laid-off" - This is also a target variable that is tangential to the percentage variable in that we are trying to predict the amount of employees laid off given the features above

---

## Data Cleaning and Exploratory Data Analysis


### Univariate Analysis (a)
In the plotly histogram below, it can be seen that the distribution of layoff events categorized by the stage of the company (i.e. Series H, Post-IPO, etc.). Most of the reductions in the workforce seem to be happening in Post-IPO companies, which are bigger companies that have gone through multiple rounds of investment and are established(hold good amount of market share) in their respective industry. This makes sense because Post-IPO companies are more subjective to layoffs due to pressure from the market/industry. Contributing to our research question, this graph shows that there could be a correlation or indication of high percentage of layoffs given the company's stage as there are more occurences of layoffs.




### Univariate Analysis (b)
The violin plot below shows the distribution of values found in the "Percentage" column of the dataset. The bulk of the percentages lie around the **5-20 range**, with few outliers lie between **60-100**. After further investigation we found that companies that fell within the 60-100 range were **predominantly in the early stages of growth**. These companies often have fewer workers, thus even losing a small number of workers would raise their loss percentage. A high percentage loss of workers in an early-stage company will most likely equal a low-percentage loss of workers in a later-stage company. These findings indicate that an early stage company is **more likely** to face a high-percentage loss of workers.




### Bivariate Analysis (a)
The graph below correlates the total amount of workers laid off by year and quarter. For reference, the quarters refer to the following range of months:


>'Q1' : January 1st - March 31st
>'Q2' : April 1st - June 30th
>'Q3' : July 1st - September 30th
>'Q4' : October 1st - December 31st

From the graph below it can be seen that the overall trend of workers laid off seem to have **spiked in 2023 and 2020 during this 4 year period**. There could be a multitude of including broader economic and political factors that cannot be predicted. For instance, the initial shock between 2020 Q1 to 2020 Q3 can be attributed to the emergence of Covid-19 forcing many companies to let go of their employees as a result of economic shock. In 2023 Q1, the spike could be attributed to tech layoffs that resulted from the mass hiring spree that companies went on in the years prior. After further investigation, we have come to the conclusion that the different quarters would not be a useful predictor mainly because of the unpredictability of real life events that may heighten the amount of layoffs in a quarter.




### Bivariate Analysis (b)
The bar plot below shows the relationship between the categorical column 'Stage' and numerical column 'Laid_Off'. Notably, aside from the  'Acquired', 'Post-IPO', and 'Private Equity' stages, there appears to be a trend of **increaseing numbers of workers laid off as companies mature**. The reason for this trend is because companies often start out with a smaller workforce, and as they grow there is a greater potential for a larger number of workers to be laid off. This figure shows that the company stage can be quite indicitive to how many workers are laid off.



### Aggregation
The figure below is a heatmap which represents a pivot table that aggregates the 'Stage', 'Industry' and 'Percentage' columns. Each cell in the heatmap represents the average percentage loss a companies that falls into 1 specific Stage and 1 specific Industry. The heatmap highlights the **intensity** in the relationship between Stage, Industry, and Percent-loss, allowing us to identify patterns among different Industry types and company stages. 

### Imputations

---

## Framing A Prediction Problem

## Baseline Model

## Final Model
