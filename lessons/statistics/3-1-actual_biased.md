[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

### Create biasing function

def BiasPmf(pmf, label):
    new_pmf = pmf.Copy(label=label)

    for x, p in pmf.Items():
        new_pmf.Mult(x, x)
        
    new_pmf.Normalize()
    return new_pmf
    
### Create and plot our PMFs

resp = nsfg.ReadFemResp()

unbiased_pmf = thinkstats2.Pmf(resp['numkdhh'], label='unbiased')

biased_pmf = BiasPmf(unbiased_pmf, label='biased')

thinkplot.PrePlot(2)
thinkplot.Pmfs([unbiased_pmf, biased_pmf])
thinkplot.Config(xlabel='children_in_household', ylabel='PMF')

![PMF Plotted](file:///Users/nicksherwin/Desktop/pmf.png)

print(unbiased_pmf.Mean(), biased_pmf.Mean())

Output: 1.024205155043831 2.403679100664282

As expected, the mean for the biased results is much higher.

 
