# Financial Report
In this report, we used Plaid API to retrieve the information necessary to create a budget analysis. We then used IEX Financial to retrieve stock's historical data and perform Monte Carlo simulations. With the information acquired, we were able to link the customer's banking accounts with their investment accounts and determine whether the portfolio met the necessary requirements. 

## Budget Analysis
In this analysis, we used Plaid to retrieve the customer's last 90 days of transactions as well as his yearly income. We sorted the transactions by categories and then organized them into a pie chart. Lastly, we illustrated the customer's monthly spending by creating a bar graph.
                                                                
| **Previous Year Income** | **Current Monthly Income** | **Projected Yearly Income** |
|--------------------------|----------------------------|-----------------------------|
| $7,893.00                |    $500.00                 |      $6,085.00              |



| **Category**|**Amount**|
|------|-------|
|Food and Drink| $3,317.19|
|Payment| $6,310.50 |
|Recreation| $235.50|
|Shops|$1,500.00|
|Transfer| $20,537.34|
|Travel|35.19|

![Pie Chart](Unit_5_API_Account_Summary_Portfolio_Planner/Images/pie_chart_spending_per_category.png)

|**Date**|**Amount**|
|--------|---------|
|January|$4,084.83|
|February|$10,145.24|
|March|$11,145.24|
|April|$6,560.41|

![Bar Graph](Unit_5_API_Account_Summary_Portfolio_Planner/Images/bar_chart_spending_per_month.png)

## Retirement Planning
In this analysis we used IEX Financial to retrieve closing prices of SPDR S&P 500 ETF Trust (SPY) and iShares Barclays Aggregate Bond Fund (AGG) and calculated their daily returns and volatility. We then set the portfolio weights to 60% SPY and 40% AGG and ran 500 Monte Carlo simulations in order to fare the porfolio's performance over the next 30 years. The results are as follows:

![Monte Carlo Simulation Of Trading Days vs. Cumulative Returns](Unit_5_API_Account_Summary_Portfolio_Planner/Images/monte_carlo.png)

This graph demonstrates 500 simulations of the number of trading days (X axis) vs. the cumulative returns (y axis) over the next 30 years. In 30 years we can predict that the cummulative returns could yield between .65 and 2.83. Narrowing this down to a 90% confidence interval we can predict that the portfolio could yield between .56 and 6.82 cummulative return.

![Visualization of ending returns](Unit_5_API_Account_Summary_Portfolio_Planner/Images/90_confidence_interval.png)

Lastly, we calculated whether a 4% withdrawal rate from the retirement portfolio would meet the value of the customer's yearly income if the initial investment is $20,000.00 and found that it will not. The customer's initial investment is $6085.00, so in order to meet or exceed this amount we would have to increase the initial investment to $30,000. When we do this we find that a 4% withdrawal rate will meet his yearly income and exceed it by $683.00.
