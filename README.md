# Time Series Analysis &amp; Forecasting of GridTrades
GUI-assisted EDA &amp; visualization using DTale. 

## Introduction
The Historical Grid Trade Master Agreements (GTMA) data is accessed from https://data.nationalgrideso.com/, the data portal of the UK National Grid ESO (UK NGESO). This project is **supported by National Grid ESO Open Data**.
The GTMA's represent the planned trades that the UK NGESO conducts to maintain grid balance where there is a foreseen energy requirement. Aside from ensuring system security where there is constraints, this function helps to keep the balancing mechanism at minimum cost. 

Visuallizations are mostly done through DTale and plotly graphic objects. The mean arctangent absolute percentage error is the criterion for model evaluation, due to the transformed target feature, Cost, having zero and negative values.

### Objectives
* Practice time series analysis on real-world data, from data preprocessing up until forecasting.
* Practice GUI-assisted EDA &amp; visualization using DTale.
* Practice SARIMA model optimization with pmdARIMA.

## Outline
1. Data Preprocessing & Feature Engineering -- Loads dataframes as downloaded from NG ESO data portal. Uses DTale for EDA and visuallization. Assigns new Start & End Dates as parsed from original data. Splits the dataset into two major categories: System Trades and Energy Trades.

2. Trend & Seasonality Decomposition -- Trend & Seasonality Decomposition using LOESS, and anomaly detection through residuals analysis. Insight gathered here is basis for long-term forecasting in the following notebooks.  
 
3. Forecasting with ExponentialSmoothing -- Resamples data in daily frequencies, then scales it through a Yeo-Johnson power transformer. Defines the train & test dataframes through a dictionary, and a specified forecast period, respectively.
   
4. Forecasting with pmdARIMA -- Data is similar to previous notebook **EXCEPT** by resampling the data in **monthly** frequencies. Automates selection of best model from a range of p, d, q, P, D, and Q values, in a manner similar to grid-search; with AICC as the optimization criterion.

## Notes
* Variables naming convention -- First, by describing what they are, and then their specifics follow. Ex.: df_train for a *dataframe* of the *train* dataset; model_arima_enrM_101  for an *ARIMA model* of the *Energy Trades* dataset *resampled Monthly*, with order *(101)*.
* Comments format -- Based on the "Better Comments" VSC plugin; [aaron-bond.better-comments].
* requirements.txt -- To follow.

## References
1.) UK National Grid ESO -- Historic GTMA data is from https://data.nationalgrideso.com/. This project is **supported by National Grid ESO Open Data**. Refer to National Grid ESO Open Data Licence v1.0., https://data.nationalgrideso.com/licence.

2.) Dtale --  https://dtale.readthedocs.io/en/latest/

3.) MAAPE -- "Thus, MAAPE is scale-independent, can be interpreted intuitively as an absolute percentage error, and is simple to calculate." [https://www.sciencedirect.com/science/article/pii/S0169207016000121]

4.) Forecasting metrics -- forecasting_metrics.py, https://gist.github.com/bshishov/5dc237f59f019b26145648e2124ca1c9

5.) Krish Naik, github -- https://github.com/krishnaik06/ARIMA-And-Seasonal-ARIMA/blob/master/Untitled.ipynb

6.) Auto-ARIMA -- https://www.alldatascience.com/time-series/forecasting-time-series-with-auto-arima/

7.) Seasonal Random Trend, Identifying ARIMA orders -- https://people.duke.edu/~rnau/411seart.htm

8.) Ritvikmath -- https://www.youtube.com/c/ritvikmath