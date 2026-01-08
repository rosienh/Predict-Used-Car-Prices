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

---


# Technical Details

## Data Overview
- 12,000 records, 30+ vehicle attributes
- Target variable: Price
- Train-test split applied (80/20)

## Evaluation Metrics
- **Mean Squared Error (MSE)** measures price prediction error.
- **R² score** measured the proportion of price variation explained by the model.

## Data Preparation
- Performed **data preprocessing** (handling missing values, encoding categorical variables, and feature standardisation).
- **Log transformation** applied to **Price** to reduce skewness.
- **Feature selection** based on insights from exploratory analysis.
  
## Exploratory Data Analysis (EDA)
- Analysed price distribution and relationships between price and key vehicle attributes.
- Identified key price drivers, segment-level differences, and non-linear pricing behaviour.

<img width="977" height="573" alt="corealtion feature w price" src="https://github.com/user-attachments/assets/d8c817b1-0360-4aaa-a039-0c06944ccc45" />



<img width="718" height="668" alt="corelation matrix" src="https://github.com/user-attachments/assets/2ab35ec4-5ec2-4bf7-930d-1db6f96b6a66" />

## Insights from EDA

### Powerful Engines and Price Relation:
- Cars with more powerful engines, represented by higher values in horsepower, engine displacement, maximum torque, and power, are generally more expensive. This relationship suggests that engine specifications are a major contributor to a vehicle's market price.
- However, these performance attributes exhibit a strong negative correlation with fuel-efficiency metrics of more than -70%. Thus, while high-performance vehicles are priced higher, they tend to be less fuel-efficient.
  
### Torque and Power RPM Preferences:
- Moderate negative correlations exist between RPMs (for both power and torque) and price, indicating a consumer preference for vehicles that reach higher peak power and torque at lower RPMs.

### Mileage and Market Age Influence on Price:
- Cars with higher mileage tend to be less expensive, reflecting the typical depreciation associated with higher usage.
- Mileage shows a strong negative correlation with the year of the car's release, highlighting that newer vehicles command higher prices. This might present a preference for newer models, likely due to updated features, technology, or lower wear.


  
## Model Selection & Training
- Used linear regression as a diagnostic baseline and identified limitations of linear assumptions.
- Selected, trained, and compared three **non-linear ensemble regression** models:
   - Bagging Regressor
   - Random Forest Regressor
   - Stacked Regression (Bagging + Random Forest)
  
### Hyperparameter Tuning
- Tuned model hyperparameters using cross-validation to improve prediction accuracy and stability.

###Final Model Evaluation
- Compared model performance on unseen test data using MSE and R².
- Selected the final model based on overall accuracy and prediction stability.
