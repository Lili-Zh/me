Readme
Link: https://github.com/Lili-Zh/me/blob/main/Will%20the%20Customer%20Accept%20the%20Coupon.ipynb

This is a summary of findings on the data analysis: Will the Customer Accept the Coupon?

Data
This data is from the UCI Machine Learning Repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios, including the destination, current time, weather, and passenger, and then asks people whether they will accept the coupon if they are the driver. There are three possible answers people can choose from:
•	“Right away”
•	“Later, before the coupon expires”
•	“No, I do not want the coupon”
The first two responses are labeled as “Y = 1,” and the third is labeled as “Y = 0.” There are five different types of coupons: Less expensive restaurants (under $20), coffee houses, carryout and takeaway, bars, and more expensive restaurants ($20–$50).

Findings:
Across all coupon types and all drivers who participated in this survey, approximately 56.84% would accept the coupon.
Bar coupon findings:
Regarding bar coupons, approximately 41% of drivers would accept them.
•	Drivers who visit bars more than three times a month are more likely to accept bar coupons compared to those who go three or fewer times (76.88% vs. 52.74%).
•	Drivers aged 25 and above who visit bars more than once a month tend to accept the coupon at a rate of 67.16%.
•	Social drivers without children, who visit bars more than once a month and do not work in farming, fishing, or forestry, are significantly more likely to accept bar coupons than others (68.79% vs. 29.35%).
•	Younger frequent bar-goers (<30) show moderate interest in bar coupons, with about 40% of those who visit bars more than once a month accepting them.
•	Cost-conscious drivers earning under $50K annually and frequenting low-cost restaurants (4+ times/month) demonstrate a higher acceptance rate for bar coupons.
•	However, drivers who go to bars more than once a month, have non-kid passengers, and are not widowed tend not to accept the coupons.

Independent investigation findings:
I explored the more expensive restaurant ($20-$50) coupon group, where the overall acceptance rate is 44.10%.
•	Drivers who visit expensive restaurants more than three times a month are slightly more likely to accept coupons than those who dine out less frequently (47.59% vs. 44.14%).
•	There is no significant difference in acceptance rates between drivers who visit expensive restaurants more than once a month and are over 25 years old compared to others (43.48% vs. 44.12%).
•	Drivers who frequent expensive restaurants, have no kid passengers, and do not work in farming, fishing, or forestry show a higher acceptance rate than other drivers (47.45% vs. 42.65%).
•	Similar to the bar coupon group, drivers who go to more expensive restaurants more than once a month, have non-kid passengers, and are not widowed tend not to accept coupons for more expensive restaurants.
•	Younger drivers (<30) who frequently visit expensive restaurants are the most likely to accept coupons, with an acceptance rate of 56.25%.
•	Nearly half (46.89%) of cost-conscious drivers who earn under $50K annually and frequently visit cheaper restaurants would accept coupons for more expensive restaurants.
