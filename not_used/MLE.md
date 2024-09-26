
# Side-story: Estimating Parameters from Data

You will often hear or read that probabilities for words are estimated using a maximum likelihood estimator by counting the number of occurences to the total. But what is "maximum likelihood"?


Remember the following two basic rules of [probabilities](https://www.wikiwand.com/en/Conditional_probability#Media/File:Bayes_theorem_visualisation.svg):
1. conditional probability of two events $A$ and $B$ **not** independent:
$$
\text{1. }  P(A,B) = P(A)*P(A|B) \\
= P(B,A) = P(B)*P(B|A)
$$
2. marginal probability as the sum of all partitions
$$
\text{2. }  P(B) = \sum_{A_i}P(B, A_i) = \sum_{A_i}P(B|A_i)P(A_i)
$$

From rule 1. we get Bayes' theorem:
$$
P(A|B) = \frac{P(A)P(B|A)}{P(B)} \\
posterior = \frac{prior * likelihood}{marginal}
$$
which is equivalent to saying "we update our beliefes after the evidence is considered".

Hopefully it is more clear now, that if we talk about maximum likelihood estimation, it might have something to do **likelihood** term $P(B|A)$ in the above equation.

## Back to the Coin
Let's start with the simplest example: we have a binary coin that returns 0, 1. We don't know at this point if the coin has been rigged and we want to use data (observed trials) to define a set of beliefes. Which one is more likely 0 or 1? Are they really equally probable?

Common sense would say each coin has the same probability, e.g., the probability of seeing $1$ is $\theta=1/2$ and that the coin is not rigged, but we can't be sure untill we see it. Sidenote, if someone is very skilled at throwing coins, it could also trick us to see what we we expect to see; is there any way to measure that?


By seeing something, here we mean that we have some **observations** or some data $D = \{1,1,1,1,0\}$. We can characterize this dataset by its size $|D| = N$. We assume the data is generated randomly using a probability distribution. Given our knowledge of the world, we can make an **explicit assumption** by saying this data is made of independent events, each event being from generated with a [Bernouli distribution](https://en.wikipedia.org/wiki/Bernoulli_distribution) (iid). The probability mass function of the Bernoulli is:

\begin{align}
f(k; \theta) = P(k;\theta) = p_{\theta}(k)&={\begin{cases}\theta&{\text{if }}k=1,\\1-\theta&{\text{if }}k=0.\end{cases}} \\
&= \theta^k(1-\theta)^{(1-k)}
\end{align}

We could also model the data as a [Binomial distribution](https://en.wikipedia.org/wiki/Binomial_distribution), which describes the success of $N$ binary (Bernouli) independent events, each with probability $\theta$. If we know we have $N$ events and want to compute the probability of observing $c$ successes, then the probability mass function of the Binomial is:

\begin{equation}
{\displaystyle f(c,N,\theta)=P(c;N,\theta)=p_{\theta, N}(c)={\binom {N}{c}}\theta^{c}(1-\theta)^{N-c}}
\end{equation}

We use different notations in PMF to make it clear that different textbooks refer to the same thing.



We know the Bernouli distribution is parameterized by $\theta$ (from its definition), therefore our question is:
- what are the most likely parameters $\theta$ of the Bernouli probability distribution $P_{\theta}(\cdots)$ that explain the data $D = \{x_1, x_2, ..., x_N\}$? let's note this as $\hat{\theta}$
- one might encounter the parameters writted with a column $P(\cdots ; \theta)$ or defined as a separate function ${\mathcal {L}}(\theta \mid \cdots) = {\mathcal {L}}(\theta) = {\mathcal {L}}_{N}(\theta )={\mathcal {L}}_{N}(\theta ; \cdots )=f_{N}(\cdots ;\theta )\;$
- we use $\cdots$ do signify any notation for data, here we will used $D$, but $\mathbf{y}$ is also often encountered; sometimes the data is ommited completely ${\mathcal {L}}(\theta)$

Bayesian statistics allows treating these parameters as coming from a distribution while frequentist statistics does not allow distributions of unobserved variables (such as parameters). Causal models (see Bayesian statistics [course here](https://github.com/rmcelreath/stat_rethinking_2024)) start by modelling a generating process of the data. For a brief comparison between Bayesian and frequentist statistics, [see this blog post](https://medium.com/@roshmitadey/frequentist-v-s-bayesian-statistics-24b959c96880). Maximum likelihood estimation is inherently a frequentist approach. Keep in mind that this is not the only approach to estimate the parameters from the data.



## Maximum Likelihood Estimation
The formal textbook definition of the likelihood function in frequentist statistics is written in multiple ways, depending on the textbook:
$$
{\mathcal {L}}(\theta \mid x) = P(X=x; \theta) =p_{\theta }(x) =P_{\theta }(X=x)
$$ 
representing the probability of observing the outcome $x$ of random variable $X$ given the probability parameter $\theta$, given a discreet probability mass function $p_{\theta}$. Yet another name for the sanme thing! The likelihood is the same as the probability mass/density function, but with a fixed parameter $\theta$ and with the interpretation that it is related to a speciffic set of observations $D$. In the case of discrete distributions, likelihood is a synonym for the joint probability of your data. In the case of continuous distribution, likelihood refers to the joint probability density of your data.

By the Maximum Likelihood Estimation, we mean the parameter $\theta$ that maximizes our entire dataset $D$:

$$
\hat{\theta}_{\text{MLE}} = \operatorname*{argmax}_{\theta} P_{\theta}(D)
$$
For independent and identically distributed random variables [iid](https://stats.stackexchange.com/a/17392), such as our dataset $D$, $P_{\theta}(D)$ will be the product of univariate density functions: 
$$
\hat{\theta}_{\text{MLE}} = \operatorname*{argmax}_{\theta} \prod_{i=1}^{N}  p_{\theta}(x_i)
$$



For our coin, these are individual Bernoullis and we have a **parameter** $0 \leq \theta \leq 1$ that gives us the chance for the coin to give value 1:

$$
p_{\theta}(1) = \theta ,\\
p_{\theta}(0) = 1-\theta
$$
therefore

$$
\begin{align}
\hat{\theta} &= \operatorname*{argmax}_{\theta} {\mathcal {L}}(D | \theta) \\
\hat{\theta} &= \operatorname*{argmax}_{\theta} \prod_{i=1}^{N}  p_{\theta}(x_i) \\
&= \operatorname*{argmax}_{\theta} \prod_{i=1}^{N} \theta^{x_i}(1-\theta)^{(1-x_i)} \\
\end{align}
$$

To maximize the function we can:

1. use log values (log-likelihood $l(\theta) = log{\mathcal{L}}(\theta)$ to aid our computation (we can do this because the log is monotonic and the likelihood is positive)
1. take the derivative and equate with zero to find points of extreme
1. check the second derivative is negative to make sure it's not a point of minimum

$$
\begin{align}
\mathcal{l}({\theta}) &=  \log \theta \sum_{i=1}^{N}x_i + \log (1-\theta) \sum_{i=1}^{N}(1-x_i)
\end{align}
$$

the sums above can be denoted as two constants defined by counts: $c = \sum_{i=1}^{N}x_i$ and therefore $N - c = \sum_{i=1}^{N}(1-x_i) $,

then if we equate with zero:
$$
\frac{\partial\mathcal{l}(\theta)}{\partial \theta} = \frac{\partial c\log\theta + (N - c)\log(1-\theta)}{\partial \theta} = 0
$$
and we get
$$
c\frac{1}{\theta} - (N-c)\frac{1}{1-\theta} = 0 \\
c(1-\theta) = (N-c)\theta \\
$$
therefore
$$
\hat{\theta} = \frac{c}{N} = \frac{\sum_{i=1}^{N}x_i}{N}
$$

which is equivalent to saying that the maximum likelihood estimator is the relative frequency of an event: the number of counts of an event divided by the total number.

Long story short, MLE estimation is a means to derive the parameters that best describe a set of observations by doing a derivative over parameters using the probability mass/density function across a dataset.

### What if we are wrong?
In the above example with $D = \{1,1,1,1,0\}$, the maximum likelihood estimator would yield $\hat{\theta} =4/5$ which is not a very good estimator for what we would expect to be a real-life coin flip scenario. If by some chance, the data is small or is dominated by a single value, then the maximum likelihood estimator does not give very good predictions. What if we have no observations of value $0$ in our sample?

A first solution would be to introduce some smoothing constants (or hallucinations) in the estimator, suppose we add $m$ heads and $m$ tails in our estimator:
$$
\hat{\theta} = \frac{c + m}{N + 2m} =  \frac{m + \sum_{i=1}^{N}x_i}{N + 2m}
$$

This can be arbitrary? How many new samples should we add after all?



