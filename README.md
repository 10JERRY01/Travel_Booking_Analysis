# Travel_Booking_Analysis
# Project Overview
## Objective:
To analyze customer behavior and predict churn in a travel booking dataset. The analysis will help identify patterns leading to churn and recommend strategies to improve customer retention.

## Dataset Description
The dataset contains information about customers’ booking habits. It includes the following columns:

Field	Description	Data Type
profile_id	Unique identifier for each customer.	Integer
Primary_sales_product_type	Type of product purchased (e.g., FLIGHT, HOTEL, TRAIN, TRIP).	Categorical
first_booking_time	Timestamp of the first booking in milliseconds.	Timestamp
last_booking_time	Timestamp of the last booking in milliseconds.	Timestamp
avg_booking_invoice_amount_idr	Average invoice amount for bookings in Indonesian Rupiah (IDR).	Numeric
count_booking	Total number of bookings made by the customer.	Integer
Target Variable:
churn: A binary indicator where:

1 indicates churn (no bookings in the last year from the dataset's reference date).
0 indicates active customers.

## Project Workflow
Step 1: Data Loading and Exploration
Load the dataset and inspect the structure.
Handle missing or inconsistent data.
Analyze the distribution of key features and relationships between variables.
Step 2: Feature Engineering
Derived Features:
Customer Tenure: Difference between the first and last booking times.
Recency: Days since the last booking compared to the dataset's reference date.
Categorical Encoding:
Encode Primary_sales_product_type using LabelEncoder.
Step 3: Data Preprocessing
Handle missing values.
Normalize numerical features using StandardScaler.
Split the data into training and testing sets (e.g., 70% training, 30% testing).
Step 4: Model Training
Selected Model: Random Forest Classifier.
Train the model on the training set using features such as booking frequency, invoice amounts, tenure, and recency.
Step 5: Model Evaluation
Evaluate model performance using:
Accuracy
Precision, Recall, F1-Score
Confusion Matrix
Visualize the results to identify areas for improvement.
Step 6: Feature Importance Analysis
Identify the most important features driving churn predictions, e.g., recency or average invoice amount.
Step 7: Recommendations
Develop actionable strategies to reduce churn based on insights from the model.
Step 8: Deployment
Save the model for deployment using joblib.
Provide a user-friendly interface for predicting churn on new customer data.

## Key Insights and Visualizations
Average Booking Amount by Churn Status
Bar chart showing differences in average invoice amounts for churned and active customers.

## Booking Frequency Analysis
Visualization of total bookings grouped by product type and churn status.

## Feature Importance
A bar plot highlighting features like recency and tenure that significantly impact churn.

## Dashboard
Overview
An interactive dashboard was created using Plotly and Dash. The dashboard includes:

Churn Statistics: Summary of churn rates by product type.
Visualizations:
Average booking amounts.
Total bookings by status.
Predictive Model Insights: Feature importance and churn prediction results.

## Recommendations Based on the analysis:

Target Customers with High Recency:

Offer discounts or loyalty rewards to engage recent customers who haven't booked in the last year.
Focus on Low-Tenure Customers:

Design onboarding campaigns to increase engagement and encourage repeat bookings.
Monitor High-Invoice Customers:

Provide personalized offers for customers with high average booking amounts to maintain their loyalty.

## Future Enhancements
Incorporate additional data, such as demographic or marketing campaign information.
Explore advanced models like Gradient Boosting or Neural Networks for improved predictions.
Implement A/B testing to evaluate the effectiveness of churn reduction strategies.

## Conclusion
This project effectively demonstrates how data analysis and machine learning can predict and mitigate customer churn in the travel industry. By identifying key drivers of churn, businesses can implement targeted strategies to enhance customer retention.
