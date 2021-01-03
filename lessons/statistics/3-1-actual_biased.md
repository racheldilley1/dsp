[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

There is a large difference in the actual and biased observations of the number of kids in a household. The actual mean was found to be 1.02 and the biased was 2.4, 134% higher than the actual (code for finding both can be found below). This is a significant difference. 

    pmf_actual = thinkstats2.Pmf(resp.numkdhh, label='actual')
    print('mean', pmf_actual.Mean())
    
    pmf_biased = BiasPmf(pmf_actual, label='observed')
    print('mean', pmf_biased.Mean())
    
When observing the graph of these distributions you can see that that the actual is heavily skewed to the right, with most observations falling between 0 and 1, while the biased is more evenly distributed between 1 and 3 (code fopr plotting both distributions can be found below). 

    thinkplot.PrePlot(2)
    thinkplot.Pmfs([pmf_actual, pmf_biased])
    thinkplot.Config(xlabel='Number of Children', ylabel='PMF')
    
These distributions logically make since, as most adults between the ages of 18 and 30 we would not expect to have kids, but every kid surveyed would have at least one, due to the fact that they would be included in the count. 