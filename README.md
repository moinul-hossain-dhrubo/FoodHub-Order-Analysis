# FoodHub-Order_Analysis

## **Context**
The number of restaurants in New York is increasing day by day. Lots of students and busy professionals rely on those restaurants due to their hectic lifestyles. Online food delivery service is a great option for them. It provides them with good food from their favorite restaurants. A food aggregator company FoodHub offers access to multiple restaurants through a single smartphone app.

The app allows the restaurants to receive a direct online order from a customer. The app assigns a delivery person from the company to pick up the order after it is confirmed by the restaurant. The delivery person then uses the map to reach the restaurant and waits for the food package. Once the food package is handed over to the delivery person, he/she confirms the pick-up in the app and travels to the customer's location to deliver the food. The delivery person confirms the drop-off in the app after delivering the food package to the customer. The customer can rate the order in the app. The food aggregator earns money by collecting a fixed margin of the delivery order from the restaurants.

## **Objective**
The food aggregator company has stored the data of the different orders made by the registered customers in their online portal. They want to analyze the data to get a fair idea about the demand of different restaurants which will help them in enhancing their customer experience. Suppose you are hired as a Data Scientist in this company and the Data Science team has shared some of the key questions that need to be answered. Perform the data analysis to find answers to these questions that will help the company to improve the business.

## **Data Description**
The data contains the different data related to a food order. The detailed data dictionary is given below.

## **Data Dictionary**
order_id: Unique ID of the order
customer_id: ID of the customer who ordered the food
restaurant_name: Name of the restaurant
cuisine_type: Cuisine ordered by the customer
cost: Cost of the order
day_of_the_week: Indicates whether the order is placed on a weekday or weekend (The weekday is from Monday to Friday and the weekend is Saturday and Sunday)
rating: Rating given by the customer out of 5
food_preparation_time: Time (in minutes) taken by the restaurant to prepare the food. This is calculated by taking the difference between the timestamps of the restaurant's order confirmation and the delivery person's pick-up confirmation.
delivery_time: Time (in minutes) taken by the delivery person to deliver the food package. This is calculated by taking the difference between the timestamps of the delivery person's pick-up confirmation and drop-off information

## **Conclusions:**
1. We have five numerical features and four categorical features. The dataset doesn't have any missing data and there are no outliers in the numerical features.

2. Order costs range from 4.47 dollars to 35.41 dollars, with a mean of 16.50 and a standard deviation of 7.48. The distribution is skewed towards right.

3. Food preparation time range from 20 minutes to 35 minutes, with a mean of 27.37 and a standard deviation of 4.63. The distribution of the food preparation time is roughly uniform.

4. Delivery time range from 15 minutes to 33 minutes, with a mean of 24.16 and a standard deviation of 4.97. The delivery time column distribution is skewed to the left.

5. The majority of customares (38.78%) did not provide rating. 30.98% customers given a 5-star rating, followed by 9.91% and 20.34% for 3 and 4 stars, respectively.

6. Orders came from 148 unique restaurants serving 14 different cuisines.

7. The majority of clients ordered items from the following cuisines, accounting for 82.56% of all orders: American (30.77%), Japanese (24.76%), Italian (15.70%), and Chinese (11.33%).Additionally, these four cuisines—American (30.44%), Japanese (24.47%), Italian (15.62%), and Chinese (11.19%)—contributed 81.72% of the total revenue generated.

<img src = "cuisine_type_count.png" width=800 height=400>

9. People are much more likely to order meals online on the weekends than on weekdays, as indicated by the fact that 71.18% of orders were placed on the weekends compared to 28.82% on weekdays.

<img src = "count_days_of_the_week.png" width=800 height=400>

11. The majority of customares (38.78%) did not provide rating. 30.98% customers given a 5-star rating, followed by 9.91% and 20.34% for 3 and 4 stars, respectively.

<img src = "rating_count.png" width=800 height=400>

13. Top five resturants in terms of receiving orders with percentage : Shake Shack (11.54%), The Meatball Shop(6.95%), Blue Ribbon Sushi(6.27%), Blue Ribbon Fried Chicken (5.06%), Parm has (3.58%).

<img src = "top_restaurants.png" width=800 height=400>

15. The average number of orders was lower for the cuisines with higher order costs and vice-versa.

16. Weekdays have a considerably greater mean delivery time (28.34) than weekends (22.47) as well as their median (28 on weekdays, 22 on weekends)
<img src = "delivery_time_difference.png" width=800 height=400>

## **Recommendations:**
Encourage Customers to give Ratings/Feedback: Apply strategies to get more ratings from individuals. For instance, specific reward points for rating items. Positive reviews can boost the reputation of the restaurant and attract more customers. In addtion, It will provide a better understanding of the orders.

Promotional offers : Offering promotional deals from restaurants with poor sales can boost sales.

Weekday Promotions : Running special promotional campaigns on weekdays can boost sales because individuals often place fewer orders on such days. Specifically, run the campaigns focusing popular cuisines on weekdays.

Improve Delivery Time : On weekdays, concentrate on reducing delivery times. Find the main causes of delivery taking longer throughout the week than on the weekend and then take necessary steps. e.g. Perhaps the delivery person doesn't think it's worthwhile to make deliveries during the workdays and that's causing lack of delivery persons which ultimately causes the delay. Maybe a third party delivery service can resolve this issue.

Imply Loyalty programs : Implement loyalty programs, special offers, or other incentives for returning customers. To keep them coming back, interact with your customers through customized campaigns.

Reconstruct menus: Try looking through their menu to see if it's expensive because the cuisines with the highest order costs have the fewest orders overall.Try offering discounts on those cuisines to see if the high price is the issue or if people simply don't like them. Or maybe some resturant has a minimum order cost requirement which are causing customer dissatisfaction.

Monitor changes based on data : Try to measure the change after implementing solutions to see whether they are truly effective. Hypotheses testing(e.g. t-test,chi-squared test, ANOVA test etc.) can be a useful way to evaluate differences.
