# Forecasting Volatility for Portfolio Optimization

In this project, I use deep learning to forecast volatility for six exchange-traded funds (ETFs).  I forecast volatility using two neural networks - a convolutional neural network and a long short term memory network.  
### Convolutional Neural Network Results
![cnn](https://user-images.githubusercontent.com/103140702/229381299-f9c63213-1e1b-4ecb-8e3f-929ba7b43156.png)

### Long Short Term Memory Network Results
![lstm](https://user-images.githubusercontent.com/103140702/229381301-a687cf42-5924-4715-a88d-270d5550f2d7.png)


Then, I construct a trading algorithm that uses the LSTM-predicted volatilities along with the Sharpe Ratio method of portfolio optimization to manage a portfolio composed of these six ETFs.  

For each day, the algorithm generates 100 random portfolio weights using the predicted asset volatilities, converted to one portfolio volatility.  

It chooses the combination of weights associated with the best expected return for the following trading day and rebalances the portfolio accordingly, buying and selling assets immediately before the end of each trading day.  

My algorithm gives a return of approximately 2% over the last trading year, compared to approximately -10% for the SP500.  
![SPY Returns - Robot Returns](https://user-images.githubusercontent.com/103140702/229381345-200d0c99-a12e-43aa-a324-14bd716a6ae0.png)
