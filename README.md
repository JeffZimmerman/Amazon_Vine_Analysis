# Amazon_Vine_Analysis: Determining Bias of Paid Product Reviews

## Overview
This project utilized a dataset of Amazon reviews in the product category of "Tools" to examine the role of paid reviews in the Amazon Vine program, with the aim of idenitifying any bias toward favorable reviews from Vine members. PySpark was used to perform the ETL process, to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into PostgreSQL with PGAdmin.

## Results
The overall purpose was geared toward understanding whether it is worthwhile for a company to participate in the Vine program, as the fee associated with buying favorable reviews must be weighed against the value such reviews might represent. Paying for reviews can guarantee that a product will receive positive ratings, but customers who are genuinely satisfied with a product may write positive reviews without having to be paid to do so. 

* For the dataset for the "Tools" product category, there 285 reviews, and 31,545 unpaid reviews. 
* Of the 285 paid reviews, 163 were 5-star. Of the 31,545 unpaid reviews, 14,614 were 5-star.

** Paid Reviews
* 57% of the paid reviews had 5 stars, which seems low, and indicates that there is no guarantee that paying for reviews will produce consistently positive results.
<img width="461" alt="Screen Shot 2022-02-10 at 11 56 24 PM" src="https://user-images.githubusercontent.com/91562577/153539679-26e9304e-0d42-400a-bbbe-160cc68d5bef.png">
A sample of paid reviews shows a range of star ratings, with the majority receiving 4 stars or better:
<img width="979" alt="Screen Shot 2022-02-10 at 11 58 23 PM" src="https://user-images.githubusercontent.com/91562577/153539841-f548564b-4d4a-47dd-abc5-6b41e995f560.png">

** Unpaid Reviews
* 46% of unpaid reviews had 5 stars, which is lower than the rate for paid reviews, though not substantially so.
<img width="507" alt="Screen Shot 2022-02-11 at 12 02 26 AM" src="https://user-images.githubusercontent.com/91562577/153540121-91297b4c-3971-45ca-ad1d-fa41e0f994a3.png">
A sample of unpaid reviews also shows a range of star ratings, though in this sample 3 of the 10 received only 1 star:
<img width="978" alt="Screen Shot 2022-02-11 at 12 04 05 AM" src="https://user-images.githubusercontent.com/91562577/153540229-a40eb4dc-565d-4452-bcea-3ff53d6c4198.png">

## Conclusions
This project was able to confirm bias in paid product reviews in the "Tools" product category, which is not surprising. However, these paid reviewers did not uniformly offer high praise in the form of 5-star product reviews, and a substantial percentage of unpaid reviewers offered 5-stars withought needing to be compensated. 
Additional analysis would explore what kinds of guarantees Vine members agreed to in exchange for being paid, and whether there are other aspects of the reviews that offer additional value, such as the written length, inclusion of product images, or helpful insights. If a company is seeking these sorts of positive feedback, the relatively low rate of 5-star ratings may be offset somewhat.
Notably, the number of paid reviews in this product category was less than 1% of the overall number of reviews, so they could easily be missed among the large percentage that were unpaid. Nearly half of the unpaid reviews offered 5 stars, meaning that these 14,614 high assessments dwarfed the 163 5-star reviews that were paid, and for that matter the 285 paid reviews that produced any level of rating. This substantial imbalance in the number of paid vs unpaid reviews suggests that at these rates the Vine program is unlikely to produce positive results for companies in this product category. 
It may be worth paying for reviews only in cases where they can be made to stand out more prominently, whether by making up a larger percentage of the total, or by tilting the scales by being overwhelmingly positive among unpaid reviews that offer more negative assessments. But depending on the tone in which they are presented, such a difference might be too obvious and lead the consumer to view the paid reviews as untrustworthy. Further analysis might examine in more detail the ways that the reviews themselves are judged, such as by looking for correlations with the "helpful votes" as assessed by fellow customers.
