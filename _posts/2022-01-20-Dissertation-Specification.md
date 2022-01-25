---
header:
  teaser: /assets/images/test.png
title: 'Dissertation Specification'
categories:
  - Dissertation
tags:
  - Work in Progress
  - Project Core
year:
  - 2021
---

[**Link To Overleaf Latex Document**](https://www.overleaf.com/project/618a3a79fcff59129dec027c)

**Project Question**

_Can machine learning improve on standard portfolio construction techniques?_

**Project Goal**

  _The goal of this project is to apply different machine learning techniques to optimize the allocation of asset classes in a portfolio, and compare the  performance of the resulting portfolios with standard portfolios (such as the Permanent Portfolio)_.

**What data will I use?**

I'll be using data starting from 2012-02-14 for now till the latest data.

_Asset Classes_


* _Goverment Bonds_
  * iShares U.S. Treasury Bond ETF ([GOVT](https://finance.yahoo.com/quote/GOVT?p=GOVT&.tsrc=fin-srch "Yahoo Finance Stock")) -> Exposure to U.S. Treasuries ranging from 1-30 year maturities

  * iShares International Treasury Bond ETF ([IGOV](https://finance.yahoo.com/quote/IGOV?p=IGOV&.tsrc=fin-srch "Yahoo Finance Stock")) -> international treasury market ETF excluding the US

* _Stocks_

  * _Large Cap_
    * S&P 500 ([ ^GSPC](https://finance.yahoo.com/quote/%5EGSPC?p=^GSPC&.tsrc=fin-srch "Yahoo Finance Stock")) -> gauge of the US large-cap equities 
    * FTSE 350 ([ ^FTLC](https://finance.yahoo.com/quote/%5EFTLC?p=^FTLC&.tsrc=fin-srch "Yahoo Finance Stock")) -> market capitalisation weighted stock market index made up of london stock exchange 350 biggest companies

  * _Small Cap to Mid Cap_
    * Russell 2000 ([ ^RUT](https://finance.yahoo.com/quote/%5ERUT?p=^RUT&.tsrc=fin-srch "Yahoo Finance Stock"))
    * iShares MSCI Europe Small-Cap ETF ([IEUS](https://finance.yahoo.com/quote/IEUS?p=IEUS&.tsrc=fin-srch "Yahoo Finance Stock"))


* _Commodities_
  * Aberdeen Standard Physical Silver Shares ETF ([SIVR](https://finance.yahoo.com/quote/SIVR?p=SIVR&.tsrc=fin-srch "Yahoo Finance Stock"))
  * Aberdeen Standard Gold ETF Trust ([SGOL](https://finance.yahoo.com/quote/SGOL?p=SGOL&.tsrc=fin-srch "Yahoo Finance Stock"))

**What are the objectives?**

  We are trying to see if machine learning in asset optimisation in a portfolio actually improves portfolio's performance. Our focus is asset optimisation, so that's what we will be varying and seeing the effect of. We will be using different machine learning methods to decide on the asset allocation. How good these methods are at asset optimisation will be what determines the performance of the portfolio. We'll need to compare it to a benchmark like the Permenant Portfolio which is basically equal allocation of the different asset classes. 
  
  I think by performance we usually refer to maximising profit within an acceptable risk level. Will need to find a proper definition.

  [Performance measure](https://www.investopedia.com/articles/08/performance-measure.asp)

  We will measure performance of a portfolio using the following measures:

  * Sharpe Ratio, which describes the performance of a portfolio accounting for the risk of the portfolio Sortino Ratio
  * MAR Ratio, which divides the CAGR (compound annual growth rate) since inception by the biggest drawdown
  * VAR (value at risk), which quantifies the risk of loss of a certain portfolio
  * Expected Tail Loss, which quantifies the market risk of a portfolio

  These were the standard ones suggested to me for use. I'll be looking at what other people are using in their 
  papers to compare measure performance, so this list might expand.


**What methods?**

  Are we going neural network route here or just pure machine learning?
  How exactly are we going to be picking the assets. What about asset breakdown. How do we know which exact asset from an asset group we are picking?

  The 2 main ones reccomended were:
  * Hidden Markov Model
    * Markov Chains
      Consists of a state space and a probability transition function
    * How would you use this to predict the asset allocation? I can predict future price, but how to go about the asset allocation prediction? Would you just create a hidden markov model for each of the 8 assets I've chosen and then simply predict the future price. Then using the future price prediction to figure out the best portfolio weights to keep in that period. This would involve multiple models to do though.
  * Bayesian approaches
    * Bayesian approaches is to do with probablities. Prio probablities and the like used to predict
    * Linear Regression is one of the approaches
    * Not a 100% sure what the Bayesian approaches work, will be doing some extra reseach on this
      * (Paper on this) Application of Bayesian Regression Model in Financial Stock Market Forecasting - Xuejun Zhao
  * Could add a simple deeplearning technique to this as well
  * Fourier transform? (We'll see)
  * A time series can be modeled as a seq2seq problem

  How in general are we optimising? Shaprie Ratio or something else? Are we doing something like mean-variance analysis?

**Some Info on Retrictions, Constraints and Methodology?**

We'll be starting off with $100'000

During the construction and analysis of portfolios, the following constraints will be applied:

    No trading costs
        Explicit costs like commisions, fees, taxes
    Infrequent rebalancing of the portfolio (no less than 3 months)
    No short-selling allowed
    

Trading strategy - Buy and hold with rebalancing every 6 months/ A passive portfolio management strategy