# Amazon Vine Analysis
## Overview of the Analysis

![Review Image](https://www.revuze.it/wp-content/uploads/2020/03/Amazon-Review-Analysis-1024x496.png)

The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. In this project, Amazon reviews written by members of the paid Amazon Vine program was analyzed using Natural Language Processing to translate the reviews for analysis. PySpark was also used to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. 

## Results
Reviews for health personal care were analyzed. The data was filtered to retrieve all the rows where the total votes count is equal to or greater than 20 to pick reviews that are more likely to be helpful. After the data has been filtered, another filter was added to retrieve all the rows where the ratio of helpful votes to total votes is equal or greater than 50%. The results were outlined below. 

![Total Votes](https://github.com/kntln/Amazon_Vine_Analysis/blob/main/images/total_votes_greater_than_20.png)

![Percent Votes](https://github.com/kntln/Amazon_Vine_Analysis/blob/main/images/percent_votes.png)

1. How many Vine reviews and non-Vine reviews were there?
    - There were 497 Vine reviews and 120,825 non-Vine reviews.

![Total Reviews](https://github.com/kntln/Amazon_Vine_Analysis/blob/main/images/total_reviews.png)

2. How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    - There were 220 5-star Vine review and 74,445 5-star non-Vine reviews.

![Paid Dataframe](https://github.com/kntln/Amazon_Vine_Analysis/blob/main/images/paid_df.png)

![Unpaid Dataframe](https://github.com/kntln/Amazon_Vine_Analysis/blob/main/images/unpaid_df.png)

3. What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
    - The percentage of Vine reviews that were 5-star are 44.27% while 61.61% of 5-star are from non-Vine reviews.

## Summary
The analysis suggests the absence of positivity bias for reviews in the Vine program. As shown in the results, the majority of 5-star reviews were from non-Vine (61.61%) compared to 44.27% 5-star reviews from Vine. Therefore, it can be concluded that having a paid Vine review is unlikely to make a difference in the percentage of 5-star reviews. To support this conclusion, an additional analysis is recommended. For instance, an analysis can be performed to determine the percentage of 5-star reviews and non 5-star reviews for Vine and non-Vine. The recommended analysis can provide a more detailed information for SellBy to determine if enrolling to the Vine program is worth the cost.