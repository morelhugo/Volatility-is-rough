# Volatility-is-rough

Study on rough volatility : How to best estimate and forecast volatility for “high-frequency” data?

# Abstract

The purpose of this paper is to model volatility. Several previous papers have been written with this goal in mind but not all of them model it perfectly.

We can cite the paper by Dupire which models the volatility surface from the market prices of European vanilla options. It turns out that the modeling is inhomogeneous but also that the dynamics is very unrealistic which generates volatility surfaces is completely different from what can be observed.

Another type of volatility model is the stochastic volatility model with a continuous Brownian semi martingale like the Hull & White model or the Heston model. The dynamics are much more realistic than the local volatility model, but they do not correspond to observed European option prices.

What is being done a lot now is to use the local stochastic volatility (LSV) model which matches the market and generates similar dynamics.

The element that will allow us to understand the stochastic volatility is the fractional Brownian motion. Indeed, volatility is a long memory process and therefore in the literature we have several papers, including one that we will detail right after. This foundation paper is about uses fBM (fractional Brownian Motion) which allows to model a long memory by choosing a Hurst parameter H > 1⁄2.

The long memory process of the volatility process always has been largely accepted as a stylized fact. It first appeared that long memory referred to the slow decay of the autocorrelation function (anything slower than an exponential). However, the article quotes Rama Conte “the econometric debate on the short range or long-range nature of dependence in volatility still goes on (and may probably never be resolved)”. But for some time, it has appeared more as the fact that the autocorrelation function is not integrable and even more that it decays like a power law with an exponent less than 1. To be more specific, a weakly stationary process have a long memory if its ACF has a slow decay.

In this paper it is shown that the autocorrelation function of volatility does not have this form at the usual time scales, so they try to provide explicit expressions that allows to analyze the dependence structure of the volatility process.

In the field, the volatility surface is modelized by SVI which is homogenous, and the homogenous models are Hull & White model or Heston model. But they do not correspond to the surface of the volatility. On the other side from the paper of Fukusawa which will be described later, authors found out that the surface of volatility can be modelized by the fractional Brownian Motion. They will use in this model a volatility with fractional Brownian motion with a Hurst parameter less than 1⁄2 which can be consistent with the empirically observed specific property of volatility time series but also with the shape of the volatility surface. They focus on modeling the volatility time series.

Report’s objective is to understand the paper first but also to critic it as much as possible in a constructive way. To do so, we have studied the environment around the paper thanks to a short but explicit literature review. After that, we focused on the main theory, ideas and equation which are developed in the paper. Then, main results are discussed, interpreted, and implemented over another time-period. Finally, we brought a critic of the paper. Beside of this report we implement all the key results in Python.

# Project' Architecture

Presentation : 
  PDF : Report Volatility is rough.pdf
Resutls :
  Results have been backtested on Covid and Pre-covid period
  1) Covid period     : volatility_is_rough_covid.html
  2) Pre-Covid period : volatility_is_rough.html
    
