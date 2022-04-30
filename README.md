# Alpha Based Mutual Fund Selection

## Intro

For most investors, they always choose mutual funds by checking historical performance (ranking, annual return, Sharpe ratio, etc), which has triggered me to ponder: 1) Is the historical performance sustainable? 2) How effective is the historical performance? 

##  Data Description

- Choose partial stock hybrid fund, flexible allocation fund fund and equity fund and their NAV
- Stock price and NAV  are adjusted
- In order to avoid false correlation produced by the unsteady price, I chose log return to do the regression
- Market return: Index of equity fund
- MKT(-): log market value
- ROE(+): roe(trailing twelve months)
- PB(-): price-to-book ratio
- GROWTH(+): yoy growth rate of net profit (seasonal)
- Initial: 300000CNY
- buy cost/sell cost: 0.5%
- **Note: 1) caution the actual publish date of stocks and mutual funds, and make sure do not include future data;  **

## Strategy Intro

- Grouped stocks into 3 batches and computed alpha for each stock as below:
- For each season, buy those whose alpha ranks top 20%

## Results

- Sharpe:0.72；Annual Return:10.92%；Max Drawdown:14.23%
- After I did some improvement: Sharpe:1.00；Annual Return:20.17%；Max Drawdown:21.17%
- Please refer to my project to get all the trails I did and the results

## Defects and Improvements

- Much more details for factor building to be done: 1) price limit should be considered; 2) new stock should also be excluded; ...
- How to choose factors to get Alpha is a thing
