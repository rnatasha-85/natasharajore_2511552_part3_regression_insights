## Dummy Variable Approach

The categorical variables region and store_type were converted into dummy variables so they could be used in the regression model. New columns were created for each dummy variable, and the dataset was updated with these new columns.

### region

The region column has four categories: East, West, North, and South.

East was selected as the reference category. No dummy variable was created for East.

The following new columns were created:
- region_West
- region_North
- region_South

The values in these columns were assigned as follows:
- 1 if the store belongs to that region.
- 0 if the store does not belong to that region.

For stores in the East region, all three dummy variable columns have a value of 0.

### store_type

The store_type column has four categories: Airport, High Street, Mall, and Residential.

Residential was selected as the reference category. No dummy variable was created for Residential.

The following new columns were created:
- store_type_Airport
- store_type_HighStreet
- store_type_Mall

The values in these columns were assigned as follows:
- 1 if the store belongs to that store type.
- 0 if the store does not belong to that store type.

For stores with the Residential store type, all three dummy variable columns have a value of 0.

One category from each variable was left out to avoid duplicate information in the regression model. The regression model will use the dummy variable columns instead of the original region and store_type columns.


## Simple Regression Model

### marketing_spend

- Regression equation : monthly_sales = 560777.3454 + 2.12957 * (marketing_spend)
- R-squared : 0.16724
- Coefficient : 2.12957
- P-value : 2.48006 X 10^(-14)
- Business interpretation : 
	- Stores that spend more on marketing tend to have higher monthly sales.
	- On average, increasing marketing spend by 1 unit is associated with an increase of about 2.12957 units in monthly sales.
	- This suggests that marketing spend has a positive effect on sales.	
- Whether the variable appears useful :
  Yes. The p-value is less than 0.05, which means the relationship is statistically significant. Marketing spend appears to be a useful predictor of monthly sales.

### avg_discount_pct

- Regression equation : monthly_sales = 697835.6296 + (-138730.4547) * avg_discount_pct
- R-squared : 0.00829
- Coefficient : -138730.4547
- P-value : 0.10399
- Business interpretation : 
	- The model shows that higher discounts are associated with lower monthly sales.
        - However, this relationship is weak and may have occurred by chance.
        - Based on this model alone, discounts do not appear to have a clear impact on monthly sales.
- Whether the variable appears useful :
	No. The p-value is greater than 0.05, so the relationship is not statistically significant. avg_discount_pct does not appear to be a useful predictor of monthly sales when analyzed on its own.

## Multiple Regression Model

### Intercept

The intercept is 147642.16. It represents the estimated monthly sales when all the independent variables have a value of zero. Although this situation is unlikely in practice, the intercept serves as the starting point of the regression equation.

### Coefficients
- marketing_spend: 1.2034
- footfall: 33.6227
- inventory_availability_pct: 2893.1764
- competitor_distance_km: -2862.4094
- region_South: 11558.4348
- store_type_HighStreet: -244.4477

### R-squared

The R-squared value is 0.8207. This means that the model explains about 82.07% of the variation in monthly sales, indicating a good fit.

### P-values
- marketing_spend: 1.51 × 10⁻¹⁸ (Statistically significant)
- footfall: 1.07 × 10⁻¹⁰² (Statistically significant)
- inventory_availability_pct: 1.50 × 10⁻⁹ (Statistically significant)
- competitor_distance_km: 1.67 × 10⁻⁶ (Statistically significant)
- region_South: 0.0704 (Not statistically significant)
- store_type_HighStreet: 0.9626 (Not statistically significant)

### Direction of Relationship
- marketing_spend: Positive
- footfall: Positive
- inventory_availability_pct: Positive
- competitor_distance_km: Negative
- region_South: Positive
- store_type_HighStreet: Negative

### Business Meaning of Each Important Variable
- marketing_spend: Higher marketing spend is associated with higher monthly sales. Increasing marketing activities may help improve sales.
- footfall: Stores with more customer visits tend to generate higher monthly sales. Increasing customer footfall can positively impact sales.
- inventory_availability_pct: Better inventory availability is associated with higher monthly sales. Maintaining adequate stock levels can help improve sales.
- competitor_distance_km: The model shows that stores farther from the nearest competitor tend to have lower monthly sales. This relationship is statistically significant, but the business reason may require further investigation.

### Variables That Appear Statistically Weak or Difficult to Interpret
- region_South: The p-value is greater than 0.05, so there is not enough evidence to conclude that stores in the South region perform differently from stores in the East region.
- store_type_HighStreet: The p-value is much greater than 0.05, indicating that this variable does not have a significant effect on monthly sales in this model.



# Model Equations

## Simple Regression Model 1

### Regression Equation

monthly_sales = 560777.35 + 2.1296(marketing_spend)

### Coefficient Explanation
- Intercept (560777.35): This is the estimated monthly sales when marketing spend is zero.
- marketing_spend (2.1296): For every one-unit increase in marketing spend, monthly sales are expected to increase by about 2.1296 units. This indicates that higher marketing investment is associated with higher sales.

## Simple Regression Model 2

### Regression Equation

monthly_sales = 697835.63 - 138730.4547(avg_discount_pct)

### Coefficient Explanation
- Intercept (697835.63): This is the estimated monthly sales when the average discount percentage is zero.
- avg_discount_pct (-138730.4547): The negative coefficient indicates that higher discount percentages are associated with lower monthly sales. However, this relationship is not statistically significant, so it should not be used alone for business decisions.


## Multiple Regression Model

### Regression Equation

monthly_sales = 147642.16 + 1.2034(marketing_spend) + 33.6227(footfall) + 2893.1764(inventory_availability_pct) - 2862.4094(competitor_distance_km) + 11558.4348(region_South) - 244.4477(store_type_HighStreet)

### Coefficient Explanation
- Intercept (147642.16): This is the estimated monthly sales when all independent variables have a value of zero.
- marketing_spend (1.2034): Increasing marketing spend is associated with higher monthly sales. On average, a one-unit increase in marketing spend is associated with an increase of about 1.2034 units in monthly sales.
- footfall (33.6227): Stores with higher customer footfall tend to achieve higher monthly sales. Each additional customer visit is associated with an increase of about 33.6227 units in monthly sales.
- inventory_availability_pct (2893.1764): Higher inventory availability is associated with higher monthly sales. A 1% increase in inventory availability is associated with an increase of about 2,893.1764 units in monthly sales.
- competitor_distance_km (-2862.4094): The model indicates that stores farther from the nearest competitor tend to have lower monthly sales. This relationship is statistically significant, although the business reason may require further investigation.
- region_South (11558.4348): The positive coefficient indicates that stores in the South region are estimated to have higher monthly sales. However, this relationship is not statistically significant, so there is not enough evidence to conclude that being in the South region has a meaningful effect on monthly sales.
- store_type_HighStreet (-244.4477): The negative coefficient indicates that High Street stores are estimated to have slightly lower monthly sales. However, the relationship is not statistically significant, so there is not enough evidence to conclude that the High Street store type has a meaningful effect on monthly sales.

### Dummy Variables

The categorical variables region and store_type were converted into dummy variables so they could be included in the regression model.

The following dummy variables were created:

region
- region_West
- region_North
- region_South

store_type
- store_type_Airport
- store_type_HighStreet
- store_type_Mall

Each dummy variable contains:
- 1 if the store belongs to that category.
- 0 if the store does not belong to that category.

### Reference Categories

One category from each categorical variable was excluded to avoid redundancy in the regression model.

- Reference category for region: East
- Reference category for store_type: Residential

The coefficients of the dummy variables are interpreted relative to these reference categories.

### Final Model Selected

The Multiple Regression Model was selected as the final model.

### Reason for Selecting the Final Model

The multiple regression model was selected because it provides a more complete understanding of the factors affecting monthly sales. It explains 82.07% of the variation in monthly sales, compared with 16.72% for the marketing spend model and 0.83% for the average discount percentage model.

The model identifies marketing_spend, footfall, inventory_availability_pct, and competitor_distance_km as significant drivers of monthly sales. This enables the leadership team to understand which business factors have the strongest association with sales and supports better decisions related to marketing investment, inventory management, and customer traffic. Although region_South and store_type_HighStreet were not statistically significant, including them allowed the model to evaluate whether store location and store type contributed to sales after accounting for the other variables.
