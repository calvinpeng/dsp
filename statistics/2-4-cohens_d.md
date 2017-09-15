[Think Stats Chapter 2 Exercise 4](http://greenteapress.com/thinkstats2/html/thinkstats2003.html#toc24) (Cohen's d)

Answer: -0.08893641177719079

Code:
```python
import math

firsts = df[df.birthord == 1]
others = df[df.birthord != 1]
diff = firsts.totalwgt_lb.mean() - others.totalwgt_lb.mean()
firsts_var = firsts.totalwgt_lb.var()
others_var = others.totalwgt_lb.var()
firsts_n, others_n = len(firsts), len(others)
pooled_var = (firsts_n*firsts_var + others_n*others_var) / (firsts_n + others_n)
d = diff / math.sqrt(pooled_var)
print(d)
```
