# Monte-Carlo

## Financial Planning

### Part 1 - Personal Finance Planner

This part allows uers to assess their personal finances. 
After importing the necessary libraries and enabling access to Alpaca Markets, we are setting the number of crypto assets that are held. In this case, 1.2 of Bitcoin and 5.3 of Ethereum.

<img width="142" alt="Screen Shot 2022-04-02 at 2 48 44 PM" src="https://user-images.githubusercontent.com/99091066/161397150-8e9ff4ed-c1d0-4c31-a368-ec2884db626b.png">

We then request the daily prices for both crypto assets and indent the data in a way that's easier to visualize and call specific information with.

<img width="523" alt="Screen Shot 2022-04-02 at 2 50 20 PM" src="https://user-images.githubusercontent.com/99091066/161397188-87dfd2dd-dad5-4284-9a73-1509da06df5b.png">

  > Example of Bitcoin shown above

As of April 2nd, 2022, the Bitcoin and Ethereum current prices can be seen below.

<img width="604" alt="Screen Shot 2022-04-02 at 2 55 30 PM" src="https://user-images.githubusercontent.com/99091066/161397398-c37adf01-e0c4-459c-be20-62982ce5b7de.png">

To find the current value of the portfolio, we multiply the current prices of both crypto assets, with the amount of each asset that we hold. The current portfolio value is $73,369.24. This can be further broken down : $55,016.40 value in Bitcoin, and $18,352.84 in Ethereum.

<img width="617" alt="Screen Shot 2022-04-02 at 2 58 49 PM" src="https://user-images.githubusercontent.com/99091066/161397498-1e41019d-b7ae-4448-8363-5c51a9112ae2.png">

<img width="366" alt="Screen Shot 2022-04-02 at 2 59 02 PM" src="https://user-images.githubusercontent.com/99091066/161397506-b164a4dd-0100-4dfd-a258-9a9c76b333e4.png">

#### Collect Crypto Price

The tickers we are analyzing are AGG (U.S Aggregate Bond ETF), and SPY (SPDR S&P 500 ETF Trust).

First, we set the variables for my_agg and my_spy and equate them to the amount of each that we hold. 200 and 50, respectively.

Using the Alpaca API, we fetch 1 year's worth of data, the range being (2021-03-25 to 2022-03-25), setting a limit for 1000.

To calculate the current value of the portfolio, we call the current price of each ticker and multiply those prices by our variable (my_agg and my_spy)

<img width="601" alt="Screen Shot 2022-04-02 at 3 06 21 PM" src="https://user-images.githubusercontent.com/99091066/161397717-3f6b779f-38c0-43f5-92fc-cef9d9a7aff7.png">

> The SPY portion of the portfolio is currently worth $22,634.50 while AGG is worth $21,220.00. The combined value of the portfolio is $43,854.50

### Savings Health Analysis



















