# DST MarketAnalysis
The Effects of Daylight Savings on Financial Markets

These notebooks analyze select Kaggle data for a significant effect on financial markets due to the Daylight Savings Time effects, which has been known to cause problems and uncertainty in human behavior. The data is from the following link:
https://www.kaggle.com/datasets/ehallmar/daily-historical-stock-prices-1970-2018

This data contains daily individual stock prices from 1971-2018 from NASDAQ and NYSE. Each row has the ticker (stock code), high, low, open, close, adjusted close, and volume.

Some notebooks are dedicated to processing the data, some to exploratory data analysis/visualization, some to statistical methods, and some to applying classifiers. We split the analysis into the following sectors: finance, tech, health, consumer services. There is also one notebook for the transportation sector but without classifiers applied (it's a fairly small percentage of the total data).

Data Processing/Scraping:
- `DST_dates,ipynb`
- `data_exploration.ipynb`
- `nikkei_scrape.ipynb`
- `nikkei_EDA.ipynb`

Statistical Methods:
-

Classifiers:
- `kaggle_finance_classify.ipynb`
- `kaggle_tech_classify.ipynb`
- `kaggle_health_classify.ipynb`
- `kaggle_consumer_classify.ipynb`


The notebooks also analyze the Nikkei 225 Index. This is an index used by the Japanese stock exchange; Japan does not observe DST and so this acts as a control group.