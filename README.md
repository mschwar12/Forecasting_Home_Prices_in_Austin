# Forecasting Home Prices in Austin, TX Using Time-Series Modeling

**Author**: [Matt Schwartz](mailto:mtschwart@gmail.com)

## Overview 

The following report provides data and analysis on the Austin housing market, and uses time series models to forecast future home prices to calculate growth rates among zip codes. 

## Business Problem

Austin, TX is the fastest growing city in the country. [From 2019 to 2020, the city saw its population grow by 3%, the largest among metropolitan areas with at least 1 million people.](https://www.bizjournals.com/austin/news/2021/05/04/census-data-austin-metro-population.html). As a consultant for an Austin-based real estate investment firm, I will be advising on what 5 zip codes to invest their money in. For the purposes of accurate forecasting, we'll be forecasting 2-year growth rates, using predicted prices for 2018 and 2019.

What makes a zip code a top 5 zip code? For this firm, it pure growth rate. The higher the growth rate, the better. With such a short time horizon of two years, the firm is willing to take big swings to produce higher returns for their investors. Using monthly data from 2010 - 2017, we'll create a time series model to help us forecast what prices would be in 2018 and 2019. The zip codes with the highest growth from 2017 to 2019 will be the optimal investments for this firm.

We'll also explore the housing market in the broader metro area, and look at how Austin prices and growth compares to other major cities.

## Data

The data in this project comes from Zillow Research. There are nearly 15K zip codes, about 35% of the total in the U.S. Other variables include

- City
- State
- Count
- Metro Area
- Size rank (population size relative to others)

## Methods

To build a prediction engine, we utilized multiple linear regression. By regressing the variables listed above on price, we were able to account for a significant portion of the variation in price. To eliminate the influence of major outliers, we limited the sample to houses that sold for between $100,000 and $1,000,000, and that were smaller than 4500 square feet in total space.

In addition, we create a number of variables based on our existing data. These include each houses' distance from downtown Seatlle in miles, age, and a dummy variable for whether a house was renovated or not.

## Results

We'll use time-series modeling (SARIMAX) to forecast future home prices using the price data from 2010 - 2017 (as to avoid major effects of the recession).

Top 5 Fastest Growing Zip Codes:

1) 78744 - South East Austin (Airport)
2) 78721 - East Austin
3) 78753 - North Austin (North Lamar)
4) 78741 - Riverside
5) 78724 - North East Austin (Daffan)

## Conclusions

- Zip codes notably do not include downtown or other up and coming locations like Mueller
- All of East Austin has great investment potential
- The growth rates in the top 5 Zip codes are all over 30%, with some eclipsing 40%.

## Further Analysis

In the future, I want to dive into what makes these zip codes such high-growth areas. What sort of developments, schools, and other infratructure are contributing to the growth rates? This can help the firm on a more granular level explain why, for example, East Austin is taking off, beyond what you can see with your eyes.

## For More Information

Please find the full analysis in the Jupyter notebook contained in this respository.

For any questions, please contact Matt Schwartz at [mtschwart@gmail.com](mailto:mtschwart@gmail.com)



## Repository Structure

```
├── data
├── images
├── .canvas
├── .gitignore
├── CONTRIBUTING.md
├── Forecasting Growth Rates in the Austin Housing Market.ipynb
├── Forecasting Growth Rates in the Austin Housing Market_Jupyter_Notebook.pdf
├── Forecasting_Austin_Home_Prices.pdf
├── README.md
```
