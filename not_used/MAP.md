
## Maximum a Posteriori
To tackle this problem, we can break the frequentist assumption that parameters are not observable events. Thus, we apply Bayesian statistics and assume that $\theta$ is drawn from a distribution $P(\theta)$, which means there are some values that we expect to be more reasonable for our event space.
This is how we introduce **prior** knowledge about the world within our model. 
The frequentist likelihood function $P(D ; \theta)$ or $P_{\theta}(D)$ becomes an actual conditional probability $P(D | \theta)$ which is the same as the likelihood in Bayes' formula. Bayesian statistics is a lot about priors. It's not about using Bayes' Theorem :-)

But we can still use Bayes' Theorem and find the best parameter $\theta$ given the data $D$:
$$
P(\theta \mid D) = \frac{P(D\mid \theta) P(\theta)}{P(D)}
$$


We have the following terminology:
- $P(\theta \mid D)$ posterior probabilities after observing the data
- $P(\theta)$ priors
- $P(D\mid \theta)$ likelihood, can be defined as the PMF or PDF
- $P(D)$ the marginals which sometimes are denoted by $Z$, are usually untractable, and treated as a normalizing factor since they do not impact $\operatorname*{argmax}_{\theta}$. The marginals may also be encountered as the sum of all partitions or an integral.

The maximum a posteriori is about finding the best parameters that explain our data by modelling the posterior probabilities:
$$
\begin{align}
\hat{\theta}_{\text{MAP}} &= \operatorname*{argmax}_{\theta} P(\theta \mid D) \\
&= \operatorname*{argmax}_{\theta} P(D\mid \theta) P(\theta) \\
&= \operatorname*{argmax}_{\theta} \log P(D\mid \theta) + \log P(\theta)
\end{align}
$$

For the Binomial distribution, we were looking at a distribution to give us the probability of $k$ successes, but now we need a distribution to give us the probability of a probability $\theta$.
But what distribution can we use to model the the probability of the prior $P(\theta)$?



## Conjugate Prioris

Remember the Binomial distribution which is defined by the rate of success of $N$ Bernouli trials, equiavalent to asking what is the probability of seeing $c$ successes (sum of all ones is $c$) after $N$ trials with binary probability $\theta$. If we preserve the previous notation of $c$ occurences of 1 and note $d = N-c$ occurences of 0, then:

$$
Bin(c | \theta, N) = \begin{pmatrix} N \\ c \end{pmatrix} \theta^c(1-\theta)^{d}
$$
where 
$$
{\displaystyle \begin{pmatrix} N \\ c \end{pmatrix} = \frac{N!}{c!(N-c)!} = \frac{(d+c)!}{c!d!} = \begin{pmatrix} d+c \\ c \end{pmatrix}}
$$
represents combinations of N taken c. 
The binomial distribution is a function that depends on $c$ and the distribution parameters are $\theta$ and $N$.


Since $0 \leq \theta \leq 1$, we need to find a continuous probability distribution. We could use the Gaussian distribution, no? Well, according to [Bayesian statistics](https://gregorygundersen.com/blog/2019/03/16/conjugacy/), it is more feasible to choose a distribution that has the same functional form as the likelihood function $P(D|\theta)$ and when we do this we call our chosen distribution the **conjugate** to the likelihood.


The prior with the same functional form as the Binomial is called the Beta distribution given by:

$$
Beta(\theta | \alpha, \beta) = B(\alpha,\beta) * \theta^{(\alpha-1)} * (1-\theta)^{(\beta-1)}
$$
where $\alpha$ and $\beta$ are distribution (hyper)parameters $\in \mathbf{R}$ and $B(\alpha,\beta)$ is a coefficient that depends on $\alpha$ and $\beta$ used to normalize everything between 0 and 1. The constant $B(\alpha,\beta)$ is similar in concept to the Binomial version and is given by the inverse of the [Beta function](https://en.wikipedia.org/wiki/Beta_function):
$$
B(\alpha,\beta) = \frac{\Gamma(\alpha+\beta)}{\Gamma(\alpha)\Gamma(\beta)}
$$

The [$\Gamma$ function](https://en.wikipedia.org/wiki/Gamma_function#Motivation) is the extension of the factorial function: ${\displaystyle \Gamma (z)=\int _{0}^{\infty }t^{z-1}e^{-t}{\text{ d}}t,\ \qquad \Re (z)>0\,}$ for any complex number $z \in \mathbb{C}$ whose real part is strictly positive. A factorial is a function that obeys the recursive property $f(x+1) = xf(x)$.


Unlike the Binomial (where we modelled the probability of successes $c$) the Beta distribution gives the porbability of the probability value $\theta$ and the distribution parameters are real values $\alpha$ and $\beta$.


If we set $\alpha$ and $\beta$ as complementary integers $\alpha+\beta = N$, we can see that the coeficient is identical to the combinations: ${\binom {\alpha+\beta}{\alpha}}$ in the Binomial distribution. You may play with the [scipy implementation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.special.gamma.html) to get a hands on some examples.

### Maximum a Posteriori Estimation
Now that we have a conjugate to model the parameter $\theta$, we can get back to our maximum aposteriori rule to find the best $\theta$ given the data: $P(\theta \mid D) = \frac{P(D\mid \theta) P(\theta)}{P(D)}$, we can see that this is equivalent to saying:

$$
\begin{align}
P(\theta \mid D) &=
C(\alpha,\beta,c,d) * \theta^c(1-\theta)^{d} * \theta^{(\alpha-1)} * (1-\theta)^{(\beta-1)} \\
&= C(\alpha,b,c,d) * \theta^{(c + \alpha-1)} * (1-\theta)^{(d+ \beta-1)} \\
&\propto  \theta^{(c + \alpha - 1)} * (1-\theta)^{(d + \beta - 1)} \\
\end{align}
$$
where $C(\alpha,\beta,c,d) = B(c+\alpha, d+\beta)$ is the normalizing constant.

It is clear now that using the conjugate form is advantageous for the posterior has the same functional dependency on $\theta$ as the prior and the likelihood, which makes calculating the derivative of the above formula with respect to $\theta$ easy -- it will have the same shape as the one for Maximum Likelihood:

$$
\hat{\theta} = \frac{c+\alpha - 1}{c+\alpha + d+\beta -2} = \frac{c+\alpha - 1}{N + \alpha + \beta -2}
$$

This is identical to the Maximum Likelihood Estimator we derived earlier, where we are adding $\alpha-1$ and $\beta-1$ "hallucinations".
As long as our priors are well defined and tractable, MAP is a very good estimator.
Looking at differrent plots of the Beta distribution
<img width="600" src="https://gregorygundersen.com/image/conjugacy/beta.png">
for different values of $(\alpha, \beta) \in \{(0.1,0.1), (1,1), (2,2), (2,3)\}$, we must make a modelling assumption based on prior knowledge. Coin flipping is expected to be a symmetric distribution with the mode at 1/2. 


Observing a data set of $m$ observations of $1$ and $m$ observations of $0$ increases the value of $\alpha$ by $m$, and the value of $\beta$ by $m$, in going from the prior distribution to the posterior distribution. This allows us to provide a simple interpretation of the hyperparameters $\alpha$ and $\beta$ in the prior as
an effective number of observations of $1$ and $0$, respectively. Note that $\alpha$ and $\beta$ need not be integers.

Furthermore, the posterior distribution can act as the prior if we subsequently observe additional data. To see this, we can imagine taking observations one at a time and after each observation updating the current posterior distribution by multiplying by the likelihood function for the new observation and then normalizing to obtain the new, revised posterior distribution. At each stage, the posterior is a Beta distribution with some total number of (prior and actual) observed
values for $1$ and $0$ given by the parameters $\alpha$ and $\beta$. Incorporation of an additional observation of $1$ simply corresponds to incrementing the value of $\alpha$ by 1, whereas for an observation of $0$ we increment $\beta$ by 1. Example by [Gregory Gundersen](https://gregorygundersen.com/blog/2019/03/16/conjugacy).



## Exercise
Derive the MLE estimator for the parameters of a Gaussian distribution.

## References
- [Statistical Rethinking](https://annas-archive.org/md5/0248fb4ed1c61ea56aa4a5872e196a85), consider starting with Chapter 2
- [Maximum Likelihood course notes](https://web.stanford.edu/class/archive/cs/cs109/cs109.1192/lectureNotes/21%20-%20MLE.pdf)
- [Comparison of MLE and MAP](https://www.cs.cornell.edu/courses/cs4780/2021fa/lectures/lecturenote04.html)
- [The Gamma Function](https://web.archive.org/web/20161112081854/http://www.plouffe.fr/simon/math/Artin%20E.%20The%20Gamma%20Function%20(1931)(23s).pdf), 1964, Emil Artin
- [The Epic Story of Maximum Likelihood](https://arxiv.org/pdf/0804.2996.pdf), Stephen M. Stiegler
- [Conjugacy in Bayesian Inference](https://gregorygundersen.com/blog/2019/03/16/conjugacy/), Gregory Gundersen