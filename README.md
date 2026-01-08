# Used Car Pricing Analysis

## Business Problem and Objective

This project analyses approximately **12,000 used-car records with 30+ key vehicle attributes** (such as age, mileage, engine size, and fuel type) to **build a reliable pricing prediction model** using Python, delivering consistent, data-driven price estimates to support sales team decision-making.


## Analytical Approach

### EDA & Feature Understanding
•	Explored relationships between **price** and **key vehicle attributes** to understand **pricing behaviour** and identify important price drivers.

### Model Training & Selection
•	Trained and compared **three regression models (Bagging, Random Forest, and Stacked Regression)**, selecting the best-performing model based on price prediction accuracy using Mean Squared Error (MSE).

### Price Prediction & Transformation
•	Predicted prices on unseen test data and applied a log transformation to stabilise price distribution and improve prediction consistency.


## Summary of Insight

### Key Price Drivers:

•	Used-car prices are mainly driven by **engine performance, vehicle age and mileage, and vehicle segment**. Performance commands price premiums, while mileage only matters when considered in conjunction with vehicle age.


### Price Behaviour:

•	Used-car prices do not change at a constant rate over time. Price movements are better understood as **percentage-based changes** rather than fixed dollar amounts, especially across different price segments.


### Pricing Risk:

•	Pricing risk is **highest in high-value vehicles**, where small pricing errors can lead to disproportionately large financial losses.


## Recommendation

•	Prioritise **engine performance** and evaluate **mileage** in the context of vehicle age and segment.

•	Evaluate price changes as **proportional (percentage-based)** movements to better reflect how vehicles lose value over time.

•	Apply closer pricing review to **high-value vehicles**, where small pricing errors can have the largest financial impact.



## Deliverable & Impact
The project delivers a trained pricing prediction model, supported by clear pricing insights and usage guidance, enabling more consistent pricing decisions and improved risk awareness across sales teams.

---


# Technical Details

## Data Overview
- 12,000 records, 30+ vehicle attributes
- Target variable: **Price**
- Train-test split applied (80/20)

## Evaluation Metrics
- **Mean Squared Error (MSE)** measures price prediction error.
- **R² score** measured the proportion of price variation explained by the model.

## Data Preparation
- Performed **data preprocessing** (handling missing values, encoding categorical variables, and feature standardisation).
- **Log transformation** applied to **Price** to reduce skewness.
- **Feature selection** based on insights from exploratory analysis.
  
## Exploratory Data Analysis (EDA)

<img width="977" height="573" alt="corealtion feature w price" src="https://github.com/user-attachments/assets/d8c817b1-0360-4aaa-a039-0c06944ccc45" />

<img width="718" height="668" alt="corelation matrix" src="https://github.com/user-attachments/assets/2ab35ec4-5ec2-4bf7-930d-1db6f96b6a66" />


### Powerful Engines and Price Relation:
- Vehicles with stronger engine characteristics (horsepower, displacement, torque, and power) are generally priced higher, indicating that **engine performance** is a key price driver.
- These performance attributes are **strongly negatively correlated** with fuel efficiency, showing a clear trade-off between **performance and fuel economy**.
  
### Torque and Power RPM Preferences:
- Higher-priced vehicles tend to reach peak power and torque at lower RPMs, suggesting a market preference for smoother and more efficient power delivery rather than high-rev performance.

### Mileage and Market Age Influence on Price:
- Higher mileage is associated with lower prices, reflecting normal depreciation from usage.
- Mileage is also **strongly negatively correlated** with vehicle release year, indicating that newer vehicles command higher prices, likely due to lower wear and updated features.


  
## Model Selection & Training
- Used **Lasso regression** as a diagnostic baseline and examined the residual plot to assess linearity assumptions.

<img width="988" height="404" alt="residual plto" src="https://github.com/user-attachments/assets/ee0f79df-9486-49a6-96e4-e6bc54f60c08" />

=> The residual plot shows a **U-shaped pattern**, indicating non-linear relationships that cannot be captured by linear models.

- **Non-linear ensemble** models were selected for price prediction:
    - Bagging Regressor
    - Random Forest Regressor
    - Stacked Regression (Bagging + Random Forest)

### Model Comparison
<img width="948" height="222" alt="model comparison" src="https://github.com/user-attachments/assets/69e8ec84-0ce7-4c99-a0f7-3f2cc7fc6f6e" />


### Hyperparameter Tuning 
- Tuned model hyperparameters using **cross-validation** to improve prediction accuracy and stability.

### Impact of Log Transformation
- Compared model performance **before and after** log transformation of the target variable (price).
  
<img width="614" height="169" alt="log vs no log" src="https://github.com/user-attachments/assets/4b0fceb7-96ee-4558-aed6-254fe5e37626" />

=> Log-transformed models showed **lower error and more stable predictions**.


### Final Model Evaluation
- Log-transformed ensemble models achieved **lower Training and Test MSE** compared to non-log models, indicating improved handling of variance and outliers.
- **Log Bagging** showed the best overall performance, with **high Test R²** and **stable generalisation** on unseen data.
