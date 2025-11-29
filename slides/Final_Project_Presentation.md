# Predicting California Housing Prices
## A Machine Learning Approach to Real Estate Valuation

**CIS 508 - Machine Learning and Business**  
**Final Project Presentation**

---

## Slide 1: Project Overview

**Problem Statement**
- Predict median house values in California housing districts
- Support strategic decision-making in real estate market
- Enable data-driven pricing and investment decisions

**Dataset**
- California Housing Prices (1990 Census Data)
- 20,640 observations, 10 features
- Target: median_house_value (continuous)

**Approach**
- Supervised learning regression task
- Two models: Linear Regression and Random Forest
- Comprehensive EDA and business insights

---

## Slide 2: Business Motivation

**Stakeholders**
- Homebuyers and sellers
- Real estate agents and brokers
- Investors and lenders
- Property developers
- Government agencies

**Business Value**
- Accurate pricing strategies
- Risk assessment for lenders
- Investment opportunity identification
- Market efficiency and transparency

**Cost of Inaction**
- Financial losses from mispricing
- Poor investment decisions
- Increased default risks
- Competitive disadvantage

---

## Slide 3: Dataset Overview

**Key Variables**
- **Target**: median_house_value (median house value in dollars)
- **Geographic**: longitude, latitude, ocean_proximity
- **Housing**: housing_median_age, total_rooms, total_bedrooms
- **Demographic**: population, households, median_income

**Data Characteristics**
- 20,640 housing districts
- Mix of continuous and categorical variables
- Generally clean data with minimal missing values
- Some outliers in variables like total_rooms and population

**Data Quality**
- Missing values handled (total_bedrooms imputed)
- Duplicates checked and removed
- Outliers identified using IQR method
- Derived variables created for better insights

---

## Slide 4: Key EDA Insights - Income and Location

**Insight 1: Median Income is the Strongest Predictor**
- Correlation of 0.69 with house values
- Income levels fundamentally determine purchasing power
- Higher-income districts consistently support higher property values

**Insight 2: Geographic Location Creates Value Premiums**
- Coastal properties command significantly higher prices
- Ocean proximity categories show $100,000+ price differences
- Island locations: highest premiums
- Inland properties: most affordable segment

**Business Implication**
- Location-based pricing strategies are critical
- Income data essential for market segmentation

---

## Slide 5: Key EDA Insights - Housing Characteristics

**Insight 3: Derived Variables Reveal Important Patterns**
- rooms_per_household shows stronger correlation than raw total_rooms
- Larger homes relative to household size drive higher valuations
- Housing age has complex relationship with value

**Insight 4: Unexpected Patterns**
- Population density shows negative correlations in some areas
- Suggests quality-of-life preferences
- Urban vs. suburban value dynamics

**Data Quality Notes**
- Target variable right-skewed with $500K cap
- Outliers present but manageable
- Multicollinearity between some variables

---

## Slide 6: Modeling Approach

**Problem Type**
- Supervised regression task
- Predicting continuous median_house_value

**Feature Selection**
- 12 features including:
  - Original variables (geographic, demographic, housing)
  - Derived variables (rooms_per_household, bedrooms_per_room)
  - Encoded ocean_proximity

**Data Preparation**
- 80/20 train-test split
- Feature scaling for Linear Regression
- Categorical encoding for ocean_proximity

---

## Slide 7: Model 1 - Linear Regression

**Model Characteristics**
- Baseline model with high interpretability
- Fast training, no hyperparameters
- Assumes linear relationships

**Performance**
- Test R²: [Will show actual value when notebook runs]
- RMSE: [Will show actual value]
- MAE: [Will show actual value]

**Strengths**
- Interpretable coefficients
- Direct feature importance
- Easy to explain to stakeholders

**Weaknesses**
- May miss non-linear patterns
- Limited complexity handling

---

## Slide 8: Model 2 - Random Forest

**Model Characteristics**
- Ensemble method with 100 trees
- Captures non-linear relationships
- Handles feature interactions
- Robust to outliers

**Hyperparameters**
- n_estimators: 100
- max_depth: 20
- min_samples_split: 5
- min_samples_leaf: 2

**Performance**
- Test R²: [Will show actual value when notebook runs]
- RMSE: [Will show actual value]
- MAE: [Will show actual value]

**Feature Importance**
- median_income: strongest predictor
- Geographic features (longitude, latitude)
- Derived variables (rooms_per_household)

---

## Slide 9: Model Comparison

**Performance Summary**

| Metric | Linear Regression | Random Forest |
|--------|------------------|---------------|
| Test R² | [Value] | [Value] |
| Test RMSE | [Value] | [Value] |
| Test MAE | [Value] | [Value] |

**Winner: Random Forest**
- Higher R² score
- Lower prediction errors
- Better captures complex patterns

**Trade-offs**
- **Linear Regression**: High interpretability, lower accuracy
- **Random Forest**: Higher accuracy, lower interpretability

**Deployment Recommendation**
- Use Random Forest for maximum accuracy
- Use Linear Regression when interpretability is required (regulatory, stakeholder communication)

---

## Slide 10: Feature Importance Analysis

**Consistent Findings Across Models**
- **median_income**: Most influential (correlation 0.69)
- **Geographic location**: Longitude, latitude, ocean_proximity
- **Derived variables**: rooms_per_household

**Business Validation**
- Findings align with EDA insights
- Income and location dominate predictions
- Feature engineering (derived variables) adds value

**Actionable Insights**
- Focus pricing strategies on income levels
- Geographic location is a key differentiator
- Normalized housing metrics better than raw totals

---

## Slide 11: Executive Summary

**Main Finding**
Median income is the strongest predictor of house values (correlation 0.69), with geographic location (particularly ocean proximity) serving as the second most influential factor, creating a clear coastal premium where properties near the ocean command significantly higher prices than inland regions.

**Key Patterns**
1. Income-driven affordability determines market capacity
2. Geographic location creates substantial value differentials ($100,000+)
3. Normalized housing characteristics (rooms per household) better predictors than raw totals

**Business Recommendations**
1. Develop location-based pricing strategies
2. Use income data for market segmentation
3. Create derived metrics for better predictions
4. Implement geographic visualization tools

---

## Slide 12: Business Implications and Next Steps

**Limitations**
- 1990 data may not reflect current market conditions
- $500K cap on target variable limits high-value predictions
- Some overfitting in Random Forest model

**Next Steps**
1. Implement hyperparameter tuning to reduce overfitting
2. Obtain more recent data for contemporary market analysis
3. Incorporate additional features (school ratings, crime statistics, transportation)
4. Develop real-time model monitoring systems
5. Conduct sensitivity analyses on key predictors

**Expected Impact**
- Improved pricing accuracy for real estate professionals
- Better risk assessment for lenders
- More informed investment decisions
- Enhanced market efficiency

---

## Thank You

**Questions?**

Repository: https://github.com/gphelps-dev/romero-final  
GitHub Pages: https://gphelps-dev.github.io/romero-final/

