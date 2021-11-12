---
header:
  teaser: /assets/images/test.png
title: 'Initial Dissertation Proposal'
categories:
  - Dissertation
tags:
  - Dissertation Proposal
year:
  - 2021
---

**_Can machine learning improve on standard portfolio construction techniques?_**

<b>Motivation</b>

Numerous papers have focused on applying machine learning techniques to improve on trend following systems for various asset classes (e.g. stocks, commodities). However, one important consideration in the construction of portfolios is the diversity of asset classes, which is a key component in diversifying the portfolio risk. Little research has been done on applying machine learning to improve on standard portfolio construction techniques (such as the Permanent Portfolio, Most Diversified Portfolio), which is the main goal of this paper. The section below outlines some notable research in this area.

<b>Previous Studies</b>

One of most distinguished papers in portfolio construction is the Markowitz portfolio theory, which allocates assets to a portfolio by applying mean-variance optimization. However, following the 2008-09 financial crisis the Markowitz's mean–variance portfolio theory has been criticized due to the change in correlation between securities (correlation goes up during crises, because all securities are correlated to widespread market events). Alternative models are the Black-Litterman model, and Sharpe’s Simplified Model of Portfolio Theory model, which are going to be explored in the current project. From a machine learning perspective, Kar Yan Tam [1] has previously used decision tree learning for portfolio construction to screen stocks before adding them to the portfolio. Tam’s method analyses individual stocks before adding them to a portfolio, whereas the purpose of this project is to combine different assets / assets classes and maximize portfolio performance by determining the optimal asset allocation. Another interesting paper was the application of genetic algorithms by Joglekar, which was able to develop a ‘fit’ portfolio from a pool of available stocks

<b>Goal and objectives</b>

The goal of this project is to apply different machine learning techniques to optimize the allocation of asset classes in a portfolio, and compare the performance of the resulting portfolios with standard portfolios (such as the Permanent Portfolio).

During the construction and analysis of portfolios, the following constraints will be applied:

    No trading costs
    Infrequent rebalancing of the portfolio (no less than 3 months)
    No short-selling allowed

In order to construct and analyse the performance of the portfolios, the following metrics will be used (presented in the order of importance):

    Sharpe Ratio, which describes the performance of a portfolio accounting for the risk of the portfolio Sortino Ratio
    MAR Ratio, which divides the CAGR (compound annual growth rate) since inception by the biggest drawdown
    VAR (value at risk), which quantifies the risk of loss of a certain portfolio
    Expected Tail Loss, which quantifies the market risk of a portfolio

This project will focus on optimizing the portfolio asset allocation for the following asset classes:

    Stocks (focusing primarily on the stocks included in the FTSE350, S&P500)
    Bonds
    Currencies
    Commodities (primarily gold, but other commodities can be considered based on the availability of data)

<b>Method:</b>

For this project the application of the Hidden Markov Model as well as Bayesian approaches will be investigated. The data required for the project will be acquired from the following sources:

    Stocks: https://finance.yahoo.com/stock-center/
    Bonds (US T-Bills, BoE Euro Bills), Gold price, Currency rates: http://www.bankofengland.co.uk/boeapps/iadb/index.asp?SectionRequired=I&first=yes&HideNums=-1&ExtraInfo=true&Travel=NIxIRx&levels=1

<b>References</b>

[1] – “Inducing Stock Screening Rules for Portfolio Construction” Author(s): Kar Yan Tam, Melody Y. Kiang and Robert T. H. Chi, Source: The Journal of the Operational Research Society,Vol. 42, No. 9 (Sep., 1991), pp. 747-757

[2] – “Two-Stage Stock Portfolio Construction: Correlation Clustering and Genetic Optimization” Author(s) Sachin Joglekar

<b>Other resources</b>

    Honey, I Shrunk the Sample Covariance Matrix, Author(s): Olivier Ledoit and Michael Wolf, Source: No 92, Working Papers from Barcelona Graduate School of Economics

    Financial Risk Forecasting: The Theory and Practice of Forecasting Market Risk with Implementation in R and Matlab by Jon Danielsson, Available on: http://www.amazon.co.uk/Financial-Risk-Forecasting-Practice-Implementation/dp/0470669438

    Risk Management and Financial Institutions Paperback by John C. Hull, Available on: http://www.amazon.co.uk/Risk-Management-Financial-Institutions-John/dp/0138006172

    Risk and Asset Allocation by Attilio Meucci, Available on: http://www.amazon.co.uk/Asset- Allocation-Springer-Finance-Textbooks/dp/3642009646/

    Portfolio Management under Stress: A Bayesian-Net Approach to Coherent Asset Allocation by Riccardo Rebonato, Available on; http://www.amazon.co.uk/Portfolio-Management-under- Stress-Bayesian-Net/dp/1107048117
