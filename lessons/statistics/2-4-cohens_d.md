[Think Stats Chapter 2 Exercise 4] 
(function provided by thinkstats to compute the difference in means expressed in number of standard deviations:)
def CohenEffectSize(group1, group2):
"""Computes Cohen's effect size for two groups.
    
    group1: Series or DataFrame
    group2: Series or DataFrame
    
    returns: float if the arguments are Series;
             Series if the arguments are DataFrames
    """
    diff = group1.mean() - group2.mean()

    var1 = group1.var()
    var2 = group2.var()
    n1, n2 = len(group1), len(group2)

    pooled_var = (n1 * var1 + n2 * var2) / (n1 + n2)
    d = diff / np.sqrt(pooled_var)
    return d 
   
   ### Comparing Birth Weights
   
   CohenEffectSize(firsts.totalwgt_lb, others.totalwgt_lb)
   
   Output: -0.088672927072602
   
   In the above we see that the difference between the mean weight of two groups is small in comparison to their combined        standard deviation. Thus, the weight difference between first babies and subsequent is not especially significant.
   
   ### Comparing Pregnancy Lengths
   
   CohenEffectSize(firsts.prglngth, others.prglngth)
   
   Output: 0.028879044654449883
   
Here we see an even smaller difference, thus the pregancny length difference between first and other babies can also be     said to not statstically significant.


    
