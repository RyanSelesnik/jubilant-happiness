**In** 1948 Claude Shannon formalised his mathematical theory of communication where he layed the foundations of the digital world as we know it today.  Eight years later J. L. Kelly, jr expanded on Shannons theory by showing how it can be applied to any arbitrary system that has the essential features of a communication system. For Kelly, it was gambling.  Ed Thorpe did so and so. 

I have had an on and off interest in trading in the stock market for a few years now. Recently the "Kelly Criterion" sparked my interest since it combined the ideas of Information theory and betting. When one thinks of trading, a naive metric is the the annualised return or the return trade. As you learn more you release not only the return matters but the probabilities associed with each return. Of course is this a contonous value.

I must say that most resources pose the question in a way that seems to be intentionally misleading. When posing the question of should you take the beat _repeatedly_? 

If the question is posed more honestly I think it becomes rather obvious what you definitely should and should not do. 

However, I’m not necessarily apposed to this approach because it did get my attention (I’m drawn to counterintuitive things). I presume the intention is to illustrate that betting or risk taking is not a single event but rather multiple. Smoking is not risky done once. But done multiple times over your life is very risky. The reason is because over time dynamics are introduced (there is some dependence between past and future states) 


- Illustrate two extremes I.e. when median coincides with mean and when they diverge. Why does this happen?
- Okay cool so now that we’ve got the worst case and the most risk averse scenario, how do we find the optimal point in between?
- Could you and I have come up with this ourselves?

we have the growth rate 
$$
\frac{1}{N}\log {\frac{V_{N}}{V_{0}}}
$$



Consider $C_{t}$ your capital at time $t$ $C_{0}$ your initial capital and $r$, the geometric growth rate. Then the capital at each time step is
$$
C_{t} = C_{0}(1+r)^t
$$
Starting with 1 unit of wealth, we bet a fraction $f$ on an outcome that occurs with probability $p$ and offers odds $b$ (for example $b$ could be $80 \ \%$)

The expected geometric growth rate $r$ is
$$
\begin{equation}
r = (1+fb)^p(1-fa)^q
\end{equation}
$$
This assumes we know $p$ which
$$
\log(r) = p\log(1+fb)+q\log(1-fa)
$$

Taking derivate with respect to f of both sides
$$
\begin{align*}
\frac{d}{df}\log{r} &= \frac{d}{df} \left[ p\log(1+fb)+q\log(1-fb)\right] \\
\frac{1}{r} &= \frac{bp}{1+fb}-\frac{qa}{1-fa}
\end{align*}
$$
we can already see from the first equatiojn that the roots are f = $-\frac{1}{b}$ and $f=\frac{1}{a}$


Lets assume you have some space $\Omega$ that contains elements $\omega$ and we have a random varible such that $X(\omega)=\{-1,1\}$

$$
X_{0}+X_{0}
$$

```python
import numpy as np
import matplotlib.pyplot as plt
W = np.linspace(0, 1, 20)
f = np.linspace(0, 1, 100)
F, W = np.meshgrid(f, W)
L = 1 - W
R = (1+F)**W * (1-F)**L
plt.plot(f, R.T)
plt.grid()
plt.legend(['W = {}'.format(np.round(w,2)) for w in W[:, 0]], bbox_to_anchor=(1.05, 1), loc='upper left')
plt.show()
```

![[Pasted image 20240424202219.png]]