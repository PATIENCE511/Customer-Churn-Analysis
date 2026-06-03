# Customer-Churn-Analysis
## This project analyzes customer churn patterns for FinServe Bank using Power BI.
The objective was to identify customer segments with the highest risk of churn, assess potential revenue loss, and provide data-driven recommendations to improve customer retention.
The dashboard was built using Power BI, DAX, Power Query, and data modeling techniques.
## Dashboard Preview
<img width="1277" height="730" alt="Screenshot 2026-06-03 152559" src="https://github.com/user-attachments/assets/9bb991b2-77af-4564-bd63-ad90f9c68b25" />
## Business Problem
Customer retention is a critical challenge in the banking industry.

FinServe Bank observed a customer churn rate of 20.37%, indicating that approximately one out of every five customers leaves the bank.

The business needed a solution to:
- Identify high-risk customer segments
- Understand factors driving customer churn
- Measure revenue exposure from churn
- Support data-driven retention strategies

## Project Objectives

The project aimed to:

1. Identify customer segments with the highest churn rates.
2. Analyze churn across geography, age groups, tenure categories, and credit ratings.
3. Measure revenue risk associated with churned customers.
4. Develop an interactive dashboard for business decision-making.
5. Provide actionable recommendations to improve customer retention.

## Dataset Information

Source: Kaggle Customer Churn Dataset

Records: 10,000 Customers

Key Features:

- Customer ID
- Geography
- Gender
- Age
- Credit Score
- Tenure
- Balance
- Number of Products
- Credit Card Status
- Active Member Status
- Estimated Salary
- Churn Status

## Dataset Information

Source: Kaggle Customer Churn Dataset

Records: 10,000 Customers

Key Features:

- Customer ID
- Geography
- Gender
- Age
- Credit Score
- Tenure
- Balance
- Number of Products
- Credit Card Status
- Active Member Status
- Estimated Salary
- Churn Status
  

## DAX Measures

The dashboard uses custom DAX measures to calculate business metrics.
* Total customer =COUNTROWS(Churn_dataset)
Churn Rate =DIVIDE(
    CALCULATE(
        [Total customer],
        Churn_dataset[Exited]=1
    ),
    [Total customer],
    0
)
* Retention = 1 - [Churn Rate]

* Revenue Risk =DIVIDE(
    [High risk Revenue],
    CALCULATE(
        SUM(Churn_dataset[Balance]),
        Churn_dataset[Exited]=0
    )
)

## Dashboard Preview
<img width="1277" height="730" alt="Screenshot 2026-06-03 152559" src="https://github.com/user-attachments/assets/9bb991b2-77af-4564-bd63-ad90f9c68b25" />
## Dashboard Features

The dashboard includes:

- KPI Cards
- Decomposition Trees
- Slicers
- Stacked Bar Charts
- Donut Charts
- Interactive Filtering

Users can analyze churn by:

- Geography
- Age Group
- Credit Category
- Gender
- Tenure Category

## Key Performance Indicators
KPI	Value
- Total Customers	10,000
- Churn Rate	20.37%
- Retention Rate	79.63%
- Revenue Risk	23.82%

## Key Insights
1. Customer Attrition Remains a Significant Business Challenge
The analysis revealed an overall churn rate of 20.37%, indicating that approximately one in five customers has left the bank. This highlights a substantial customer retention challenge with potential implications for long-term revenue growth and customer acquisition costs.

2. Germany Exhibits the Highest Churn Concentration
Among all geographic markets analyzed, Germany recorded the highest churn rate at 32.44%, significantly exceeding France and Spain. This suggests that customer retention issues are disproportionately concentrated within the German market and warrant further business investigation.

3. Older Customers Represent the Highest-Risk Segment
Customer churn increases considerably with age. The Old customer segment recorded a churn rate of 55.21%, making it the most vulnerable demographic group within the customer base. This finding suggests that age-related factors may be influencing customer retention outcomes.

4. Revenue Exposure Extends Beyond Customer Loss
The dashboard identified a Revenue Risk of 23.82%, indicating that a notable proportion of customer value is associated with customers who eventually churned. This demonstrates that churn is not only a customer retention issue but also a direct financial risk to the business.

5. Credit Profile Appears to Influence Retention Behaviour
Customers within lower credit-score categories exhibited stronger churn tendencies compared to other customer groups. This pattern suggests a potential relationship between credit profile, product accessibility, and customer loyalty.

6. Customer Distribution Is Relatively Balanced Across Tenure Segments
Analysis of tenure categories showed a fairly even distribution between New_bie, Regular, and Loyal customers. While this provides a useful view of customer composition, additional churn analysis by tenure would provide deeper insights into customer lifecycle behaviour.

## Recommendations
1. Focus Retention Initiatives on the German Market
Given its significantly higher churn rate, Germany should be prioritized for customer retention efforts. Further analysis should be conducted to identify market-specific drivers contributing to customer attrition.

2. Strengthen Engagement Strategies for Older Customers
The elevated churn rate among older customers suggests the need for tailored retention initiatives. Personalized support, improved customer communication, and simplified service experiences may help improve retention within this segment.

3. Prioritize High-Value Customer Retention
Customer retention strategies should focus not only on reducing churn volume but also on protecting high-value customers who contribute significantly to overall revenue and account balances.

4. Review Customer Experience for Lower Credit Segments
The business should assess whether product offerings, lending policies, or service limitations are contributing to churn among customers with lower credit profiles and identify opportunities to improve customer satisfaction.

5. Enhance Dashboard Monitoring Capabilities
Future dashboard iterations should incorporate churn analysis by tenure category, customer lifetime value metrics, and predictive analytics to support more proactive retention planning.

6. Establish Ongoing Churn Performance Monitoring
The dashboard should serve as a continuous decision-support tool, enabling stakeholders to monitor churn trends, evaluate retention initiatives, and make data-driven business decisions based on evolving customer behaviour.

## Future Improvements
- Build a machine learning churn prediction model.
- Add customer lifetime value (CLV) metrics.
- Create real-time reporting.
- Add churn analysis by tenure category.
- Integrate automated retention alerts.

## Skills Demonstrated

- Power BI
- Power Query
- DAX
- Data Modeling
- Data Cleaning
- Customer Analytics
- Churn Analysis
- Dashboard Design
- Data Visualization
- Business Intelligence
- Business Reporting

  ## Author

Patience Ugwu

Data Analyst

### Connect With Me

Email: ugwup3100@gmail.com
