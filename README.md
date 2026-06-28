# natasharajore_2511552_part3_regression_insights

## Dataset Review

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
