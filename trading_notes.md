# Company Valuation

```python
intrinsic value = (annual dividend earned)/(discount rate)
# intrinsic value is the value of all future dividends

book value = (total assets) - (intangible assets) - (liabilities) 
## intangible assets include stuff like brand worth.
# essentially the value of each sector of a company (like alphabet = google + google maps + ... + waymo) 


market cap = (outstanding market shares) * (number of market shares)
# value the market is placing on the company
```

## Strategies
When investing, look for deviations between these intrinsic values, book value, and market cap

### Lowering intrinsic value, stagnant market cap
If some exogenous force causes the company's intrinsic values  dividends to go down and the market cap has not changed
reflecting this, you should **short** the stock. However, if the intrinsic value increases and market cap is low, you should **buy**

### Book value is the lowest value of the company
If the market cap is below the book value, you buy the company immediately


# Market Portfolios

## What is it
Market is generally just the S&P 500; indexes. Market portfolios weight a portfolio of a subset of the stocks in the market.

Most indexes are cap weighted:

```python
weight_indvl_stock_i = market_cap_of_comp_i/sum(market_cap_of_all_comps)
```
Larger companies represent a larger portion of the S&P 500. 

## Capital Assets Pricing Model

The return of a particular stock on a day is dependent somewhat on the return of the market on that day.
Beta is the elasticity of the market on the stock; alpha is random, and therefore has an expected value of 0.

### Strategies

#### Passive investing
Create a weighting of all the stock in the S&P 500 based on the weighting of the S&P 500. Basically you should just buy an index portfolio and hold. This is in accordance with the Efficient Market Hypothesis and the CAPM theory that the expected value of the residual is 0.

#### Active investing
You pick stocks and assign different weights than accordance with theory. This type of investing assumes alpha is not 0.
They can compare two stocks and think stocks will go up or down relative to the market.
You can use information/ML to find stocks with positive or negative alpha.

### Portfolio Return

Given CAPM, the return on a portfolio is the linear combination of each stock weight times the stock priced by CAPM:

```python
port_return = sum(weight_i*(Beta_of_i*market_return_that_day + alpha_for_stock_i_that_day))
```

For upward markets, we want the stock tied to market returns, so we look for stocks with higher Beta.
Vice versa for downward markets.

### Arbitrage Pricing

In this strategy, we create a Beta for each sector of the market and use the market return for the sector
(perhaps better performance is simply the betas are averaged and the market return is used because each
sector is still affected by the overall market?)


