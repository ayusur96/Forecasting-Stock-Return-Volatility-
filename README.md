# Forecasting-Stock-Return-Volatility-
Aim of this project: Apply at least three out of five techniques illustrated in the course (Deep Neural Network; Cross-validation; Ensemble Model; Autoencoder; Interpretability) to sovle a financial problem.

Topic
Can we use deep neural network to forecast the stock return volatility? Which model provides the best forcasting performance?

Data
In computer lab_3_1, we show the method to download stock prices from Yahoo Finance. This topic uses the stock adjusted prices to calculate its volatility (use the standard deviation of the past 30-day arithmetic return as the volatility).

Method
The features include the downloaded five columns of Open, High, Low, Close, and Adj Close and the calculated arithmetic return and current volatility. We may model the seven features as multi-dimensional time series to forecast the future volatility over 𝐻 future horizons (𝐻 ≥ 1). The features can be defined as a vector.

𝐗𝑡 = (𝑂𝑡, 𝐻𝑡, 𝐿𝑡, 𝐶𝑙𝑜𝑠𝑒𝑡, 𝐴𝑑𝑗𝐶𝑙𝑜𝑠𝑒𝑡, 𝑟𝑡 ,𝑉𝑂𝐿𝑡)T
This project is to estimate the function 𝑓(∙), that takes a sequence of historical 𝐗𝑡 as input and generates vector 𝐕𝐎𝐋𝑡 = (𝐕𝐎𝐋𝑡, 1, … , 𝐕𝐎𝐋𝑡, 𝐻)𝑇 as output:

𝐕𝐎𝐋𝑡 = 𝑓(𝐗𝑡, 𝐗𝑡−1, 𝐗𝑡−2, … , 𝐗𝑡−𝑾).
Where 𝑾 is the look back window, 𝑗 = 1, … , 𝐻.

This topic shall use LSTM as one of the potential models. You may try to train the LSTM model with the raw 7-dimension features 𝐗𝑡 with different 𝑾. You may also extract the features with lower dimensions 𝑀 < 7 by autoencoder and then train the LSTM model using the extracted features with different 𝑾. You can provide a comparison of those two methods.

This topic may also answer what look back window 𝑾 and horizon 𝐻 generate the best forecasting results.
