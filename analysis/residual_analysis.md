## Residual Analysis

### Top 5 Largest Positive Residuals

The following stores have the largest positive residuals:
- STR-1028
- STR-1058
- STR-1051
- STR-1026
- STR-1045

These stores achieved much higher monthly sales than predicted by the regression model. This indicates that the model under-predicted sales for these stores. There may be additional business factors influencing sales that are not included in the model. No clear pattern is observed based on the available region_South and store_type_HighStreet variables, as all five stores are outside the South region and only one store is a High Street store.

### Top 5 Largest Negative Residuals

The following stores have the largest negative residuals:
- STR-1023
- STR-1012
- STR-1017
- STR-1001
- STR-1008

These stores recorded lower monthly sales than predicted by the regression model. This indicates that the model over-predicted sales for these stores. Most of these stores are also outside the South region, and only one is a High Street store. Similar to the positive residuals, no consistent pattern is observed based on the selected dummy variables.

### Interpretation of Residuals
- Positive residuals indicate that the actual monthly sales were higher than the predicted sales. This means the model under-predicted sales for these stores.
- Negative residuals indicate that the actual monthly sales were lower than the predicted sales. This means the model over-predicted sales for these stores.

### Model Prediction Pattern

Based on the top positive and negative residuals, there is no clear evidence that the model consistently under-predicts or over-predicts a particular type of store. The largest residuals are spread across different values of marketing_spend, footfall, inventory_availability_pct, and competitor_distance_km. This suggests that the remaining unexplained variation in monthly sales may be due to factors not included in the regression model.
