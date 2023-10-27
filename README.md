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

Nearly all words have low rates per thousand words; thus the occurrence of any one word at one spot in a text is a rare event. In many statistical problems distributions of rare events are governed by the [Poisson law](https://en.wikipedia.org/wiki/Poisson_distribution), which gives the probability of a count of $k$ as a function of the mean count, $\lambda$, as follows:

$$ f(k;\lambda )=\Pr(X{=}k)={\frac {\lambda ^{k}e^{-\lambda }}{k!}}  $$

[...]

To find out how well the Poisson fits the distribution of Hamilton and Madison word counts, we broke up a collection of Federalist papers into 247 blocks of approximately 200 words, and tabulated the frequency distribution of counts for each of many different words. [...] we give distributions
for Hamilton in Table 2.4. The distributions for *an, any*, and *upon* are fitted rather well by the Poisson, but even a motherly eye[^1] sees disparities for *may* and *his*.





<!--
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
-->


#### References
- see the links in the excerpts above
- [Understanding of Multinomial Naive Bayes for Text Classification](https://web.stanford.edu/~jurafsky/slp3/4.pdf)

[^1]: *even a motherly eye*? worth noting a random sexist remark in an academic paper of the '60s

