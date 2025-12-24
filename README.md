# NYC-Housing-Market-Analysis

# Project Overview
This project analyzes residential housing prices in New York City to identify the key factors driving price variation across boroughs. The analysis focuses on understanding how property characteristics, borough location, transit accessibility, and crime indicators influence housing prices. Using Python-based data processing and statistical analysis, the project provides insights into borough-level affordability patterns and pricing dynamics.

# Data Source and Description
Data Source - NewYork Housing Dataset - ("https://data.cityofnewyork.us/resource/qgea-i56i.json?$limit=2000")
Data type - Structured, CSV file.

New York Housing Dataset:
Key Statistics:
Rows: 4,802
Columns: 17

MTA Subway Station Dataset:
Key Statistics:
Rows: 497
Columns: 19

# Preprocessing Steps
# 1) Data Cleaning : 
Removed records with missing or invalid price and square footage values. Filled missing numeric fields (bedrooms, bathrooms) using median values to reduce skew.
Standardized borough names and resolved inconsistent address formats. Dropped irrelevant and duplicate columns to simplify analysis

# 2) Data Integration : 
Merged housing and transit datasets using latitude–longitude proximity. Calculated nearest subway station and station counts within an 800m radius using the Haversine distance formula.  Aggregated borough-level crime statistics and joined them with housing data.

# 3) Feature Engineering : 
Created price_per_sqft for standardized valuation comparison. Engineered stations_nearby to represent transit accessibility. Computed felony_share to normalize crime data across boroughs.                                                                                                                                                                       
# Analysis
# 1) Borough-Level Price Analysis
Compared housing prices across NYC boroughs using descriptive statistics and identified Manhattan as the highest-priced borough and Bronx/Staten Island as more affordable markets.

# 2) Feature Relationship Analysis
Assessed relationships between price and property attributes (sqft, bedrooms, bathrooms) and found square footage and bathroom count to be stronger predictors than bedroom count.

# 3) Crime & Transit Impact Analysis
Evaluated the association between housing prices and borough-level crime indicators. Observed minimal direct impact of crime on pricing at borough granularity
Identified a modest positive effect of transit accessibility on housing prices.

# 4) Statistical Modeling
Applied ANOVA to confirm significant price differences across boroughs. Built OLS and log-price regression models, explaining approximately 63% of price variation.                      
# Libraries Used
Pandas – For data loading, cleaning, merging, and transformation.
NumPy – For numerical computations and feature engineering.
Statsmodels – For ANOVA testing and regression modeling.
Geopy / Haversine – Distance calculations for transit proximity.

# Output & Insights
Borough location emerged as the strongest determinant of housing prices.
Property size (sqft) and bathrooms significantly influenced valuation.
Transit access added value, but to a lesser extent than location and size.
Borough-level crime indicators showed weak explanatory power for pricing.

# Conclusion
This project demonstrates the effective use of Python scripting, multi-source data integration, feature engineering, and statistical analysis to uncover key pricing dynamics in the NYC housing market. The findings provide actionable insights for homebuyers, investors, urban planners, and data analysts, highlighting the dominance of location and property characteristics over broader crime indicators in housing valuation.
