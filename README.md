# S-P-Stock-Prediction

This project is a data-driven exploration and prediction project focused on the S&P 500 index. S&P 500 dataset contains historical stock prices (last 5 years) for all companies currently found on the S&P 500 index. This project harnesses historical stock data, collected and analyzed using Python libraries such as yfinance, pandas, and machine learning techniques. The aim is to uncover insights into stock behavior and create a predictive model capable of anticipating future price movements.

----------------

## Data Visualisation
### Collecting and Preparing Data
In this section, we collect historical stock data for the S&P 500 index using the Yahoo Finance API (yfinance). The data is then cleaned and prepared for analysis. Unnecessary columns such as dividends and stock splits are removed, and a new column, "Tomorrow," is created by shifting the closing prices by one day.

To focus on a specific timeframe, we filter the data to include only records after January 1, 1990. Subsequently, we create additional columns to aid in our analysis. The "Increase_Decrease" column signifies whether the volume increased or decreased from one day to the next, and the "Buy_Sell_on_Open" and "Buy_Sell" columns indicate potential buy or sell signals based on open and close prices, respectively. The "Returns" column represents the percentage change in closing prices.

### Visualizing Stock Data
We leverage various data visualization techniques to gain insights into the stock data. Line plots are employed to visualize the closing prices over time, while additional line plots with color differentiation illustrate volume increases and decreases. A count plot provides a clear view of the distribution of volume changes, aiding in understanding the frequency of increases and decreases.

Scatter plots and regression plots help explore relationships between open and close prices. Box plots with strip plots highlight the distribution of closing prices based on volume changes, offering insights into potential patterns.

The visualizations extend to joint plots and FacetGrids, providing comprehensive views of bivariate relationships and allowing for the exploration of stock data patterns. These visualizations are essential in understanding historical trends, potential signals, and the overall behavior of the S&P 500 index.

## Stock Prediction
### Making Predictions
In this section, stock prices are predicted using machine learning. The target variable, "Target," is created by comparing the closing price of the current day with that of the next day. If the closing price increases, the target is set to 1 (Yes), otherwise 0 (No). This binary classification sets the stage for predicting whether the stock price will rise or fall based on historical data.

### Model Evaluation
The performance of the model is assessed using a classification report, providing precision, recall, and F1-score for each class (No and Yes). The report offers insights into the model's ability to correctly predict positive and negative instances.

### Prediction Function
A prediction function is defined to streamline the process of using the trained model on new data. This function takes the model, training set, testing set, and predictor variables as input, providing a series of predicted values for comparison with the actual target values.

The ultimate aim of this project is to leverage historical stock data to create a predictive model capable of anticipating whether the stock price will increase or decrease on the following day. This predictive capability has valuable applications for traders and investors seeking informed decision-making based on historical trends and patterns.


## Code
All the code can be found in Data_visualisation.ipynb and Stock_prediction.ipynb files.
