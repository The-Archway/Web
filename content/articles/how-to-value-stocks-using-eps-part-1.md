# Valuing Stocks Using EPS
For the sake of simplicity, there are two primary methods of valuing a company's stock price. One method uses the **dividend discount model** (which will be covered in a later article), and the other uses the **earning per share model**. The focus of this article will be on using a company's earnings to estimate its stock price, and then determine whether the current stock price is fairly valued, overvalued or undervalued.  

### Earnings
The first step of the EPS model is determining the earnings of a company. There is an old saying, "_past performance is no guarantee of future results_." So, what are we supposed to do? Unless you have a crystal ball, the easiest way to predict future performance is using a company's previous earnings. Let's take a look at the following imaginary company.  

>##### Acme Company
>|Year (TTM) | 2019  | 2018  | 2017  |
>|:---       |   ---:|   ---:|   ---:|
>|EPS        |  4.38 |  4.50 |  5.00 |

If you look at Acme Company's 10-K (its yearly SEC Filing), you will see the last three years' income statements. At a quick glance, it's easy to see a trend in Acme's earnings per share. For 2020, we could quickly estimate an EPS of roughly $4.00 per share. To arrive at our stock price, all we need to do is multiply our $4.00 per share by it's **Price to Earnings or PE ratio**. The **PE Ratio** represents how much per share of a company's stock that we are willing to pay for each dollar of earnings. Going back to our example, let's assume that Acme Company has a trailing twelve months (**TTM**) PE Ratio (multiple) of 25. We can now compute Acme Company's stock price: $4 x 25 = $100 per share.  

Using a company's EPS from its 10-K is great, but what do we do if we are in the middle of the year? We would rather not wait an entire year to compute a company's stock price. Luckily, the SEC requires additional filings throughout the year. The second most commonly used filing is the 10-Q. A 10-Q is almost the same as a 10-K except that it is filed every _quarter_. This allows us to compute our stock price more frequently.   

Computing a company's stock price using a 10-Q is almost the same as a 10-K except it requires us to look at more than one document. The only real complication comes from Q4. Companies do not file a 10-Q in the fourth quarter - only a 10-K. So, we'll need to do a little math to figure out our Q4 EPS. To get our Q4 EPS, we'll need to subtract the sum of Q1-Q3 from the 10K of the same year. Let's take a look at our Acme Company.  

>##### Acme Company
>|Year (TTM) | 2019 (10-K)  | 2019 (Q3)  | 2019 (Q2)  | 2019 (Q1)  |
>|:---       |          ---:|        ---:|        ---:|        ---:|
>|EPS        |         4.38 |       0.58 |       1.34 |       1.40 |

Based on the table above, our Q4 EPS is 1.06. This is calculated using the following simple formula: Q4 = 4.38 - 0.58 - 1.34 - 1.40. Now, let's pretend we would like to compute the stock price of Acme Company for Q1 2020. All we need to do is add our estimate for Q1 to the previous three quarters. That calculation would look something like this: Q1 (estimate) + 1.06 (Q4 2019) + 0.58 (Q3 2019) + 1.34 (Q2 2019) = TTM EPS. We're simply adding the last three quarters' earnings to our estimate for the upcoming quarter to reach our trailing twelve months EPS. If the consensus estimate for Q1 is $1.25, the TTM EPS for Acme Company would be $4.23. Next, we just need to multiply our estimated TTM EPS by our PE Ratio (or multiple). This gives us a stock price of $105.75 ($4.23 x 25).  

Hopefully this article is able to clarify the basics of calculating a company's share price using its earnings per share. The next article will discuss the PE Ratio and which one to use.  

