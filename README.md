# Archaeology of Intelligent Machines


## Introductory course

- [Three Thousand Years of Algorithmic Rituals: The Emergence of AI from the Computation of Space](https://www.e-flux.com/journal/101/273221/three-thousand-years-of-algorithmic-rituals-the-emergence-of-ai-from-the-computation-of-space/), Matteo Pasquinelli 

<img src="https://upload.wikimedia.org/wikipedia/commons/e/e5/Gospers_glider_gun.gif"  width="400">

- Excerpt:

The term “algorithm” comes from the Latinization of the name of the Persian scholar al-Khwarizmi. His tract On the Calculation with Hindu Numerals, written in Baghdad in the ninth century, is responsible for introducing Hindu numerals to the West, along with the corresponding new techniques for calculating them, namely algorithms. In fact, the medieval Latin word “algorismus” referred to the procedures and shortcuts for carrying out the four fundamental mathematical operations—addition, subtraction, multiplication, and division—with Hindu numerals. Later, the term “algorithm” would metaphorically denote any step-by-step logical procedure and become the core of computing logic. In general, we can distinguish three stages in the history of the algorithm: in ancient times, the algorithm can be recognized in procedures and codified rituals to achieve a specific goal and transmit rules; in the Middle Ages, the algorithm was the name of a procedure to help mathematical operations; in modern times, the algorithm qua logical procedure becomes fully mechanized and automated by machines and then digital computers.


Looking at ancient practices such as the Agnicayana ritual and the Hindu rules for calculation, we can sketch a basic definition of “algorithm” that is compatible with modern computer science:

1. an algorithm is an abstract diagram that emerges from the repetition of a process, an organization of time, space, labor, and operations: it is not a rule that is invented from above but emerges from below;
2. an algorithm is the division of this process into finite steps in order to perform and control it efficiently; 
3. an algorithm is a solution to a problem, an invention that bootstraps beyond the constrains of the situation: any algorithm is a trick; 
4. most importantly, an algorithm is an economic process, as it must employ the least amount of resources in terms of space, time, and energy, adapting to the limits of the situation.

Today, amidst the expanding capacities of AI, there is a tendency to perceive algorithms as an application or imposition of abstract mathematical ideas upon concrete data. On the contrary, the genealogy of the algorithm shows that its form has emerged from material practices, from a mundane division of space, time, labor, and social relations. 


#### References
- [Language, Cohesion and Form (Studies in Natural Language Processing)](http://libgen.rs/book/index.php?md5=4EBE0188B1C9E63E3293BB70918F8C5A), Margaret Masterman, Yorick Wilks    
- [The Perceptron](https://blogs.umass.edu/brain-wars/files/2016/03/rosenblatt-1957.pdf), 
Frank Rosenblatt
- [Calculating Space](https://sferics.idsia.ch/pub/juergen/zuserechnenderraum.pdf), Konrad Zuse 
- [Algorithmic Theories of Everything](https://arxiv.org/abs/quant-ph/0011122), Jürgen Schmidhuber
- [Theory of Self-Reproducing Automata](https://cba.mit.edu/events/03.11.ASE/docs/VonNeumann.pdf), John von Neumann


## Exploratory Data Analysis, Federalist Papers, and Bayesian Inference

- [Inference in an Authorship Problem](https://ptrckprry.com/course/ssd/reading/Most63.pdf), Frederick Mosteller and David L. Wallace

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/Poisson_pmf.svg/1280px-Poisson_pmf.svg.png"  width="400">

Excerpts:

As statisticians, our interest in this controversy is largely methodological.
Problems of discrimination are widespread, and we wished a case study that would give us an opportunity to compare the more usual methods of discrimination with an approach via Bayes’ theorem.

[...]

The classical approach to discrimination problems, flowing from Fisher’s "linear discriminant function" and from the Neyman-Pearson fundamental lemma, is well exposited by [Rao 10, Chapter 8](https://archive.org/details/advancedstatisti00raoc). Important recent writings on Bayesian statistics include the books by [Jeffries 6](https://archive.org/details/in.ernet.dli.2015.2608/page/n129/mode/2up), by [Raiffa and Schlaifer 9](https://gwern.net/doc/statistics/decision/1961-raiffa-appliedstatisticaldecisiontheory.pdf), and by [Savage 11](https://gwern.net/doc/statistics/decision/1972-savage-foundationsofstatistics.pdf)


[...]

Let us look in Table 2.1 at frequency distributions for rates of the high-frequency words *by, from*, and *to* in 48 Hamilton and 50 Madison papers (some exterior to The Federalist®). 
[Table 2.1. contains frequency distribution of rates per thousand words for the 48 Hamilton and 50 Madison papers.] High rates for *by* usually favor Madison, low favor Hamilton; for *to* the reverse holds. 
Low rates for *from* tell little, but high rates favor Madison. In Table 2.2, we see that rates for the word *war* vary considerably for both authors. The meaning of *war* automatically suggests that the rate of use of this word depends on the **topic** under discussion. In discussions of the armed forces the rate is expected to be high; in a discussion of voting, low. We call words with such variable rates **"contextual"** and we regard them as *dangerous for discrimination*.

[...]

Nearly all words have low rates per thousand words; thus the occurrence of any one word at one spot in a text is a rare event. In many statistical problems distributions of rare events are governed by the [Poisson law](https://en.wikipedia.org/wiki/Poisson_distribution), which **gives the probability of a count of $x$** as a function of the mean count, $\lambda$, as follows:

$$ f(x;\lambda )=\Pr(X{=}x)={\frac {\lambda ^{x}e^{-\lambda }}{x!}}  $$

Modern books designate the counts by $k$ instead of $x$, but we will follow the original paper's notation.

[...]

To find out how well the Poisson fits the distribution of Hamilton and Madison word counts, we broke up a collection of Federalist papers into 247 blocks of approximately 200 words, and tabulated the frequency distribution of counts for each of many different words we give distributions
for Hamilton in Table 2.4.

[**observed** values contain the number of blocks where the word has been observed 0 times, 1 time, etc. **Poisson** values are computed using the function above ${\frac {\lambda ^{x}e^{-\lambda }}{x!}} * 247$, where $\lambda$ is estimated as the average number of occurences / block. For example, given the table, *any* appears in average $0.67$ times per block. The [Poisson PDF](https://www.wolframalpha.com/input?i=poisson+distribution%28mean%3D0.67%2C+x%3D1%29) predicts $f(1; 0.67) = 0.342845$. Therefore the total number of blocks is $0.342845*247 = 84.68$; the results may vary significantly by a few points, depending on the precision used.
]

The distributions for *an, any*, and *upon* are fitted rather well by the Poisson, but even a motherly eye[^1] sees disparities for *may* and *his*.

|    $x$ counts:| 0     | 1    | 2    | 3    | 4   | 5   | 6 | 7 or more  | 
|---------------|-------|------|------|------|-----|-----|---|------------|
|*an* observed  | 77    | 89   | 46   | 21   | 9   | 4   | 1 |            |
|*an* Poisson   | 71.6  | 88.6 | 54.9 | 22.7 | 7.0 | 1.7 | 4 | 1          |
|*any* observed | 125   | 88   | 26   | 7    |  0  |  1  |   |            |
|*any* Poisson  | 126.3 | 84.6 | 28.5 | 6.4  | 1.1 | 2   |   |            |

[...]

Let $p_1 = P(H)$ and $p_2 = 1-p_1 = P(M)$, be the probabilities before the observations that Hypotheses 1 and 2 respectively are true. For example, Hypothesis 1 ($H$) might be that Hamilton wrote the paper, Hypothesis 2 ($M$) that Madison wrote it. [These are the priors we discussed in class.]

Let $f_i(x)$ be the conditional probabilities of observing the result $x$, given that Hypothesis $i$ is true, e.g.,  $f_1(x) = P(x | H)$.

The conditional probability that Hypothesis 1 is true given observation $x$ is:

$$
P(H | x) = \frac{p_1 f_1(x)}{p_1 f_1(x) + p_2 f_2(x)} = \frac{P(H)*P(x | H)}{P(x)}
$$

Both computational and intuitive advantages accrue if we use odds instead of probabilities. [...] 

$$
Odds(H, M | x) = \frac{P(H | x)}{P(M | x)} = \frac{P(H)*P(x | H)}{P(M)*P(x | M)}
$$


The logarithmic form of Bayes’ theorem can be obtained by taking the logarithm:

$$
\log{Odds(H, M | x)} =  \log{\frac{P(H)}{P(M)}} + \log{\frac{P(x | H)}{P(x | M)}}
$$

The initial odds or priors $\log{\frac{P(H)}{P(M)}}$ are treated in Naive Bayes as the normalized counts for each author / class. The authors make extensive analyses of the impact of these priors, see Section 4C in the paper and Section 3.1C in the book. And they conclude by setting the initial odds as equally probable, turning them into a constant factor: *thus 1/2 is the initial odds determined by our beliefs prior to the execution
of the experiment*.


Suppose Hamilton’s and Madison’s use of the word *also* are well represented by Poisson distributions with parameters $w\mu_H$ and $w\mu_M$, where $w$ is paper length
in thousands of words and the $\mu$ are the rates per thousand. [The authors renamed $\lambda$ from Poisson PDF into $\mu$ to resemble an estimation of the mean $\mu_{\{H,M\}}$ from the data as the average number of occurences / 1000 words for each author.
If you check the 1964 textbook, you'll see some different numbers in Table 3.1-1 vs Table 4.1 from the paper, probably due to the errors of computing these in 1963 when the paper was published.]

So, assuming Poisson distribution, for a single word with frequency $x$, we model $P(x | H) = f(x; \mu_H )={\frac {\lambda ^{x}e^{-\lambda }}{x!}}$.

then the log-likelyhood ratio between hypotheses $H$ and $M$ is

$$ 
\log{\frac{P(x | H)}{P(x | M)}}=\log{\frac{f(x;\mu_H)}{f(x;\mu_M)}}=\log{(\mu_H/\mu_M)^x e^{-w(\mu_H-\mu_M)}} \\
=x\log{\mu_H/\mu_M} - w(\mu_H-\mu_M) 
$$

Based on the *Naive* assumption that words appear independently in a text, and the authors decision to set the priors as equally probable ($P(H) = P(M) = 1/2$) the priora cancel out in the log-odds ratio and it is resuced to the log-likelyhood ratio for all feature words of interest $\{x_1, ..., x_n\}$ becomes:

$$
\text{decision} =  \log{\frac{P(x_1, ..., x_n | H)P(H)}{P(x_1, ..., x_n | M)P(M)}} \\
=\log \prod_{i=1}^{n} \frac{P(x_i| H)}{P(x_i | M)} \\
= \sum_{i}^{n} \log \frac{ P(x_i| H)}{ P(x_i | M)} \\
= \sum_{i}^{n} x_i \log{\frac{\mu_{H_i}}{\mu_{M_i}}} - w(\mu_{H_i}-\mu_{M_i})
$$

where $\mu_{H_i}$ and $\mu_{M_i}$ are estimated means of occurences / 1000 words for eaach individual word $i$.

**decision** is a predictor that states the odds with which Hamilton is the author over Madison. This can be proven to be an optimal predictor that minimizes the empirical risk, and for a modern approach to this part, you may want to check [Chapter 1 of mlstory.org](https://www.mlstory.org/prediction.html).

<!--
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
-->


#### References
- [Understanding of Multinomial Naive Bayes for Text Classification](https://web.stanford.edu/~jurafsky/slp3/4.pdf)
[Chapter 8 for Discrimination Problems](https://archive.org/details/advancedstatisti00raoc) 
- [Jeffries, Bayesian statistics](https://archive.org/details/in.ernet.dli.2015.2608/page/n129/mode/2up)
- [Bayesian statistics, Raiffa and Schlaifer](https://gwern.net/doc/statistics/decision/1961-raiffa-appliedstatisticaldecisiontheory.pdf)
- [Bayesian statistics, Savage](https://gwern.net/doc/statistics/decision/1972-savage-foundationsofstatistics.pdf)


[^1]: *even a motherly eye*? worth noting a random sexist remark in an academic paper of the '60s

