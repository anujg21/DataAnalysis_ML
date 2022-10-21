# Driving Coupon Analysis #
***The repository consists the analysis of customers to accept or reject the driving coupons***

#### About the data ####  
***(data/coupon.csv)***
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, passenger, etc., and then asks people whether they will accept the coupon if they are the driver. Answers given that the users will drive there “right away” or “later before the coupon expires” are labeled as “Y = 1”, and answers “no, I do not want the coupon” are labeled as “Y = 0”. There are five different types of coupons—less expensive restaurants (under $20), coffee houses, carry out and take away, bars, and more expensive restaurants ($20–$50).

#### About the analysis ####  
***CouponAnalysis-Oct2022.ipynb***
* There are six phases in the CRISP-DM data science lifecycle. Business Understaning (find the acceptance rate of the driving coupons), Data Understanding and Data preparing (we will do the subsequent steps), Data modeling & Evaluation and Deployment (at this moment, aren't needed for this analysis)
* Data Understanding 
    * Is executed by understanding the type of data, columns, and any bad data (NaN, Null). It was further analysed by finding the correlation and Covariance matrix between the data. 
    * The part of data prepation was done by dropping and replacing the NaN values from the data.
