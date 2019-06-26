[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

mean = 178
sigma = 7.7
dist = scipy.stats.norm(loc=mean, scale=sigma)

dist.cdf(185.42) - dist.cdf(177.8)

Output: 0.3427468376314737

The above tells us that approximately 34% of the US male population is in the height range to be a blue man.
