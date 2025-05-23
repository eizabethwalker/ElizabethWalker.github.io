# Case Study: Investment Optimization - 5 Year Performance of SPY, VTI, and AGG
## Context 
I wanted to evaluate how different investment strategies would have performed over the past 5 years. I chose to look at the performance of the following:  
- S&P 500 EFT- Large Cap U.S. Stocks
- Total Stock Market EFT- Broad U.S. Market Exposure
- Aggregate Bond EFT- U.S. Bonds
  
I was interested in seeing how these EFTs interact with diversified portfolios and how they behaved during market downturns and recoveries.

## Objective 
Analyze the historical performance of SPY, VTI and AGG from 1/1/2019-12/29/2023 

## Design Process
I chose to use RStudio to clean, calculate and analyze the data. After completing the necessary steps, I used RMarkdown to create a graph to display the necessary information. 

### Step 1: Data Collection & Merging
I choose to use MarketWatch as my main data source for SPY, VTI, and AGG's past performance over a 5 year period. MarketWatch is a crediblt source owned by News Corp that presents the data in a organized spreadsheet. 

#### *Cleaning and Merging the Data*
The data was cleaned by ensuring the date* formats across the three datasets were set to the pattern, Month, Date, Year. This was important for the next step, *merging*, where the three data sets were combined by date.  

### Step 2: Calculate Performance & Risk Metrics
Claculating performance and risk metrics is important to help understanding contributions to portfolio growth, risk management, and being able to compare behavior in different market conditions.

#### *Normalizing the Data*
The data was first normalized to ensure all the assest were on the same scale. 

#### *Calculating Returns*
Calculating returns was interesting as I did not where to start. I decided using matrices would be the most appropriate. I began by removing the date column, creating a matrix and computing the price differences from day to day for each EFT. After completing these steps, I assigned the appropraite dates to daily percentage return. 

#### *Calculating Rolling Volatility*
I then calculated a 30-day rolling window standard deviation of daily returns for each EFT. The output is the annualized rolling volatility of each EFT (last day of each 30-day window).  

#### *Finding the Sharpe Ratio*
The final step was the find how much excess return you recieve per unit of risk per EFT. I was able to calculate which EFT had the best return of risk taken over the period. 


### Step 3: Visualization
The following line chart represents the normalized price performance of SPY, VTI, and AGG over a 5 year period (1/1/19-12/29/23)

![image](https://github.com/user-attachments/assets/c617067a-0d89-4955-ad0e-ff7b604def99)


## Summary
SPY and VTI are highly correlated while AGG provides a strong diversification. During Market downturns, AGG remained relatively stable. VTI slightly overperformed SPY in the long-term but mained similar risk. 

### Application
For aggresive growth favor VTI and/or SPY and for stability choose AGG.
Suggested allocation for medium risk with a strategic tilt toward large-cap stocks: 
60% VTI 
30% AGG 
10% SPY 


