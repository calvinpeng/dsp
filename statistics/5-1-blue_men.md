[Think Stats Chapter 5 Exercise 1](http://greenteapress.com/thinkstats2/html/thinkstats2006.html#toc50) (blue men)

Answer: 34.27% of US Males

Code:
```python
import scipy
mu = 178
sigma = 7.7

low = 177.8 # 5'10" in cm
high = 185.42 # 6'1" in cm

low_z = (low - mu)/sigma
high_z = (high - mu)/sigma
low_pct = scipy.stats.norm.cdf(low_z)
high_pct = scipy.stats.norm.cdf(high_z)
print('%f%% of US Males' %((high_pct - low_pct)*100))
```
