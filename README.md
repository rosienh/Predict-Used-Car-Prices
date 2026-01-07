# Used Car Pricing Analysis

## Business Problem and Objective

Used-car pricing often relies on intuition and simple rules, which can lead to mispricing, particularly for high-value vehicles.

This project analyses approximately 12,000 used-car records with 30+ key vehicle attributes (such as age, mileage, engine size, and fuel type) to build a reliable pricing prediction model using Python, delivering consistent, data-driven price estimates to support sales team decision-making.


## Analytical Approach
**•	EDA & Feature Understanding**
Explored relationships between price and key vehicle attributes to understand pricing behaviour and identify important price drivers.

**•	Model Training & Selection**
Trained and compared three regression models (Bagging, Random Forest, and Stacked Regression), selecting the best-performing model based on price prediction accuracy using Mean Squared Error (MSE).

**•	Price Prediction & Transformation**
Predicted prices on unseen test data and applied a log transformation to stabilise price distribution and improve prediction consistency.


## Summary of Insight

### Key Price Drivers

Used-car prices are primarily driven by engine performance, vehicle age and mileage, and vehicle segment. Stronger engine specifications command price premiums, while mileage impacts price only when evaluated in the context of vehicle age. Different vehicle segments follow distinct pricing patterns rather than a single rule.


### Price Behaviour

Used-car pricing exhibits non-linear behaviour, meaning price does not change at a constant rate as vehicles age or accumulate mileage. Price differences are better interpreted as relative (percentage-based) changes rather than absolute dollar adjustments, especially across different price segments.

### Pricing Risk

Pricing risk is concentrated in high-value vehicles, where large prediction errors occur more frequently and carry significantly higher financial impact. Small percentage mispricing in this segment can result in disproportionately large losses.

## Decision Guidance (Recommendation)

## Deliverable & Impact
The project delivers a trained pricing prediction model supported by clear pricing insights and usage guidance, enabling more consistent pricing decisions and better risk awareness across sales and acquisition teams.
