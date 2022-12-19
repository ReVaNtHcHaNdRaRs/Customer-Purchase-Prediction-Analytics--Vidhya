# Customer-Purchase-Prediction-Analytics--Vidhya
This Hackathon was conducted by American Express in collabation with Analytics Vidhya


## Problem Statement
We are given information about customers and their purchases till now. Given this information, we have to predict what products the customers might be in next 6 months 


## Approach
1. The columns Product_Holding_B1 and Product_Holding_B2 are converted into one hot columns as the these features are list of products.
2. Created new features like count_of_current_product, and converted discrete columns like age and vintage to categorical
3. Used count based label encoding technique and one hot encoding technique to convert categorical features into numerical features
4. Trained the dataset after scaling using logistc regression and the top products are sorted based on the distance from predicted probability and decison cutoff for all the products. A cutoff vector which maximizes ROC AUC has been calculated for it and the product which is farthest from cutoff has been given first preference.
5. Since we need to predict top 3 probable products,  the list is truncated to a maximum size of 3 to create the final output


## Data
| Column              | Description                                                       |
| ------------------- | ----------------------------------------------------------------- |
| Customer_ID         | unique identification of customer                                 |
| Gender              | Gender of customer                                                |
| Age                 | Age of customer in Years                                          |
| Vintage             | No. of months customer has been active                            |
| Is_Active           | whether a customer is active or not                               |
| City_Category       | City category of the customer                                     |
| Customer_Category   | Category of the customer                                          |
| Product_Holding_B1  | List of products owned by the customer now                        |
| Product_Holding_B2  | List of products owned by the customer in the future- 6 months    |


