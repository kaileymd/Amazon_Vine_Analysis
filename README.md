# Amazon Vine Paid Reviews Analysis
The Amazon Vine program is a service where companies can pay a small fee for Amazon to provide their products to program members, who are then required to publish a review. When money is invovled there is always a potential for bias - so does this program create biased, favorable reviews? This analysis will be performed on a randomly selected database of [Amazon Review datasets](https://s3.amazonaws.com/amazon-reviews-pds/tsv/index.txt). The selected database is Video Games.

### Results
To narrow down our data set to reviews that are more influential, we transformed the data to only include reviews with more than 20 votes and an indicator that more than 50% of those voters thought the review was helpful. 

![paid_summary.png](https://github.com/kaileymd/Amazon_Vine_Analysis/blob/main/Images/paid_summary.png)

![unpaid_summary.png](https://github.com/kaileymd/Amazon_Vine_Analysis/blob/main/Images/unpaid_summary.png)

### Summary

The percentages (51% vs. 39%) would indicate that there is a favor bias amongst Amazon Vine reviewers, however, the sheer difference in the number of paid reviews as opposed to unpaid reviews (94 vs. 40,471) would suggest that these reviews aren't dramatically changing the rating of any product. 

To verify, I would join the review_id_table (also created in the data extraction portion of this analysis) to make sure that these reviews aren't a significant portion of any one product's review count and therefore skewing its rating upwards. Additionally, I would recommend graphing the distribution of paid vs. unpaid star ratings to get the bigger picture on any potential differences.
