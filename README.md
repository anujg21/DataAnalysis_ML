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
    * The part of data preparation was dropping and replacing the NaN values from the data. 
    * Calculated the covariance and correlation matrices to find the relation between the characteristics. For example, it seems temperature and acceptance attributes have a relationship. More the temperature (in the '80s), the customers accepted more coupons.
    * I plotted the bar chart of the coupon distribution. Coffee House coupons were distributed more than any other coupons, and expensive restaurant coupons were the least circulated.
* Understanding the Bar coupons 
    * I created a new data frame where coupon is equal to Bar. I used this dataset in the subsequent analysis to determine the characteristics of the customers accepting the Bar coupons. 
    * The overall acceptance rate of the bar coupons is 41%. 
    * I analyzed the data of the frequent bar visitor to the infrequent visitors. 
        The % of Bar coupons accpeted those who went a bar 3 or fewer times - 81%
        The % of Bar coupons accpeted those who went more than 3 times - 18%
    * The acceptance rate is 69.5% for drivers who go to a bar more than once a month and are over the age of 25 compared to all others
    * There seems to be a high acceptance rate (71%) of the Bar coupon if passengers are other than kids and have occupations other than farming, fishing, or forestry.
    * The coupons were 72% likely to be accepted by customers under 30. 
    * The monthly salary does not considerably affect the Bar's decision-making. The acceptance rate was only 45%, even with the high monthly salary. 
    * In conclusion, the coupon distributors should target the audience of frequent bar visitor, passangers with no kids, and are under 30. 
* Understand the acceptance behavior of the cheap resturants (coupon is "Restaurant(<20))
    * I cleansed the data by replacing the NaN with the other existing values instead of dropping the NaN altogether, as the NaN contribution seemed less. 
    * From the analysis, it is clear that customers tend to accept restaurant coupons more likely during lunch and dinner. In the plot, you can see it between 2 pm and 6 pm.
    * Another contributing attribute is age - Ages between 21 t0 31 tend to be more likely to accept the coupons than the other age group.
    * Gender has no significant contribution. Males and females are equally to accept the coupons.
    * The weather was another compelling analysis, as customers likely accept the coupons during Sunny weather.
    * It seems there is slight possibility of 29% that the coupon less than 15 mins will be accepted. However, there is a good chance of 51% that coupons more than 25 mins away are to be rejected. Of course, driver won't prefer driving extra miles to use the resturant coupons. 
