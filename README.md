# Market_Predictor_AI
Created for Major League Hacking, uses polynomial regression to predict future stock market values

#Inspiration
Predicting how the stock market will perform is one of the most difficult things to do. There are so many factors involved in the prediction – physical factors vs. psychological, rational and irrational behaviour, etc. All these aspects combine to make share prices volatile and very difficult to predict with a high degree of accuracy.

Can we use machine learning as a game changer in this domain? Using features like the latest announcements about an organization, their quarterly revenue results, etc., machine learning techniques have the potential to unearth patterns and insights we didn’t see before, and these can be used to make unerringly accurate predictions. Inspired by this challenge, I decided to create a machine learning model to predict stock prices for this financial themed hackathon.

#What it does
Big Board AI takes stock price vales from the last 5 years as its data training set, and utilizes a Long Short Term Memory neural network and a polynomial regression function, to predict stock market values. LSTMs are widely used for sequence prediction problems and have proven to be extremely effective. The reason they work so well is because LSTM is able to store past information that is important, and forget the information that is not. LSTM has three gates:

The input gate: The input gate adds information to the cell state The forget gate: It removes the information that is no longer required by the model The output gate: Output Gate at LSTM selects the information to be shown as output

In this case, the training data would be the stock price from the last 5 years (web scraped from robinhood's public domain). This alongside the polynomial regression function (of which the user can adjust the value of the nth power), would be the input layer.

Once the user has selected a ticker symbol and a value of n, the algorithm is run, and they are provided with a model that should be able to somewhat predict the stcok price for the respective ticker symbol for the next ten days.

#How I built it
The first step was the back-end development. I used the beautiful soup library to webscrape data for a large number of ticker symbols from the last 5 years. This was converted into a csv file using jupyter notebooks.

I went on to use streamlit to create the front-end UI. Once this was complete, I created the regression function and neural network. The LSTM model can be tuned for various parameters such as changing the number of LSTM layers, adding dropout value or increasing the number of epochs.

#Challenges I ran into
Given the time limit this was still an amateur neural network, and the results vary depending on the ticker selected. Of course stock market prediction is a huge industry, so a project created in such a short time frame would not be incredibly accurate.


