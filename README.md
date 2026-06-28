# natasharajore_2511552_part3_regression_insights

## 1. Business Problem Summary

The purpose of this analysis is to identify the business factors that are associated with monthly sales. Regression analysis is used to understand which variables have the strongest relationship with sales and to provide recommendations that can help improve business performance.

## 2. Dataset Description

The dataset contains 320 records, with each record representing the monthly performance of a retail store. It includes information on store characteristics, operational metrics, and business performance, such as marketing spend, customer footfall, average discount percentage, staff count, inventory availability, competitor distance, holiday status, customer rating, monthly sales, and monthly profit. The dataset was used to identify the factors associated with monthly sales through regression analysis.

## 3. Dataset Review

### Dependent Variable
- monthly_sales – Target variable representing the monthly sales of each store. This is the dependent variable for the regression analysis.

### Potential Independent Variables
The following variables are considered potential predictors of monthly sales:
- marketing_spend
- footfall
- avg_discount_pct
- staff_count
- inventory_availability_pct
- competitor_distance_km
- holiday_flag
- customer_rating
- region
- store_type
- month

### Numerical Variables
- marketing_spend
- footfall
- avg_discount_pct
- staff_count
- inventory_availability_pct
- competitor_distance_km
- customer_rating
- monthly_sales
- monthly_profit

### Categorical Variables
- month
- region
- store_type
- holiday_flag (binary categorical variable)

### Variables That May Need Cleaning or Transformation
- The competitor_distance_km and customer_rating columns contain missing values. Since these are numerical variables, the missing values will be replaced with the median or mean, as appropriate.
- A few outliers were identified in the marketing_spend, staff_count, inventory_availability_pct, and competitor_distance_km columns. These values appear to be realistic business observations, so no cleaning or transformation will be performed.
- The categorical variables (month, region, and store_type) will be encoded into numerical format before building the regression model.
- The holiday_flag column was checked and contains only valid binary values (0 and 1). Therefore, no cleaning or transformation is required.

### Variables That May Not Be Useful for Regression
- store_id may not be useful because it is only a unique identifier.
- monthly_profit may not be used because it is a business outcome closely related to monthly_sales and could affect the regression results.

## 4. Regression Approach

The analysis began with simple linear regression to evaluate the relationship between individual independent variables and monthly_sales. A multiple linear regression model was then developed using multiple numerical variables and dummy variables to examine their combined relationship with monthly_sales. The models were compared using regression equations, R-squared values, coefficients, and p-values to identify the variables that were most strongly associated with monthly sales and to select the final model.

## 5. Dummy Variable Approach

The categorical variables region and store_type were converted into dummy variables for use in the regression model. One category from each variable was excluded to serve as the reference category and avoid redundancy in the model.

- Reference category for region: East
- Reference category for store_type: Residential

## 6. Model Comparison Summary

Three regression models were developed and compared.

- Simple Regression Model 1 (marketing_spend) explained 16.72% of the variation in monthly sales and showed a statistically significant positive relationship.
- Simple Regression Model 2 (avg_discount_pct) explained only 0.83% of the variation in monthly sales and was not statistically significant.
- Multiple Regression Model explained 82.07% of the variation in monthly sales and identified marketing_spend, footfall, inventory_availability_pct, and competitor_distance_km as statistically significant variables.

## 7. Final Model Selected

The multiple regression model was selected because it provided the highest explanatory power (R² = 0.8207) and identified the key business variables associated with monthly sales.

## 8. Business Recommendation

Leadership should focus on increasing customer footfall, optimizing marketing spend, and maintaining high inventory availability, as these variables showed the strongest positive association with monthly sales. The relationship between competitor distance and monthly sales should be investigated further before making business decisions based on it. Variables such as region_South, store_type_HighStreet, and avg_discount_pct should not be over-interpreted because they were not statistically significant in the analysis.

## 9. Assumptions & Limitations

Assumptions
- A linear relationship exists between the independent variables and monthly_sales.
- The dataset is assumed to be accurate after data cleaning and preparation.
- The selected independent variables are assumed to be appropriate for explaining monthly sales.
- The dummy variables correctly represent the categorical variables in the regression model.

Limitations
- The multiple regression model explains 82.07% of the variation in monthly sales, while 17.93% of the variation remains unexplained.
- The regression analysis identifies associations between variables and monthly sales but does not prove that one variable causes changes in sales.
- Some variables in the model, such as region_South and store_type_HighStreet, were not statistically significant and should be interpreted with caution.
- The findings are based only on the available dataset and variables included in the analysis.

## 10. Screenshots Included

The following screenshots have been included as evidence of the analysis:
- Simple regression output
- Multiple regression output
- Residuals preview
- Model comparison preview
