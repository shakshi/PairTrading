# PairTrading
Finding pair of stocks that can be traded together using Machine Learning 

# Pair Trading 
This is a very powerful technique used by investors to play safe in the stock market
So basically they find stocks that have historically moved together 
and this happens mostly with stocks of companies that belong to the same sector (eg. Pepsi & Coca-Cola, Amazon & Google)
or companies that are dependent on one another (eg: one company drills oil wells, other manufactures drills)

Idea is that when their prices diverge, buy the lower one, sell the higher
We know that they will meet in near future 
If lower one's price increases - u can earn profit by selling it now
If higher one's price decreases - u have earned profit by selling it at higher price earlier

This is a market neutal risk strategy very popular in stock trading 

# Project aim 
This project aims to find pairs of stocks that are correlated and can be traded together 

# Idea
We can find correlation between every pair of stocks and see which pairs have highest correlation 
But, given the fact that we have almost 500 companies - it is practically not possible to check correlation for all
possible pairs

So, instead of blindly finding correlation between stock prices, we first decided find companies that might to related to each other 
and then check for pairs amongst them 
This adds intuitive knowledge - so we dont completely rely on statistical tools

