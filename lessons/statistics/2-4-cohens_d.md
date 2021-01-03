[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Based on a histogram and the summary statisticv of the mean, we can conclude that first babies tend to be lighter than others. From the histogram we see that first babies weight are highest from 5 to 6 pounds where others are highest from 7 to 8.5 pounds. Code for finding the histogram can be found below.

    first_hist = thinkstats2.Hist(firsts.totalwgt_lb, label='first')
    other_hist = thinkstats2.Hist(others.totalwgt_lb, label='other')
    width = 0.45
    thinkplot.PrePlot(2)
    thinkplot.Hist(first_hist, align='right', width=width)
    thinkplot.Hist(other_hist, align='left', width=width)
    thinkplot.Config(xlabel='pounds', ylabel='Count', xlim=[4, 10])
    
The mean weight for first and other babies was 7.20 and 7.32 pounds respectively, a 0.12 pound difference. Code used to find the means is found below.

    firsts.totalwgt_lb.mean(), others.totalwgt_lb.mean()
    
The Cohen effect size for the difference in baby weights for first babies and others was found to be 0.09 standard deviation. The Cohen effect size for the difference in pregnancy length for first babies and others was 0.029 standard deviations. The difference in baby weights while still small, is higher than the difference in pregnancy lengths.
