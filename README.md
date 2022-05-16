# stock_price_prediction
Implementing a LSTM.nn to predict the future prices of an equity as my Capstone Project for my **Data Science Nanodegree Certification** at [Udacity](https://www.udacity.com)

![front_image](/Images/Front_image_readme_file.jpg)

## MY MOTIVATION FOR THIS PROJECT - _Business Understanding_

As an engineer, number lover, data scientist, and AI student, and as a young investor, I have always loved the idea of using my knowledge and understanding to predict the future prices of any stock traded on the stock market, if this were possible. My little experience in machine learning and deep learning algorithms, and the access that technology has given me to a vast amount of data related to these stocks, makes me believe that I can find that magic formula and predict prices in the future, and possibly have some benefit from it.

This idea to predict future prices or events of very important assets that follows a time series data structure, the kind of data I dealt with in this project, is widely researched and developed by the biggest funds and banks worldwide, whom invest a lot of money and resources in the search for the perfect signals to invest.

More than succeeding in this challenge and finishing my Data Science Course, I am very excited by all the experiences lived during this project, and the knowledge gained which definitely prepared me to improve this type of models or any other time series model in the future.


## LIBRARIES:

Please be sure to have already installed in your notebook environment the next libraries:

* numPy
* pandas
* requests
* time
* matplotlib
* torch
* os
* sklearn
* scipy
* statsmodels


## FILES IN THIS REPOSITORY:

- **Images** : folder with all the images and graphics saved by the jupyter notebook used for this Readme.me file and the blog where I publish this project.
- **Old** : folder with the initial exercises.
- **Final_Capstone_Stock_Pred.ipynb** : The jupyter notebook with all my final thoughts and practices.
- **AAPL_allf_1min** : The two years minute by minute data for AAPL stock price collected. You can collect the data or load this one with the functions provided in the notebook.
- **AAPL_allf_5min** : The two years every 5 minutes data for AAPL stock price collected. You can collect the data or load this one with the functions provided in the notebook.
- **AAPL_allf_30min** : The two years every 30 minutes data for AAPL stock price collected. You can collect the data or load this one with the functions provided in the notebook.
- **aapl_predicting_model_1minute.dat** : The initial trained model for 1 minute data.
- **aapl_predicting_model_5minute.dat** : The initial trained model for 5 minute data.
- **aapl_predicting_model_30minute.dat** : The initial trained model for 30 minute data.
- **aapl_predicting_fmodel_1minute.dat** : The final and succesful trained model for 1 minute data.


## THE DATA:

The data used in this project was collected thanks to the [Alpha_Vantage_API](https://www.alphavantage.co).

If you will collect the data from the source, you will need to create an Alpha Vantage Account and fill the API variable created for that purpose in the first cell of our notebook.

You can also avoid the collection with the '**_loading_**' function created.

The data downloaded comes with the OHLC prices information (Open, High, Low, Close) plus the volume info. The 'close' price data is already adjusted.

For our training purposes here, I only used the 'close' and 'volume' data, and two more features related to them.


## THE PROCESS:

The project here is divided in five big sections:

1. The global variables declaration, where I specified all the parameters to be involved in our trains.
2. Gathering and cleaning the data, where I start collecting and processing all the input data to our model.
3. Modeling, where I start with the process of creation of the LSTM model and start testing it.
4. Looking for Stationarity, a second part where we first deal with the stationarity need for our time series.
5. Final training, where we performed our final approaches for predicting the stock prices.
6. Other unsuccsesful trials performed.


## ABOUT THE METRICS INVOLVED

My initial approach was to predict the line of prices of a certain stock, in this case Apple Inc. The best netric to achieve a better model was the Mean Square Error (MSE), to measure how the new predicted price line differs or is separated from the original price line.

But when I realize that the model will not work as expected, and I change the approach to measure the MSE on the returns of that price line per every step to improve the model; the results, with some overfitting and bad testing errors, push me to find a metric that finds inside the results a signal that our model is learning, a little peace of information that show me that somehow I am in the right direction, and that metric was the Accuracy of the positive or negative momentums, or the accuracy of the signal of the momentum and not its magnitude.

In the stock market you can bet to win for positive returns and for negative returns as well. In this case, the returns data is very symmetric, meaning  have a symmetric distribution of true positives and true negatives, and also for false positive and false negatives. So, Accuracy will be enough to measure how truly are our momentum predictor.


## A BRIEF SUMMARY IN IMAGES:

Some images can help me to show you the process and the results achieved:

* The raw stock data downloaded:
![front_image](/Images/zoom1_close-volume-AAPL.jpg)

* The input features data to feed our model:
![front_image](/Images/CVMM_AAPL-data.jpg)

* The model:
![front_image](/Images/LSTM_nn.jpg)

* The first multiple approach training:
![front_image](/Images/MultiOptimizers_Train_AAPL.jpg)
![front_image](/Images/MultiOptimizers_Results_AAPL.jpg)

* The best predicted data with the best Adam model:
![front_image](/Images/Price_Prediction_AAPL.jpg)

* A closer look to the lag in the predicted and real data:
![front_image](/Images/Zoom_Predicted_Price_Test-Area_AAPL.jpg)

* The non-stationarity problem:
![front_image](/Images/First_ADF_AAPL_1min_SMA.jpg)
![front_image](/Images/Autocorrelation_1min_nonsta.jpg)

* The stationary approach:
![front_image](/Images/Final_ADF_AAPLE_1min.jpg)
![front_image](/Images/Autocorrelation_1min_stationary.jpg)

* The training with the new stationary data and returns:
![front_image](/Images/FInal_trainingloss_1min_sta.jpg)
![front_image](/Images/Final_testingloss_1min_sta.jpg)

* The final predicted returns with the last approach:
![front_image](/Images/Fnal_trainingloss_1min_sta.jpg)

* A closer look to that result:
![front_image](/Images/Final_predicted_return_training_1min_sta.jpg)
![front_image](/Images/Final_predicted_return_testing_1min_sta.jpg)

* A final and succesful accuracy of predicting the next minute momentum:
![front_image](/Images/Accuracy_stationary_only_regular_hours.jpg)


## ABOUT THE METRICS INVOLVED


The cases performed show different results that graphically don't allow me to conclude about the eficiency of the LSTM model I'm trying to implement. 

With those results, the forecast lines show erratic charts compared to the original price line.

That reason pushed me to look for a signal inside any of the results that would allow me to think that the model is learning; a piece of information that shows me that I am somehow heading in the right direction. 

That metric is the accuracy of the positive or negative pulses, or the accuracy of the momentum's signal without its magnitude.

In the stock market you can bet to win with positive returns and also with negative returns. In this case, the data is highly symmetric, meaning that it has a symmetric distribution of true positives and true negatives, and also of false positives and false negatives. Therefore, accuracy will be enough to measure how real our new momentum's predictor is; it will check how accurate the model was in predicting true positive or true negative momentums for the next minute or step.


## DELIVERING RESULTS AND THOUGHTS - _Deployment_

Finally, after all this process, you can find my deeper thoughts for this project in my blog:

[Stock Price Prediction…in the search of The Holy Grail.](https://carloslarocha.medium.com/stock-price-prediction-in-the-search-of-the-holy-grail-ea8523302f94)

Enjoy!

## LICENSING, AUTHORS, ACKNOWLEDGEMENTS

Thanks to ALpha Vantage for permititing us collect the price data ([licensed](https://www.alphavantage.co/terms_of_service/))

Thanks [Udacity](https://www.udacity.com) for the opportunity and such a great course.

And thanks to many other reasearchers and websites for sharing their knowledge:
  * [www.investopedia.com](https://www.investopedia.com)
  * [www.machinelearningmastery.com](https://machinelearningmastery.com)
  * [www.quantstart.com](https://www.quantstart.com)
  * among others

