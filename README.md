# Mean-Variance-Optimization
For this assignment, each team will write a Python program that will take the stock price data inputs as provided in Canvas: Files: Models & Spreadsheets: MPT_MVO Models: Raw Adjusted Prices.  This contains price data for FB, GOOG, and JPM from 2015 to 2020.

Using this data, convert the prices to returns.  Then, present the following data in professional tabular format (note that the returns you are provided are a sample so use the appropriate formulas:

For each return series:
Average return 
Variance 
Standard deviation 
Covariance matrix of all the series 
You can use "brute force" methods with loops; but using matrices will greatly simplify your code and improve your processing speeds in general.

Next, query the user for the user's "current portfolio weights" for FB, GOOG, and JPM.  Make sure you have error handling to confirm that the weights sum to 1.  Compute and present the user portfolio's expected return and standard deviation.

Then, conduct a constrained portfolio optimization to produce and present the weight vectors and statistics of interest (expected return, variance, standard deviation, covariance) for the following portfolios:

Global Minimum Variance Portfolio  (min variance s.t. sum of weights = 1)
Maximum Return Portfolio (min variance s.t. expected return = return of highest returning asset AND sum of weights = 1)
Next, use these two portfolios to create an Efficient Frontier.   (Note:  Remember that the EF can be computed as a combination of these two portfolios above; OR you could "brute force" method again by just doing a variance minimization at each level of expected return (starting at the GMV)--its your choice). 

When you illustrate the Efficient Frontier (standard deviation the x axis, expected return on the y axis), make sure you also:

Illustrate a point where the user's current portfolio resides (this should show up in the interior of the EF).
Identify a point on the EF that has the same expected return as the user's portfolio but lower standard deviation.
Use some language to explain to the user why the EF portfolio that you identified is superior to their portfolio.

Finally, you will introduce a risk free rate (use 2.5% APR).  You will use this information to compute the Optimal Risky Portfolio (ORP) aka the "tangency portfolio" and the optimal Capital Allocation Line (CAL).

To compute the ORP, you are essentially doing another constrained optimization.  This time, you will find the ORP weight vector by maximizing the Sharpe Ratio (defined as (expected return - risk free rate)/standard deviation).  You may use the solution presented in the handout "Portfolio Theory with Matrix Algebra" (p. 24) or you can use another optimization procedure of your choice.

You will then re-draw the chart that has the EF, the user's portfolio, and the user's efficient portfolio, and overlay the following:

A highlighted point with the ORP (it should reside on the EF itself)
An optimal Capital Allocation Line (remember this is a straight line from the risk free y-intercept through the ORP and extended above).
Remember that the optimal CAL is computed by simply taking a portfolio combination of the ORP and the risk free rate as two new portfolios
So you can still use all the portfolio combination formulas from before, the only difference is that this will be a little easier since:
you'll have different weights for the ORP and the RF (still have to sum to 1), but the variance of the risk free rate is zero and the covariance between the risk free rate and the ORP will also be zero!
A highlighted point on the CAL that has the same Expected return as the user's portfolio (but should have significantly less standard deviation than the user's portfolio and should have less standard deviation than the previously identified point for the user's portfolio on the EF.
Report back to the user information on expected returns, standard deviation, and sharpe ratio in professional, comparative table format for each of the following:

User's original portfolio
"Improved" portfolio (the equivalent one on the EF)
"Optimal" portfolio (the equivalent one on the CAL)
If you did this correctly, the Sharpe Ratio of the Optimal > Improved > Original.

Provide a narrative that describes the improvement (by not only highlighting the comparative numerical Sharpe Ratios but also by explaining what the SR is in "plain language").  In this narrative, you could also compute and demonstrate how much the standard deviation is reduced (for the same return) and/or how much the expected return could be increased (for the same variance) by investing on the CML versus the original portfolio.

Each team will submit:  Python code (ipynb) and a PDF of a couple of trial runs (samples that you have done).  Make sure that the PDF is written in a memo format that looks professional (as if you were presenting to an employer).

