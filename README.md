# Asthma & Smoking Risk Analysis

## Inspiration

As we all grew up around an environment with a high exposure to second hand smoke, we were interested to see the percentage of asthma rate around our area (LA/OC zip-codes) and the top factors that are most likely to be associated and influenced this exposure. We focused on couple variables such as percentage of smoking rate, race groups, median household income, percentage of mental distress, education level, etc.

## What it does & How we built it

We merged Melissa Zip-Code dataset for demographics and Health related dataset PLACES from the CDC by zip-codes in LA/OC county as our main data frame. Using XGBoost, we computed the top 5 most important features for our predictive model for asthma rate, with the top three being:

1. Percentage of Population who are Asian (negative)
2. Percentage of Adults experiencing Frequent Mental Distress
3. Percentage of Population who are African American
   
(Test R^2 = 0.6914)

These findings contradicted our original hypothesis that being Asian would correlate to asthma rates in a positive matter (due to our own experiences being surrounded by smoking Asian American adults). Out of curiosity, we trained another model to predict cigarette smoking prevalence, to see if Asian Americans smoke more but are simply less prone to asthma (as has been found in research studies). We did not, however, find Asian population percentage as a top 5. The top three where:

1. Percentage of population without a high school diploma
2. Median Household Income (negative)
3. Percentage of Adults experiencing Frequent Mental Distress
   
(Test R^2 = 0.6594)

## Challenges we ran into

We shifted our project focus multiple times from exploring health related indicators such as Airborne disease and Covid 19 Vaccination rate to determine the overall health in OC county, but concluded that they couldn't accurately predict the broader health analysis of the entire county. Another challenge we faced is the limited amount of available datasets on LA/OC related to our idea and containing related zip-codes data as it was our primary key.
