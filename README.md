# Amazon Vine Review Analysis

## Overview

The purpose of this project is to analyze Amazon reviews written by members of the paid Amazon Vine program. For this project we have selected the reviews about musical instruments. PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into postgres.PySpark was then used to determine if there is any bias toward favorable reviews from Vine members in the data

## Results:

For the purpose of this analysis, the data was filtered for reviews that had more than 20 votes and had 50% votes for helpful review. The results of the analysis are listed below

- There are a total 59 vine member review and 13452 non-vine member review for musical instruments
- 34 review were 5 star reviews for vine member review and 7674 for non-vine member reviews
- The percentage of 5 star ratings for vine member reviews and non-vine member reviews is approximately 57% (Vine reviews - 57.6%, Non-Vine Review - 57.02%)

**Vine Member Review Summary**

![vine_summary](https://github.com/ssathyanath/Amazon_Vine_Analysis/blob/main/Images/VineSummary.PNG)


**Non-Vine Member Review Summary**

![nonvine_summary](https://github.com/ssathyanath/Amazon_Vine_Analysis/blob/main/Images/NonVineSummary.PNG)


## Summary:
Based on the results of the analysis, there is no positivity bias for reviews in the Vine program. The difference between the percentage of positive review for vine members and non-vine members is 0.6%, which is relatively small. Further analysis can be performed to understand if there is positivity bias for reviews in the Vine program. Few of them are listed below,

- Verified purchase can be used as a filter to see if the percentage of fivestar reviews remain consistent for vine and non-vine members
- Analysing the reviews by customer can also indicate if a customer tends to provide frequent positive or negative review, which can then be factored into the vine vs non-vine review analysis