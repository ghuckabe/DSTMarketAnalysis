# The Effects of Daylight Savings Time Changes on Financial Markets

Daylight savings time (DST) was first implemented in Canada in 1908 and then in the US in 1918 primarily to conserve resources during wartime. DST has been demonstrated to have an impact on sleep and health, and some evidence has been presented by Kramer, Kamstra, and Levi that suggests measurable impacts from DST change on the American stock market. Other statisticians such as Berument, Dogan, and Onar refute this notion, so the issue is certainly controversial. This project aims to contribute to this discourse by answering the question of if DST changes impact stock market behaviors and to characterize this impact if such exists. We found a statistically significant result via statistical analysis and machine learning classifiers.

Some notebooks in this repository are dedicated to processing the data, some to exploratory data analysis/visualization, some to statistical methods, and some to applying classifiers. We split the analysis into the following sectors: finance, tech, health, consumer services. There is also one notebook for the transportation sector but without classifiers applied (it's a fairly small percentage of the total data). Below, we will describe each directory but first, we describe the data.

### Data

The notebooks in this repository analyze select Kaggle data for a significant effect on financial markets due to the Daylight Savings Time effects, which has been known to cause problems and uncertainty in human behavior. The data is from the following link:
https://www.kaggle.com/datasets/ehallmar/daily-historical-stock-prices-1970-2018 

These data contains daily individual stock prices from 1971-2018 from NASDAQ and NYSE. Each row has the ticker (stock code), date, high, low, open, close, adjusted close, and volume.

The notebooks also analyze the Nikkei 225 Index which contain date, high, low, open, close. The data are found here: https://indexes.nikkei.co.jp/en/nkave/archives/data. The Nikkei 225 is an index used by the Japanese stock exchange; Japan does not observe DST and so this was intended as a control group, in a way. We also analyzed individual Japanese stocks (data found here: https://www.kaggle.com/datasets/cryptrader/huge-japanese-stock-market-dataset-all-in-one/data)

Lastly, there are individual stocks found on Yahoo Finance, investing.com, and Google which contain date, high, low, open, close, adjusted close, and volume. The notebooks indicate where to find them.

To run everything in this repository, download the data from the links given. Many of the data files are too large to push to Github which is why we do not provide them in this repository. In the main directory, we do include a file for DST changes:

`DaylightSavingsTimeChangeDates_1971-2024.csv`


### Data_Scraping

This directory contains the files listed below. We focused on different sectors of the market (or Japan) and in these notebooks, scraped and preprocessed the data. These notebooks then produce .csv files which are used by the rest of the notebooks.

`consumer_scrape.ipynb`
`energy_scrape.ipynb`
`finance_scrape.ipynb`
`health_scrape.ipynb`
`japan_scrape.ipynb`
`nikkei_scrape.ipynb`
`tech_scrape.ipynb`
`transport_scrape.ipynb`

### Exploratory_Data_Analysis

These notebooks do some exploratory data analysis and visualization either by sector or even individual stocks.

`kaggle_exploration.ipynb`
`kaggle_sector_EDA.ipynb`
`kaggle_transportation.ipynb`
`nikkei_EDA.ipynb`

### Statistical Methods

In the main directory, we have a notebook that did all the statistical analysis such as running a Welch's t-test and power analysis:

`Statistical_Tests.ipynb`

### Classification_Exploration

The names of these files should explain their main purpose. We ran many different classifier models on the various sectors such as logistic regression, k-nearest neighbors, (balanced) decision tree, (balanced) random forest, (balanced) extra trees, and AdaBoosted trees/forests.

`ADABoost_Finance.ipynb`
`Logistic_Regression_Finance.ipynb`
`SVM_Finance.ipynb`
`SVM_lowerDim_Finance.ipynb`
`kaggle_consumer_classify.ipynb`
`kaggle_finance_classify.ipynb`
`kaggle_health_classify.ipynb`
`kaggle_tech_classify.ipynb`

The classifier showing the best performance is found in the following notebook in the main directory:

`BoostedDecistionTree_Classifier.ipynb`

### Trading_Strategies

We have a few notebooks dedicated to exploring some rudimentary trading strategies in an attempt to leverage DST weekends. This merits much further investigation but we include it here to show the initial steps.

`trading_strategy2_comparison.ipynb`
`trading_strategy2_preprocessing.ipynb`
`trading_strategy_comparison.ipynb`


### Miscellaneous

We also have one notebook in the main directory that does some rudimentary time series analysis of the finance sector.

`FinanceStock_TimeSeries.ipynb`
