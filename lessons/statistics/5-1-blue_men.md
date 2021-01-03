[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

The percentage of the male population between the heights of 5'10 and 6'1 is 34%. To get to this percentage, you must start by first converting feet and inches to centimeters. Centimeters is the units of our mean and standard deviation (mu and sigma respectively) shown below.
    
    upper = (6*12+1)*2.54
    lower = (5*12+10)*2.54
    mu = 178
    sigma = 7.7
    
The next step is the compute the CDFs of the upper and lower percentiles found using scipy.stats.norm.cdf. Subtravting the lower percentile from the upper percentile gives us the percentile range (shown below).
    
    upper_cdf = scipy.stats.norm.cdf(upper, loc=mu, scale=sigma)
    lower_cdf = scipy.stats.norm.cdf(lower, loc=mu, scale=sigma)
    percentage_range = (upper_cdf - lower_cdf)*100
