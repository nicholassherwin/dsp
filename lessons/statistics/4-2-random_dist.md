[Think Stats Chapter 4 Exercise 2](http://greenteapress.com/thinkstats2/html/thinkstats2005.html#toc41) (a random distribution)

### Plotting the CMF 

rand_pmf = thinkstats2.Pmf(rand)

thinkplot.Pmf(rand_pmf)
thinkplot.Config(xlabel='Random_Numbers', ylabel='Pmf')

![PMF](file:///Users/nicksherwin/Desktop/randpmf.png)

### Plotting the CDF

rand_cdf = thinkstats2.Cdf(rand)

thinkplot.Cdf(rand_cdf)
thinkplot.Config(xlabel='Random_Numbers', ylabel='Cdf')

![CDF](file:///Users/nicksherwin/Desktop/randcfd.png)

While we cannot tell the distribution in the PMF because each value has the same probability of occurring and all have the same value of .001, we can see that the probabilities are normally distributed in the CDF.
