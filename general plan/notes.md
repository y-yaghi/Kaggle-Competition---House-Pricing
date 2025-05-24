### Business Problem
_________________________________________________________________________________________________________________________________________________
Okay given the goal:

  It is your job to predict the sales price for each house. For each Id in the test set, you must predict the value of the SalePrice variable. 
  
Our business question would be:

  **"How can we accurately predict the sale price of a house based on its characteristics to support smarter property valuation and investment decisions?"**

What are somethings that impact a homes price?

**Location & Neighborhood**

1. Proximity to amenities: Homes near schools, parks, shopping centers, and public transportation often command higher prices.
2. Neighborhood quality: Safety, cleanliness, and overall appeal of a neighborhood can significantly impact property values.
3. School districts: Properties in reputable school districts tend to be more valuable.

**Property Characteristics**

1. Size and layout: Larger homes with functional layouts are typically more desirable.
2. Age and condition: Newer homes or well-maintained older homes usually fetch higher prices.
3. Upgrades and renovations: Modern kitchens, bathrooms, and energy-efficient features can add value.

**Economic Indicators**

1. Interest rates: Lower mortgage rates can increase buyer affordability, driving up demand and prices.
2. Employment rates: Higher employment levels often correlate with increased housing demand.
3. Inflation and economic growth: General economic health influences buyer confidence and purchasing power.

**Market Dynamics**

1. Supply and demand: Limited housing supply with high demand leads to price increases.
2. Comparable sales (comps): Recent sale prices of similar properties in the area set benchmarks for pricing.
3. Time on market: Properties that linger on the market may indicate overpricing or less desirable features.
Steers Global Real Assets

**Government Policies and Taxes**

1. Property taxes: High property taxes can deter buyers, affecting prices.
2. Zoning laws: Regulations can limit or enhance property development, influencing values.
3. Subsidies and incentives: First-time homebuyer programs or tax credits can stimulate demand.

**Environmental Factors**

1. Climate and weather risks: Properties in areas prone to natural disasters may be less desirable.
2. Environmental amenities: Proximity to green spaces or waterfronts can increase property values.
3. Pollution levels: High pollution can negatively impact desirability and prices.

What models may we use as we go further into this project?

This is a classic **supervised learning problem**, with the goal of predicting a continuous target — in this case, the sale price of a house — as a function of a very descriptive set of input attributes describing each property. Since the target variable (SalePrice) is already available in the training set, the model will be able to discover the input-output mappings. This specification is especially well-adapted to regression models, and a first option would be to employ Linear Regression. It is a highly standard technique applied in predictive modeling for its simplicity of implementation, fast calculation, and interpretability. By examining the coefficients of the model, estimates can be derived about the contribution of different home features to the sale price, both data science- and business-aware.

But although Linear Regression is nice as a baseline, it is not ideal. It assumes a linear relationship between response and predictors, which is unlikely to hold for housing data in the real world, where relationships are most likely to be non-linear, dependent, or influenced by multi-way interactions. It's also prone to multicollinearity and outliers and can perform poorly if there isn't important feature engineering or if the data is noisy. That's where more advanced methods — including Lasso or Ridge regression for regularization, and tree-based approaches like Random Forest or Gradient Boosting (e.g., XGBoost, LightGBM) — tend to be used to maximize predictive accuracy. They are better able to identify complex patterns and feature interactions, thus stronger contenders, especially for contests like this one.
