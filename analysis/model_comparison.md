# Model Comparison

## Simple Regression Model 1

### Variables Used

Dependent Variable: monthly_sales

Independent Variable: marketing_spend

### R-squared

0.16724 (Explains 16.72% of the variation in monthly sales.)

### Significant Variables

marketing_spend

### Business Usefulness

This model helps evaluate the impact of marketing spend on monthly sales. It can support decisions related to marketing budgets by showing whether higher marketing investment is associated with higher sales. However, since it considers only one factor, it provides a limited view of the business.

### Limitations

The model uses only one independent variable and explains 16.72% of the variation in monthly sales. This means that 83.28% of the variation is explained by other factors not included in the model. Therefore, the model provides only a partial understanding of the factors affecting monthly sales and should not be used on its own for business decision-making.


## Simple Regression Model 2

### Variables Used

Dependent Variable: monthly_sales

Independent Variable: avg_discount_pct

### R-squared

0.00829 (Explains 0.83% of the variation in monthly sales.)

### Significant Variables

None

### Business Usefulness

This model helps evaluate whether the average discount percentage is associated with monthly sales. The results show that avg_discount_pct is not a statistically significant predictor of monthly sales when considered on its own. Therefore, the model does not provide sufficient evidence to support business decisions related to changing discount levels based only on this analysis.

### Limitations

The model uses only one independent variable and explains only 0.83% of the variation in monthly sales. The relationship between avg_discount_pct and monthly sales is not statistically significant, indicating that this variable alone does not adequately explain changes in monthly sales. Other business factors should be considered for a more reliable analysis.


## Multiple Regression Model

### Variables Used

Dependent Variable: monthly_sales

Independent Variables:
- marketing_spend
- footfall
- inventory_availability_pct
- competitor_distance_km
- region_South
- store_type_HighStreet

### R-squared

0.82070 (Explains 82.07% of the variation in monthly sales.)

### Significant Variables

- marketing_spend
- footfall
- inventory_availability_pct
- competitor_distance_km

### Business Usefulness

This model provides a more complete view of the factors influencing monthly sales. It helps management identify the most important drivers of sales and prioritize business actions such as increasing marketing spend, improving inventory availability, and attracting more customers. By considering multiple factors together, it supports more informed and reliable business decisions.

### Limitations

The model explains 82.07% of the variation in monthly sales, which means that 17.93% of the variation remains unexplained. Although the model provides a good overall fit, some variables included in the model (region_South and store_type_HighStreet) are not statistically significant and may not contribute meaningfully to explaining monthly sales. The model identifies statistical relationships between the selected variables and monthly sales but does not establish cause-and-effect.
