# Monte Carlo path generation using Generative Adversarial Network (GAN)

Monte Carlo methods have long been used in the field of finance to analyze complex instruments by simulating sources of uncertainty. These simulations use randomized values to build a path.
Efforts have been made in the last few years to accurately capture the true distribution in the movement of underlyings, because it is not a uniform distribution.

In this project, I plan to use market data to train a GAN, which can reproduce probability distributions that match all training data.

I am currently taking in data on interest rates, volatility and market indices. Most of this data is coming from Quandl, but some data (eg. the complete interest rate term structure) needs to come from some premium sources. I will get this data from Bloomberg. Since in this field, data is key, I realize that not all data can be scraped from the web.

The reason for choosing a GAN over other neural networks is the proven capability of a GAN to recognize patterns and to get results that get better. 
The generative neural network will start off with noise, but will generate a probability distribution.
The discriminative neural network, which will be trained on real market data, will determine if the generated distribution is "real" or not. This error will then be back-propogated.