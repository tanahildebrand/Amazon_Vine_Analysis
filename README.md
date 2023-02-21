# Amazon Vine Analysis

## Overview of the Analysis
The Amazon Vine program is a paid service to generate product reviews. I analyzed a dataset specific to Grocery products, provided by Amazon, which includes data for both paid (Vine) and non-paid reviews. Using PySpark I completed the ETL process, connect to an AWS RDS instance, and loaded the data into pgAdmin.

I then analyzed the data to determine if there is bias toward favorable reviews if the review was part of the Vine program. The starter data was filtered to products with more than 20 votes and % of helpful votes greater than 50%.

## Results
![Vine Summary](/Images/Vine_Summary.png)
  - How many Vine reviews and non-Vine reviews were there?
    - There were 56 Vine reviews and 26,299 non-Vine reviews for grocery products.
  - How many Vine reviews were 5 stars? How many non-Vine reviews were 5 stars?
    - There were 18 5-star Vine reviews, and 14,616 5-star non-Vine reviews.
  - What percentage of Vine reviews were 5 stars? What percentage of non-Vine reviews were 5 stars?
    - Vine 5-star reviews accounted for 32% of total Vine reviews. Non-Vine 5-star reviews accounted or 56% of total non-Vine reviews.

## Summary
Given that a higher percentage of products were given a 5-star review for non-Vine (56%) compared to Vine (32%), I do not see a bias to review a product favorably because it's part of the paid program.

Additionally, I would want to limit the dataset to only those reviews with a verified purchase of the product. I believe this would eliminate the possibility that rewiews are being given for products that were not actually purchased. Eliminating this data would remove the possibility that non-Vine reviews are being given to purposely raise the overall product star ranking.
