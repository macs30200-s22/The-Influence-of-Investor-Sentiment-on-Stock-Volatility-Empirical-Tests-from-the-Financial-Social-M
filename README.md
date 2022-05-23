# The Influence of Investor Sentiment on Stock Volatility: Empirical Tests from the Financial Social Media Platform

## Project Workflow

The code is written in Python 3.8.12 and all of its dependencies can be installed by running the following in the terminal (with the `requirements.txt` file included in this repository):

```
pip install -r requirements.txt
```

### Step 1: Data Collection (in the folder `Data`)
- Social Media Data: 10 target companies' text data (posts). The data is in the folder `Data/scrapped_data`.
  - Using data crawler `scraper_stocktwits.ipynb`, collecting the data of each stock's posts, date, user id and trading decision from StockTwits.
- Stock Volatility Data (`VIX.csv`): VIX's historical data, which is downloaded from Yahoo Finance.
- Combined Data (`volatility_polarity.csv`): this dataset includes sentiment score and volatility.  

### Step 2: Sentiment Analysis
- Sentiment Analysis for this project uses Harvard IV-4 sentiment dictionary as frequency dictionaries by applying Python library `pysentiment2`.
  - Calculate each post's polarity by using `polarity_sentiment_analysis.ipynb`

### Step 3: Time Series Analysis
- The reseach involved Granger Causality Test and Vector Autoregression model to investigate the casual and correlation relation between investor sentiment and stock volatility. 
  - Data Analysis: `final_data_analysis_multivariable_30200.ipynb`

## Initial Findings
As the figures shown, the blue line represents the change of investor sentiment, and the red line represents the change of stock volatility. Compare with plots of GOOGL's sentiment scores and volatility in one month period, the plots shows both of them have similar trend and goes up in the end of the month. Based on data visualization, the result may prove the relationship between investor sentiment and stock volatility. For further findings,  I need to investigate more sentiment scores of stocks inclued in the VIX index.

![image](https://github.com/macs30200-s22/replication-materials-YLHan97/blob/main/Data%20Visualization/Granger_Causality_Test_Results(lag6-12).png）{:height="36px" width="36px"}

![image](https://github.com/macs30200-s22/replication-materials-YLHan97/blob/main/Data%20Visualization/Heatmap_for_Correlation_Matrix.png = 250x250)

![image](https://github.com/macs30200-s22/replication-materials-YLHan97/blob/main/Data%20Visualization/Feature_Correlating_with_Stock_Volatility.png = 250x250)

## How to Cite
```
@software{YLHan97,
  author       = {Yulun Han},
  title        = {macs30200-s22/replication-materials-YLHan97},
  month        = apr,
  year         = 2022,
  publisher    = {Github},
  journal      = {Github repository},
  howpublished = {\url{https://github.com/macs30200-s22/replication-materials-YLHan97}},
  commit       = {}
}
```
