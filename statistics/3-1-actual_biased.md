[Think Stats Chapter 3 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2004.html#toc31) (actual vs. biased)

Actual mean: 1.02420515504
Biased mean: 2.40367910066

Code:
```python
resp = nsfg.ReadFemResp()
pmf_numkdhh = thinkstats2.Pmf(resp.numkdhh, label='Actual')
pmf_numkdhh_biased = BiasPmf(pmf_numkdhh, label='Biased')
thinkplot.PrePlot(2)
thinkplot.Pmfs([pmf_numkdhh, pmf_numkdhh_biased])
thinkplot.Config(xlabel='Children in household', ylabel='PMF')
print('Actual mean:',pmf_numkdhh.Mean())
print('Biased mean:',pmf_numkdhh_biased.Mean())
```
