# Used Car Pricing Analysis

## Business Problem and Objective

This project analyses approximately **12,000 used-car records with 30+ key vehicle attributes** (such as age, mileage, engine size, and fuel type) to **build a reliable pricing prediction model** using Python, delivering consistent, data-driven price estimates to support sales team decision-making.


## Analytical Approach

### EDA & Feature Understanding
•	Explored relationships between price and key vehicle attributes to understand pricing behaviour and identify important price drivers.

### Model Training & Selection
•	Trained and compared three regression models (Bagging, Random Forest, and Stacked Regression), selecting the best-performing model based on price prediction accuracy using Mean Squared Error (MSE).

### Price Prediction & Transformation
•	Predicted prices on unseen test data and applied a log transformation to stabilise price distribution and improve prediction consistency.


## Summary of Insight

### Key Price Drivers:

•	Used-car prices are mainly driven by engine performance, vehicle age and mileage, and vehicle segment. Performance commands price premiums, while mileage only matters when considered alongside vehicle age.


### Price Behaviour:

•	Used-car prices do not change at a constant rate over time. Price movements are better understood as percentage-based changes rather than fixed dollar amounts, especially across different price segments.


### Pricing Risk:

•	Pricing risk is highest in high-value vehicles, where small pricing errors can lead to disproportionately large financial losses.


## Recommendation

•	Prioritise **engine performance** and evaluate **mileage** in the context of vehicle age and segment.

•	Evaluate price changes as **proportional (percentage-based)** movements to better reflect how vehicles lose value over time.

•	Apply closer pricing review to **high-value vehicles**, where small pricing errors can have the largest financial impact.



## Deliverable & Impact
The project delivers a trained pricing prediction model supported by clear pricing insights and usage guidance, enabling more consistent pricing decisions and better risk awareness across sales and acquisition teams.
