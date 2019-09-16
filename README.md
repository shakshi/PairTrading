# PairTrading
Finding pair of stocks that can be traded together using Machine Learning 

## Pair Trading 
This is a very powerful technique used by investors to play safe in the stock market
They find stocks that have historically moved together. This happens mostly with stocks of companies that belong to the same sector (eg. Pepsi & Coca-Cola, Amazon & Google) or companies that are dependent on one another (eg: one company drills oil wells, other manufactures drills)

Strategy - when prices of these stocks diverge, buy the lower one, sell the higher
Assumption - prices will meet in near future 
Thus, If lower one's price increases - they can earn profit by selling it now
If higher one's price decreases - they have earned profit by selling it at higher price earlier

This is a market neutal risk strategy very popular in stock trading 

## Project aim 
This project aims to find pairs of stocks that are correlated and can be traded together 

## Idea
We can find correlation between every pair of stocks and see which pairs have highest correlation 
But, given the fact that we have almost 500 companies - it is practically not possible to check correlation for all
possible pairs

So, instead of blindly finding correlation between stock prices, we first decided find companies that might to related to each other 
This adds intuitive knowledge - so we dont completely rely on statistical tools

Thus, its a 2 step filtering process 

## Algorithm
To find similar companies -
Based on our research, we found that besides sector a company belongs to, factors like sector and price per earning is also a deciding factor to see whether company is related to other or not.

So, we took dataset from datahub.io - that had information about company - sector, market capitalization and price per earning 

Preprocessing dataset -
  - converting sector to numerical categories 
  - replacing blanks in p/e by mean 
 
We used K means clustering algorithm to group similar companies in on clustering (k=11)

On a average, we got 8-10 companies in each cluster. Then we ran correlation test on stock prices of each pair 
If correlation between 2 companies > 0.6 (threshold), then the algorithm considers it to be a good pair for trading 
