---
header:
  teaser: /assets/images/test.png
title: 'Project Specification'
categories:
  - Dissertation
tags:
  - Work in Progress
  - Project Core
year:
  - 2021
---
# Work in Progress

  Mostly contains some notes and general questions about certain areas in the project speficiation

[**Link To Overleaf Latex Document**](https://www.overleaf.com/project/618a3a79fcff59129dec027c)

**Project Question**

_Can machine learning improve on standard portfolio construction techniques?_

**Project Goal**

  _The goal of this project is to apply different machine learning techniques to optimize the allocation of asset classes in a portfolio, and compare the performance of the resulting portfolios with standard portfolios (such as the Permanent Portfolio)_.

**What data will I use?**

  I'm not sure about the timeframe for the stockmarket that I should be looking at. The 2 majour crashes of the stock market were the dot-com bubble crash and the 2008 financial crisis. Then most recent effect on the stock market would be covid.

  Also what currencry will we want to be doing the evaluation in?

  I will be looking at the following asset classes: 
  * Stocks (focusing primarily on the stocks included in the FTSE350(UK), S&P500(US))
    * Will we be comparing the stock performance against the indexes?
    * [S&P 500](https://finance.yahoo.com/quote/%5EGSPC?p=%5EGSPC) general index on yahoo has data since 1927. The companies in the indexes do change
    * [FTSE 350](https://finance.yahoo.com/quote/%5EFTLC?p=^FTLC&.tsrc=fin-srch) general index on yahoo has data since 1986.
    * Are we just buying individual stocks here? What about something like index funds?
  * Bonds
    * Are we looking at just the US bonds or EU as well?
      * Hmm, what market in general will we be focusing on?
    * [US Treasury Bill results](https://www.bankofengland.co.uk/boeapps/database/FromShowColumns.asp?Travel=NIxIRxSUx&searchText=US+Treasury+Bills) Not sure what data from this we care about. Not sure how we are evaluating bonds in general.
    * [Euro Bills](https://www.bankofengland.co.uk/boeapps/database/FromShowColumns.asp?Travel=NIxIRxSUx&searchText=Euro+bills) Again not sure what we care about with these.
  * Currencies
    * What are the standard currencies people are looking at? I'm guessing dollars, euros, maybe pounds, but not sure about others.
  * Commodities (primarily gold, but other commodities can be considered based on the availability of data)
    * [Gold](https://www.bankofengland.co.uk/boeapps/database/FromShowColumns.asp?Travel=NIxIRxSUx&searchText=Gold)
      * Do we care about monthly average or the end of month price
  
  We have asset classes, but how will we choose which asset we will pick from it? The asset class options are a bit arbritary at the moment.

**What are the objectives?**

  We are trying to see if machine learning in asset optimisation in a portfolio actually improves portfolio's performance. Our focus is asset optimisation, so that's what we will be varying and seeing the effect of. We will be using different machine learning methods to decide on the asset allocation. How good these methods are at asset optimisation will be what determines the performance of the portfolio. We'll need to compare it to a benchmark like the Permenant Portfolio which is basically equal allocation of the different asset classes. 
  
  I think by performance we usually refer to maximising profit within an acceptable risk level. Will need to find a proper definition.

  We will measure performance of a portfolio using the following measures:

  * Sharpe Ratio, which describes the performance of a portfolio accounting for the risk of the portfolio Sortino Ratio
  * MAR Ratio, which divides the CAGR (compound annual growth rate) since inception by the biggest drawdown
  * VAR (value at risk), which quantifies the risk of loss of a certain portfolio
  * Expected Tail Loss, which quantifies the market risk of a portfolio

  These were the standard ones suggested to me for use. I'll be looking at what other people are using in their papers to compare measure performance, so this list might expand.

**What methods?**

  Are we going neural network route here or just pure machine learning?
  How exactly are we going to be picking the assets. What about asset breakdown. How do we know which exact asset from an asset group we are picking?

  The 2 main ones reccomended were:
  * Hidden Markov Model
    * Markov Chains
      Consists of a state space and a probability transition function
  * Bayesian approaches
    * Linear Regression is one of the approaches
    * Not a 100% sure what the Bayesian approaches are. Will be doing extra reading on this.


