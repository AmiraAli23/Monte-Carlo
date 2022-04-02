# Monte-Carlo

## Financial Planning

### Part 1 - Personal Finance Planner

This part allows users to assess their personal finances. 
After importing the necessary libraries and enabling access to the Alpaca Markets API, we set the number of crypto assets that are held. In this case, 1.2 of Bitcoin and 5.3 of Ethereum.

<img width="142" alt="Screen Shot 2022-04-02 at 2 48 44 PM" src="https://user-images.githubusercontent.com/99091066/161397150-8e9ff4ed-c1d0-4c31-a368-ec2884db626b.png">

We then requested the daily prices for both crypto assets, and indented the data in a way that is easier to visualize and call specific information with.

<img width="523" alt="Screen Shot 2022-04-02 at 2 50 20 PM" src="https://user-images.githubusercontent.com/99091066/161397188-87dfd2dd-dad5-4284-9a73-1509da06df5b.png">

  > Example of Bitcoin shown above

As of April 2nd, 2022, the current Bitcoin and Ethereum prices can be seen below.

<img width="604" alt="Screen Shot 2022-04-02 at 2 55 30 PM" src="https://user-images.githubusercontent.com/99091066/161397398-c37adf01-e0c4-459c-be20-62982ce5b7de.png">

To find the current value of the portfolio, we multiply the current prices of both crypto assets, with the amount of each asset that we hold. The current portfolio value is `$73,369.24`. This can be further broken down: `$55,016.40` value in Bitcoin, and `$18,352.84` in Ethereum.

<img width="617" alt="Screen Shot 2022-04-02 at 2 58 49 PM" src="https://user-images.githubusercontent.com/99091066/161397498-1e41019d-b7ae-4448-8363-5c51a9112ae2.png">

<img width="366" alt="Screen Shot 2022-04-02 at 2 59 02 PM" src="https://user-images.githubusercontent.com/99091066/161397506-b164a4dd-0100-4dfd-a258-9a9c76b333e4.png">

#### Collect Crypto Price

The tickers we are analyzing are AGG (U.S Aggregate Bond ETF), and SPY (SPDR S&P 500 ETF Trust).

First, we set the variables for `my_agg` and `my_spy` and equate them to the amount of each that we hold, which is 200 and 50, respectively.

Using the Alpaca API, we fetch 1 year's worth of data, ranging from (2021-03-25 to 2022-03-25), and set a limit for 1000.

To calculate the current value of the portfolio, we call the current price of each ticker and multiply those prices by our variables (`my_agg` and `my_spy`)

<img width="601" alt="Screen Shot 2022-04-02 at 3 06 21 PM" src="https://user-images.githubusercontent.com/99091066/161397717-3f6b779f-38c0-43f5-92fc-cef9d9a7aff7.png">

> The SPY portion of the portfolio is currently worth `$22,634.50` while AGG is worth `$21,220.00`. The combined value of the portfolio is `$43,854.50`.

### Savings Health Analysis

We will now analyze our total crypto and share values, and visualize each on a pie chart. 


<img width="523" alt="Screen Shot 2022-04-02 at 3 41 27 PM" src="https://user-images.githubusercontent.com/99091066/161398689-af044eac-6475-44c5-b472-becb74995f2e.png">

Assuming the monthly income is $12,000, and the emergency fund is equal to three times the monthly income, we calculated the total savings, and constructed an "if statement" to generate a statement depending on if the emergency funds are available. 

In this case, the total savings amounted to `$117,223.74`

<img width="533" alt="Screen Shot 2022-04-02 at 3 43 53 PM" src="https://user-images.githubusercontent.com/99091066/161398777-70a537d4-642c-4b6a-bc2b-180714a534d4.png">

> Since our savings are greater than the emergency funds, `$36,000`, the code generated the statement above. 

## Part 2 - Retirement Planning

For the Monte Carlo simulation, I pulled 5 years of data for AGG and SPY, and then combined the two dataframes together. After importing the MCForecastTools file that can be found [here](https://github.com/AmiraAli23/Monte-Carlo/blob/52012bab5f26f872d3d7e0b88698599ff5bf144c/MCForecastTools.py), I ran a simulation given the portfolio data, weights (0.4 for AGG and 0.6 for SPY), for 500 runs and 7560 trading days (30 years).

<img width="517" alt="Screen Shot 2022-04-02 at 4 07 20 PM" src="https://user-images.githubusercontent.com/99091066/161399473-f95a388f-8501-4fc4-b6ca-3e4259396c1c.png">

> These are the visualized cumulative portfolio return trajectories.



<img width="529" alt="Screen Shot 2022-04-02 at 4 11 24 PM" src="https://user-images.githubusercontent.com/99091066/161399582-4e52db5b-ff57-4699-b3e7-a4e207276bd9.png">

> Above is the probability distribution and confidence intervals. 



<img width="419" alt="Screen Shot 2022-04-02 at 4 13 14 PM" src="https://user-images.githubusercontent.com/99091066/161399625-1ef84936-8d2d-426d-bd29-0be78c36bbec.png">

Using the summary statistics in the table above, we can calculate with 95% confidence, that an initial investment of $20,000 can become within the range of $75,550.28 and $1,026,629.45 in 30 years.

If this initital investment were to increase by 50%, to $30,000, we can say with 95% confidence that the value in 30 years will be between $113,325.42 and $1,539,944.17.

