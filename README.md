# DSCI 521: Data Analysis and Interpretation Final Project

## Financial Market Data Analysis and Interpretation

### Group 1 - Members
- Geoff Patton - gp495@drexel.edu
- Ananda Mahalingam - asm465@drexel.edu
- Fengtian Lu - fl373@drexel.edu
- Rohit Bhattacharya - rb689@drexel.edu

### Project Summary
Our appication will generate real-time and historical financial market data. Our data store is available to view in Google Drive: [Access Link](https://drive.google.com/drive/folders/1hgWRHwlC9thoPKd7-dRqEHTPGYv3LtUk?usp=sharing). It contains data from all S&P 500 companies. We use [Finnhub](https://finnhub.io/docs/api) as the source of our data. Below is a list of the data we generate for analysis:
  - __Candlestick Data:__ Daily candlestick data (OHLCV) for stocks.
   - `candlestick_data.csv`
 - __Company Surprise Earnings:__ Historical quarterly earnings containing expected and actual earnings
   - `surprise_earnings.csv`
 - __Recommendation Trends:__ The latest analyst recommendation trends for a company.
   - `recommendation_trends.csv`
 - __Insider Sentiment:__ Insider sentiment for companies using the Monthly Share Purchase Ratio (MSPR). To give investors a glimpse at what the executives are thinking about the stock price and valuation in the near future.
   - `insider_sentiment.csv`
 - __Insider Transactions:__ Insider transactions data sourced from Form 3,4,5, SEDI and relevant companies' filings.
   - `insider_transactions.csv`
 - __Social Media Sentiment:__ Social sentiment for stocks on Reddit and Twitter.
   - `social_media_sentiment.csv`
 - __Senate Lobbying Activities:__ List of reported lobbying activities in the Senate and the House.
   - `senate_lobbying.csv`

### Issues and Limitations:
 - Timeouts/Rate Limit:
   - 60 finnhub API calls/minute for each client
   - 300 google API Calls/minute
 - Our historical data is limited due to using a free version of finnhub

## Our Data
- Our data is available to view on a shared [Google Drive](https://drive.google.com/drive/folders/1hgWRHwlC9thoPKd7-dRqEHTPGYv3LtUk?usp=sharing)

## Running the Application
1. `project_1.ipynb`: this notebook will use the local CSV files to run the analysis


### Software Pre-requisites:
Install the following dependencies in the python environment.
```
pip install pandas
pip install finnhub-python
```

### Running with Visual Studio Code
1. Install or enable the Python and Jupyter extenstions
2. Open the `final_project_group_one.ipynb` jupyter notebook
3. Press `Run All` Button

### Running with jupyter notebook server
1. Run the `jupyter notebook` command in terminal from `dsci-511-project` directory
2. The notebook should open in your browser.
3. From the browser run all cells

> To run from server, jupyter must be installed: `pip install -U jupyter`


### Code Overview
Our jupyter notebooks are designed to iterate over a collection of stock symbols and will populate each one our datasets with the most up to date financial information provided from Finnhub. Our datasets are designed to allow additional entries to be added to them while maintaining all historical data that already exists and not allow duplicate entries.

### Defining Stock Symbols:
The last section of the notebook contains a hardcoded set of stock tickers that determines which financial data is generated.
