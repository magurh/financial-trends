# MemeStocks

I recently looked at the whole ‘meme stock saga’ 💎, popularized on some subreddits from early 2021. While I’m not trying to explain what happened back then, I think that an analysis of the stock price is actually rather interesting. 

### Context

Let me start by giving you a bit more context: in the early days of 2021, a certain large hedge fund opened a short position against GameStop, which was still suffering from the effects of the pandemic. The stock price was around $7 at that point, but by the end of January, it reached a whopping $483, roughly a 6800% price increase in only a few days. 🕐 

(The stock underwent a stock split, which is why the price appears slightly different in the TradingView plot.)

This fast price increase is called a ‘short squeeze’, and is due to an excess of short selling of a stock. In theory, the short sellers were trying to buy back the stock after something triggered the stock price to go against their initial expectations.
 
<p align="center">
  <img src="https://github.com/magurh/MemeStocks/assets/122356566/5ca5754b-fd79-4c84-a1fc-19dbec1b2c7e">
</p>

Such events already happened in the past, like the somewhat famous squeeze of Volkswagen in 2008, when the stock price increased by 5 times in about two days. This was largely due to Porsche acquiring a large stake in the VW company (roughly 40% at the time), with the German government also having a 20% stake. This meant that only a small percentage of shares was actually available for traders and thus people started covering their short positions, ultimately leading to the short squeeze.
 
GameStop and the other ‘meme’ stocks (AMC, BB), were, however, not in the same position as VW in 2008. They were all still struggling after the pandemic and probably not many people saw the squeeze coming. A very interesting Reddit sentiment analysis was done in a recent paper from October 2022: https://onlinelibrary.wiley.com/doi/epdf/10.1111/fire.12328.


### Stock price analys

The stock price analysis that I will be doing is be based on the Security Market Line, which a linear model between stock returns and a ‘market portfolio’, for which I will be using the S&P 500 index. From my experience, this model works better for monthly returns, as it eliminates possible daily outliers. Note that by using this model instead of simply considering the stock returns, we automatically look for excess returns besides the market trend. 📈

A scatter plot for the GME vs S&P 500 returns is shown in the plot below. 

<p align="center">
  <img src="https://github.com/magurh/MemeStocks/assets/122356566/9336511b-2488-4c09-9d01-62b959a6cf8d">
</p>

What we notice is that the linear model would be a very decent approximation, if it weren’t for the one outlier in the data, which corresponds to the month of January 2021! Outliers are typically detected in residual plots (residuals are the difference between the stock returns and the values predicted by the model). To compare the residuals across different stocks, I will normalize the residuals, such that they have unit variance – so it is less and less likely that values of +1, +2, +3 (and so on) will be seen.

The standardized residual for the GME returns in January 2021 reaches a value of 7.42! 🚀 This is particularly impressive, since the returns are averaged over a whole month, which would normally eliminate daily outliers, as previously alluded to. While this linear model does not capture all the intricacies of the stock market, I would still like to see how the GME results compare to other stocks. Looking, for instance at all S&P 500 stocks, I found some outliers for APA (5.9) and EQT (4.46), while all the other stocks have values of at most around 4 or much lower. APA and EQT are both in the Energy sector and the outliers correspond to April 2020, which is the first month after the covid market crash, when the whole sector (tracked by the XLE index) experienced some wild fluctuations. ⚡

It is fair to say, however, that a comparison of GME with S&P 500 stocks might not be very reliable, as the market cap of GME at the beginning of 2021 was only $1.3B, compared to the minimum requirement for the S&P 500, which is now $13.1B. Hence, it is perhaps more reasonable to compare the stock with the other components of the Russell 2000 index, of which GME was part until June 2021, when it was upgraded to Russell 1000. The results are shown in the second attached plot, where now we have some other outliers of comparable size, showing thus that the GME surge is not quite unique!

<p align="center">
  <img src="https://github.com/magurh/MemeStocks/assets/122356566/b58ab434-3641-424d-bc0f-a0232ad53839">
</p>

The case of PHUN is very interesting, as it appears to have had monthly returns even greater than GME at its peak. The PHUN stock price surged by 2000% after going public in early 2019, on the back of excitement about blockchain technology and cryptocurrency. See https://www.fool.com/investing/2019/02/11/how-phunware-shares-gained-nearly-2000-in-january.aspx, for instance, for more details.

