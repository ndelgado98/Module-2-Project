# Module-2-Project

## Predicting House Prices in King County

I took the housing dataset which contains information about different houses in King County.On this project were used only 11 features  from the 19 feature variables in original dataset. The objective was to predict the prices houses using the given features.


The prices of the house indicated by the variable 'price' was the target variable and the remaining were the feature variabes that I used to predict the target variable.



# Data Used

|Variable  |Type    | Description                            | Used in the Model|
|----------|--------|----------------------------------------|------------------|     
|Price     |Float   |Prices of the houses (Target Variable)  |   Y              |
|Bedrooms  |Numeric |No. of bedrooms                         |   Y              |
|Bathrooms |Float   |No. of bathrooms                        |   Y              |
|Floors    |Float   |No. of floors                           |   N              |
|sqft_livin|Numeric |square footage of the home              |   Y              |
|sqft_lot  |Numeric |square footage of the lot               |   Y              |
|waterfront|Float   |House which has a view to a waterfront  |   N              |
|condition |Numeric |How good the condition is ( Overall )   |   Y              |
|grade     |Numeric |Overall grade given to the housing unit |   Y              |
|yr_built  |Numeric |Year the house was built                |   Y              |






Data Preprocessing

I analyzed the degree of correlation of all features with target variable in order to have a quick view of potential feature importance and redundancies.
Some of the features have a categorical type, I didn't created dummy variables because they are numeric(not continuous) and therefore I used them like they were.


Model Testing

For my final input,I used 7 variables, distributed for three models.I used a 80-20 train-test split cross-validation to train my model.I first built a multivariate regression model model which combines grade, condition, squared foot lot and year.As my model gave me a good R squared I tried another model with others features, on this second one I used grade, bathrooms and year, again the results based on th R squared satisfied me. Tested a third model, this time the R squared was not so good, runned some tests, trying to validate the assumptions but all were failed. So I refinement the model, dropping the outliers on the feature price. After this, the assumptions were validated but the R squared showed a lower value.


Conclusion

In my test dataset, ~64% of the predictions for home prices can be explained by my model.The model predicts the home prices in King Couty.As I focussed mainly on the physical features of the house,I can conclude that house prices are not only based on the physical properties of a house but also on several other factors.


Future Work

For future work,I would like to include macro features, based essentially on economic indicators and extreme events like wars or economic meltdowns that could have a huge effect on the house prices.

