# practical-application-5.1

## Problem statement: Will the Customer Accept the Coupon?
### Context
Imagine driving through town and a coupon is delivered to your cell phone for a restaurant near where you are driving. Would you accept that coupon and take a short detour to the restaurant? Would you accept the coupon but use it on a subsequent trip? Would you ignore the coupon entirely? What if the coupon was for a bar instead of a restaurant? What about a coffee house? Would you accept a bar coupon with a minor passenger in the car? What about if it was just you and your partner in the car? Would weather impact the rate of acceptance? What about the time of day?
Obviously, proximity to the business is a factor on whether the coupon is delivered to the driver or not, but what are the factors that determine whether a driver accepts the coupon once it is delivered to them? How would you determine whether a driver is likely to accept a coupon?
Overview
The goal of this project is to use what you know about visualizations and probability distributions to distinguish between customers who accepted a driving coupon versus those that did not.
Data
This data comes to us from the UCI Machine Learning repository and was collected via a survey on Amazon Mechanical Turk. The survey describes different driving scenarios including the destination, current time, weather, passenger, etc., and then ask the person whether he will accept the coupon if he is the driver. Answers that the user will drive there ‘right away’ or ‘later before the coupon expires’ are labeled as ‘Y = 1’ and answers ‘no, I do not want the coupon’ are labeled as ‘Y = 0’. There are five different types of coupons -- less expensive restaurants (under 20), coffee houses, carry out & take away, bar, and more expensive restaurants (20 - $50).

### Data Description
Keep in mind that these values mentioned below are average values.
The attributes of this data set include:
#### 1. User attributes
    * Gender: male, female
    * Age: below 21, 21 to 25, 26 to 30, etc.
    * Marital Status: single, married partner, unmarried partner, or widowed
    * Number of children: 0, 1, or more than 1
    * Education: high school, bachelors degree, associates degree, or graduate degree
    * Occupation: architecture & engineering, business & financial, etc.
    * Annual income: less than $12500, $12500 - $24999, $25000 - $37499, etc.
    * Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    * Number of times that he/she buys takeaway food: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    * Number of times that he/she goes to a coffee house: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    * Number of times that he/she eats at a restaurant with average expense less than $20 per person: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
    * Number of times that he/she goes to a bar: 0, less than 1, 1 to 3, 4 to 8 or greater than 8
#### 2. Contextual attributes
    * Driving destination: home, work, or no urgent destination
    * Location of user, coupon and destination: we provide a map to show the geographical location of the user, destination, and the venue, and we mark the distance between each two places with time of driving. The user can see whether the venue is in the same direction as the destination.
    * Weather: sunny, rainy, or snowy
    * Temperature: 30F, 55F, or 80F
    * Time: 10AM, 2PM, or 6PM
    * Passenger: alone, partner, kid(s), or friend(s)
#### 3. Coupon attributes
    * time before it expires: 2 hours or one day

### Coupon Acceptance Analysis:

#### The proportion of the total observations choose to accept the coupon is : 0.5684326710816777

#### The proportion of bar coupons accepted is: 0.41001487357461575
 
##### Based on the observations made above we can hypothesize following about the drivers who accepted the bar coupon.
Drivers who accepted have following characteristics.
* They went to bar more than once a month
* They are over the age of 25
* They are not with a kid passenger
* They are not widowed
* They go to cheap restaurants more than 4 times a month
* Their income is less than 50k
In summary, the coupon should be offered to the audience satisfying the above mentioned criteria that indicates highter acceptence.

#### The proportion of Restaurant20To50 coupons accepted is: 0.4410187667560322
##### Based on the observations made above we can hypothesize following about the drivers who accepted the Restaurant20To50 coupon.
Drivers who accepted have following characteristics.
* The top 4 values of income range reported were - $100000 or More, $50000 - $62499, $25000 - $37499, $37500 - $49999
* The highest proportion of 'Restaurant20To50' column was captured by less1 and 1~3 values
* Among the drivers who accepted following age groups were part of the higher proportion in the overall age distribution - 31,21 and 26, where as gender of the drivers is not affecting coupon acceptance rate significantly.
* Among the drivers who accepted 81% were opposite direction
* The top 7 occupations were - Computer & Mathematical, Unemployed, Student, Sales & Related, Office & Administrative Support, Education&Training&Library, and Management
