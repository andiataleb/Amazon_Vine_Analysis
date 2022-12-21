# Amazon_Vine_Analysis

##Overview

In this project, I worked on analyzing Amazon reviews written by the members of a paid program called Amazon Vine. The purpose of this analysis is to determine if paid reviewers are more likely and more biased to give a 5-satr review to the products compared to non paid reviewers. 
Some companies pay a small fee to Amazon to send their products to the members of this group to write a review for their products.
PySpark was used to perform the ETL process to extract the dataset, transform the data, connect to an AWS RDS instance, and load the transformed data into pgAdmin. Then, by using the PySpark, the bias toward 5-star reviews form the Vine member groups was determined.

##Results

The result of my analysis on the bias of the Vine members reviews are as follow:
After narrowing down all the votes to rows with vote counts of 20 or greater in order to pick more helpful reviews, I filtered these to retrieve the rows where more than 50% of the votes are helpful. From there, separated the Vine members from non-Vine members and retrieved the rows with 5-star reviews for each group and calculated the percentage of 5-star reviews for Vine members and non Vine members to see if there is a positive bias in the Vine members group. 
- There are a total number of 104 Vine member reviews and 65275 reviews from the non-member group. 
- For the Vine member group reviews, 48 of them were 5-star and from the non-Vine member group 20439 reviews were 5-star. 
- This means 46.1% of the Vine-member reviews were 5-star compared to the 31.3% in the non-member group. 


![](/Images/1.png)


![](/Images/2.png)


##Summary

The results are showing about 15% of positivity bias for reviews in the Vine program. However, the total number of the votes in the Vine program are significantly lower compared to the non-member group. My recommendation is to study other groups of reviews and compare them for the same positivity bias to see if this is a trend that repeats in other groups as well. 

