# Amazon_Vine_Analysis

## Background

Since your work with Jennifer on the SellBy project was so successful, you’ve been tasked with another, larger project: analyzing Amazon reviews written by members of the paid Amazon Vine program. The Amazon Vine program is a service that allows manufacturers and publishers to receive reviews for their products. Companies like SellBy pay a small fee to Amazon and provide products to Amazon Vine members, who are then required to publish a review.

In this project, you’ll have access to approximately 50 datasets. Each one contains reviews of a specific product, from clothing apparel to wireless products. You’ll need to pick one of these datasets and use PySpark to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Next, you’ll use PySpark, Pandas, or SQL to determine if there is any bias toward favorable reviews from Vine members in your dataset. Then, you’ll write a summary of the analysis for Jennifer to submit to the SellBy stakeholders.

## Results

- How many Vine reviews and non-Vine reviews were there?

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/total_reviews.png)

  There were a total of 40565 reviews.

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/total_paid_reviews.png)

  There were a total of 94 Vine reviews.

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/total_non_paid.png)

  There were a total of 40471 non-Vine reviews.

- How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/total_five_reviews.png)

  There were a total of 15711 5 star reviews.

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/total_paid_five_reviews.png)

  There were a total of 48 Vine 5 star reviews.

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/total_five_unpaid.png)

  There were a total of 15663 non-Vine 5 star reviews.

- What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?

  The percent of Vine reviews that are 5 stars are:

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/percent_paid_five.png)

  51.06% of all Vine reviews were 5 stars

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/percent_five_paid.png)

  0.31% of all 5 star reviews were Vine reviews

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/percent_five_paid_total_reviews.png)

  0.12% of all reviews (both Vine, non-Vine) were 5 star Vine reviews

  
  The percent of non-Vine reviews are 5 star are:

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/percent_unpaid_five.png)

  99.69% of all 5 star reviews are non-Vine

  ![](https://github.com/labinskin/Amazon_Vine_Analysis/blob/main/Resources/percent_unpaid_five_total.png)

  38.61% of all reviews are 5 star non-Vine reviews

## Summary

There does appear to be a slight positivity bias in the Vine program. Over half of the Vine reviews, 48 of 94 (51.06%), were five star reviews. This is a higher percentage of five star reviews compared to non-Vine reviews. Non-Vine 5 star reviews were 38.61% of the total number of reviews. Vine reviewers were about 12-13% more likely to post a 5 star review. However, there should be some caution here, as there was a sample size of only 94 Vine reviews in total, compared to 40,471 non-Vine reviews. More data, with a larger sample size is needed to determine if there is a Vine bias. A little bit more evidence to back this up is that 99.69% of all 5 star reviews were non-Vine, but again the sample size comes into effect here. More data on Vine is needed. With there being more links to more Amazon datasets out there, a larger aggregate of all Vine reviews, across all the different platforms, datasets, and reviews is needed to determine with stronger confidence whether or not there is a positivity bias with the Vine program. Additionally, if we were going to only to continue using this dataset, we could examine the four, three, two, and one star reviews and compare the percentages. But again, the best way to test this slight Vine positivity bias is to include more datasets.
