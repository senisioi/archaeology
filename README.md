# Archaeology of Intelligent Machines


<div style="width: 100%;">
  <img width="600" src="https://github.com/senisioi/archaeology/blob/main/img/welcome.svg?raw=true">
</div>


## Table of Contents

- [Project Ideas](#ideas)
- [Introductory Course](#intro)
    - [References](#intro_refs)
- [Exploratory Data Analysis, Federalist Papers, and Bayesian Inference](#eda)
    - [References](#eda_refs)
- [Is Language Related to Thought? Are Machines Able to Think?](#thought)
    - [Wittgenstein and Language](#thought_witt)
    - [Chomsky on Language and Cognition](#thought_chomsky)
    - [The Game / Игра - Анатолій Дніпров (1961)](#thought_game)
    - [Thinkin Machine Dehumanizing Women](#thought_sexism)
    - [The Language System in the Human Brain](#thought_LLMs)
    - [References](#thought_refs)
- [Side-story: Estimating Parameters from Data](#map_mle)
    - [Maximum Likelihood Estimation](#mle)
    - [Conjugate Priors](#conj)
    - [Maximum a Posteriori Estimation](#map)
    - [References](#map_mle_refs)

- [Entropy](#entropy)
    - [References](#entropy_refs)
- [Cybernetics](#cybernetics)
    - [References](#cybernetics_refs)

## Projects
<a name="ideas"></a> 

1. gather some colleagues and make a team of maximum 3 people
1. choose a topic that you would like to research; propose your own or [check the project list](https://cryptpad.fr/kanban/#/2/kanban/view/jas2VVWrT6jsBQY9tWByDx9FNjB-6tICxl7kZebQV2s/embed/)
1. make sure your topic does not overlap with other topics that are in progress and that have been chosen by your colleagues
1. email sergiu to announce your team, your proposal and to discuss how to approach it
1. after you obtain the approval, mark it as being in progress on the kanban list, and start working on it
1. prepare the project, a presentation, and a report [using this template](https://www.overleaf.com/read/dfsmrfysqdgb#de94a7)
1. place everything in a digital storage space somewhere: a git repo, a drive, some file on a server etc.; don’t send large files by email, send only URLs
1. current deadline for completing projects: January 20



## Introductory Course
<a name="intro"></a> 

- [Three Thousand Years of Algorithmic Rituals: The Emergence of AI from the Computation of Space](https://www.e-flux.com/journal/101/273221/three-thousand-years-of-algorithmic-rituals-the-emergence-of-ai-from-the-computation-of-space/), Matteo Pasquinelli 

<img src="https://upload.wikimedia.org/wikipedia/commons/e/e5/Gospers_glider_gun.gif"  width="600">

- Excerpt:

The term “algorithm” comes from the Latinization of the name of the Persian scholar al-Khwarizmi. His tract On the Calculation with Hindu Numerals, written in Baghdad in the ninth century, is responsible for introducing Hindu numerals to the West, along with the corresponding new techniques for calculating them, namely algorithms. In fact, the medieval Latin word “algorismus” referred to the procedures and shortcuts for carrying out the four fundamental mathematical operations—addition, subtraction, multiplication, and division—with Hindu numerals. Later, the term “algorithm” would metaphorically denote any step-by-step logical procedure and become the core of computing logic. In general, we can distinguish three stages in the history of the algorithm: in ancient times, the algorithm can be recognized in procedures and codified rituals to achieve a specific goal and transmit rules; in the Middle Ages, the algorithm was the name of a procedure to help mathematical operations; in modern times, the algorithm qua logical procedure becomes fully mechanized and automated by machines and then digital computers.


Looking at ancient practices such as the Agnicayana ritual and the Hindu rules for calculation, we can sketch a basic definition of “algorithm” that is compatible with modern computer science:

1. an algorithm is an abstract diagram that emerges from the repetition of a process, an organization of time, space, labor, and operations: it is not a rule that is invented from above but emerges from below;
2. an algorithm is the division of this process into finite steps in order to perform and control it efficiently; 
3. an algorithm is a solution to a problem, an invention that bootstraps beyond the constrains of the situation: any algorithm is a trick; 
4. most importantly, an algorithm is an economic process, as it must employ the least amount of resources in terms of space, time, and energy, adapting to the limits of the situation.

Today, amidst the expanding capacities of AI, there is a tendency to perceive algorithms as an application or imposition of abstract mathematical ideas upon concrete data. On the contrary, the genealogy of the algorithm shows that its form has emerged from material practices, from a mundane division of space, time, labor, and social relations. 



### References
<a name="intro_refs"></a> 

- [Language, Cohesion and Form (Studies in Natural Language Processing)](http://libgen.rs/book/index.php?md5=4EBE0188B1C9E63E3293BB70918F8C5A), Margaret Masterman, Yorick Wilks    
- [The Perceptron](https://blogs.umass.edu/brain-wars/files/2016/03/rosenblatt-1957.pdf), 
Frank Rosenblatt
- [Calculating Space](https://sferics.idsia.ch/pub/juergen/zuserechnenderraum.pdf), Konrad Zuse 
- [Algorithmic Theories of Everything](https://arxiv.org/abs/quant-ph/0011122), Jürgen Schmidhuber
- [Theory of Self-Reproducing Automata](https://cba.mit.edu/events/03.11.ASE/docs/VonNeumann.pdf), John von Neumann

---
---

## Exploratory Data Analysis, Federalist Papers, and Bayesian Inference
<a name="eda"></a> 

- [Inference in an Authorship Problem](https://ptrckprry.com/course/ssd/reading/Most63.pdf), Frederick Mosteller and David L. Wallace

<img src="https://upload.wikimedia.org/wikipedia/commons/thumb/1/16/Poisson_pmf.svg/1280px-Poisson_pmf.svg.png"  width="600">

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
\log{Odds(H, M | x)} =  \log{\frac{P(H)}{P(M)}} * \log{\frac{P(x | H)}{P(x | M)}}
$$

The initial odds [priors] $\log{\frac{P(H)}{P(M)}}$ are treated in Naive Bayes as the normalized counts for each author / class. The authors make extensive analyses of the impact of these priors, see Section 4C in the paper and Section 3.1C in the book. And they conclude by setting the initial odds as equally probable, turning them into a constant factor: *thus 1/2 is the initial odds determined by our beliefs prior to the execution
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

Based on the *Naive* assumption that words appear independently in a text, and the authors decision to set the priors as equally probable ($P(H) = P(M) = 1/2$) the log-likelyhood ratio for all feature words of interest $\{x_1, ..., x_n\}$ becomes:

$$
\text{decision} =  \log{\frac{P(x_1, ..., x_n | H)P(H)}{P(x_1, ..., x_n | M)P(M)}} \\
=\log \prod_{i=1}^{n} \frac{P(x_i| H)}{P(x_i | M)} \\
= \sum_{i}^{n} \log \frac{ P(x_i| H)}{ P(x_i | M)} \\
= \sum_{i}^{n} x_i \log{\frac{\mu_{H_i}}{\mu_{M_i}}} - w(\mu_{H_i}-\mu_{M_i})
$$

where $\mu_{H_i}$ and $\mu_{M_i}$ are estimated means of occurences / 1000 words for eaach individual word $i$.

<!--
<script src="https://cdnjs.cloudflare.com/ajax/libs/mathjax/2.7.7/MathJax.js?config=TeX-AMS-MML_HTMLorMML"></script>
-->


### References
<a name="eda_refs"></a> 

- [Understanding of Multinomial Naive Bayes for Text Classification](https://web.stanford.edu/~jurafsky/slp3/4.pdf), Jurafsky and Martin
- [Chapter 8 - Discrimination Problems](https://archive.org/details/advancedstatisti00raoc), Radhakrishna Rao 
- [Bayesian statistics](https://archive.org/details/in.ernet.dli.2015.2608/page/n129/mode/2up), Jeffries
- [Bayesian statistics](https://gwern.net/doc/statistics/decision/1961-raiffa-appliedstatisticaldecisiontheory.pdf), Raiffa and Schlaifer
- [Bayesian statistics](https://gwern.net/doc/statistics/decision/1972-savage-foundationsofstatistics.pdf), Savage




---
---


## Is Language Related to Thought? Are Machines Able to Think?
<a name="thought"></a> 


This is part of a wider philosophical regarding language and cognition. We shall only lift up the dust from these debates and point to the most lowdly-heard opinions.

---

### L. Wittgenstein
<a name="thought_witt"></a> 

<img src="https://api.architectuul.org/media/54eb15b4-9e1c-4ec7-b0de-76f16d7b5e1b/1600x900.jpg" width="600">


*A înţelege o propoziţie înseamnă a înţelege un limbaj.
A înţelege un limbaj înseamnă a stăpîni o tehnică.
Cum explic eu cuiva semnificaţia cuvintelor "regulat", "uniform", "acelaşi"?
Unuia care, să zicem, nu vorbeşte decât franceză, îi voi explica aceste cuvinte prin cuvintele franţuzeşti corespunzătoare. Dar cine nu posedă încă aceste noţiuni, pe acela îl voi învăţa să folosească cuvintele prin exemple şi prin exerciţiu.
Şi cînd fac asta, nu-i comunic mai puţin decît ştiu eu însumi.* Wittgenstein, Cercetări Filozofice

[Short summary of his work](https://plato.stanford.edu/entries/wittgenstein/#MeanUse):

“For a large class of cases of the employment of the word ‘meaning’—though not for all—this word can be explained in this way: the meaning of a word is its use in the language” (PI 43). This basic statement is what underlies the change of perspective most typical of the later phase of Wittgenstein’s thought: a change from a conception of meaning as representation to a view which looks to use as the crux of the investigation. Traditional theories of meaning in the history of philosophy were intent on pointing to something exterior to the proposition which endows it with sense. This ‘something’ could generally be located either in an objective space, or inside the mind as mental representation. As early as 1933 (The Blue Book) Wittgenstein took pains to challenge these conceptions, arriving at the insight that “if we had to name anything which is the life of the sign, we should have to say that it was its use” (BB 4). 

--- 

### N. Chomsky - The Psychology of Language and Thought
<a name="thought_chomsky"></a> 

[URL here](https://chomsky.info/1983____/)

<img src="https://i.pinimg.com/originals/8b/63/61/8b6361373652c10fdfe45486f8fa6e25.jpg" width="600">

QUESTION: What role does cognition play in the acquisition and development of language? Do linguistic factors influence general cognitive development?

CHOMSKY: I would like to re-phrase the first question and ask what role other aspects of cognition play in the acquisition of language since, as put, it is not a question I can answer. I would want to regard language as one aspect of cognition and its development as one aspect of the development of cognition. It seems to me that what we can say in general is this:

There are a number of cognitive systems which seem to have quite distinct and specific properties. These systems provide the basis for certain cognitive capacities — for simplicity of exposition, I will ignore the distinction and speak a bit misleadingly about cognitive capacities. The language faculty is one of these cognitive systems. There are others. For example, our capacity to organize visual space, or to deal with abstract properties of the number system, or to comprehend and appreciate certain kinds of musical creation, or our ability to make sense of the social structures in which we play a role, which undoubtedly reflects conceptual structures that have developed in the mind, and any number of other mental capacities. As far as I can see, to the extent that we understand anything about these capacities, they appear to have quite specific and unique properties. That is, I don’t see any obvious relationship between, for example, the basic properties of the structure of language as represented in the mind on the one hand and the properties of our capacity, say, to recognize faces or understand some situation in which we play a role, or appreciate music and so on. These seem to be quite different and unique in their characteristics. Furthermore, every one of these mental capacities appears to be highly articulated as well as specifically structured. Now it’s perfectly reasonable to ask how the development of one of these various systems relates to the development of others. Similarly, in the study of, say, the physical growth of the body, it makes perfect sense to ask how the development of one system relates to the development of others. Let’s say, how the development of the circulatory system relates to the development of the visual system.

But in the study of the physical body, nobody would raise a question analogous to the one you posed in quite this form. That is, we we would not ask what role physical organs and their function play in the development of the visual system. Undoubtedly, there are relations between, say, the visual and circulatory systems, but the way we approach the problem of growth and development in the physical body is rather different. That is, one asks — quite properly — what are the specific properties and characteristics of the various systems that emerge — how do these various organs or systems interact with one another, what is the biological basis — the genetic coding, ultimately — that determines the specific pattern of growth, function and interaction of these highly articulated systems: for instance, the circulatory system, the visual system, the liver, and so on. And that seems to provide a reasonable analogy, as a point of departure at least, for the study of cognitive development and cognitive structure, including the growth of the language faculty as a special case.

---

###  The Game / Игра - Анатолій Дніпров (1961)
<a name="thought_game"></a> 


<img width="600" src="https://github.com/senisioi/archaeology/blob/main/img/igra.png?raw=true">


[URL here](https://www.hardproblem.ru/en/posts/Events/a-russian-chinese-room-story-antedating-searle-s-1980-discussion/) short version on [wikipedia](https://en.wikipedia.org/wiki/Anatoly_Dneprov_(writer)#The_Game), trilingual [PDF here](http://q-bits.org/images/Dneprov.pdf)

A game on a stadium where people act according to mechanical and logical instructions to produce a translation from Portuguese.

"Outcries and laughter filled the hall for quite a while. Zarubin laughed with us. Then he shook his notebook in the air and, when the hall was silent again, he read slowly:
“Os maiores resultados sao produzidos роr – pequenos mas continues esforcos”.

This is a sentence in Portuguese. I don’t think you can guess what it means. However, it was you who yesterday made a perfect Russian translation. Here it is: “The greatest goals are achieved through minor but continuous ekkedt.”


“Remember that part of Turing’s article in which he said that to find out whether machines are able to think, you have to become a machine. Experts in cybernetics believe that the only way to prove that machines can think is to turn yourself into a machine and examine your thinking process.

Hence, yesterday we spent four hours operating like a machine. Not a fictional one, but a serial, domestic machine named Ural. If we had more people, we could have worked as Strela, Large Electronic Computing Machine, or any other computing machine. I decided to try Ural and used you, my dear young friends, as elements to build it at the stadium. I prepared a program to translate Portuguese texts, did the encoding procedure, and placed it into the “memory unit” – the Georgian delegation. I gave the grammatical rules to our Ukrainian colleagues, and the Russian team was responsible for the dictionary.

Our machine handled the mission flawlessly, as the translation of the foreign sentence into Russian required absolutely no thinking. You definitely understand that such a living machine could solve any mathematical or logical problem just like state-of-the-art electronic computing machines. However, that would require much more time. And now let us try to answer one of the most critical questions of cybernetics: Can machines think?”

“No!” everyone roared.

“I object!” yelled our “cybernetics nut,” Anton Golovin. “During the game we acted like individual switches or neurons. And nobody ever said that every single neuron has its own thoughts. A thought is the joint product of numerous neurons!”

“Okay,” the Professor agreed. “Then we have to assume that during the game the air was stuffed with some ‘machine superthoughts’ unknown to and inconceivable by the machine’s thinking elements! Something like Hegel’s noûs, right?”

Golovin stopped short and sat down.

“If you, being structural elements of some logical pattern, had no idea of what you were doing, then can we really argue about the ‘thoughts’ of electronic devices made of different parts which are deemed incapable of any thinking even by the most fervent followers of the electronic-brain concept? You know all these parts: radio tubes, semiconductors, magnetic matrixes, etc. I think our game gave us the right answer to the question ‘Can machines think?’ We’ve proven that even the most perfect simulation of machine thinking is not the thinking process itself, which is a higher form of motion of living matter. And this is where I can declare the Congress adjourned.”


---

### Thinking Machine Dehumanizing Women
<a name="thought_sexism"></a> 


<img width="600" src="https://github.com/senisioi/archaeology/blob/main/img/pygmalion_ErscoiKleinherenbrinkGuest2023.png?raw=true">

- image from [Pygmalion displacement paper](https://osf.io/preprints/socarxiv/jqxb6)
- [The Thinking Machine](https://www.youtube.com/watch?v=cvOTKFXpvKA) documentary from the '60s where the is moderator smoking a pipe nonchalantly.

I ask you to watch **who** are the people doing the actual research. Worth noting [minute 10:31](https://youtu.be/cvOTKFXpvKA?feature=shared&t=631) where somebody is being tested[^2]. To understand more about the context, see the recent [Pygmalion displacement paper](https://osf.io/preprints/socarxiv/jqxb6) by Lelia A. Erscoi, Annelies Kleinherenbrink, and Olivia Guest. Short excerpts below:

First, we examine the fictional fascination with AI, or minimally AI-like entities, e.g. automata, which are created with the explicit purpose to displace women by recreating artificially their typical social role (examples shown on the left and in pink in Figure 2). 

In the section titled Fictional Timeline, we trace the ways in which the misogyny expressed in the original telling of the Pygmalion myth has been echoed and transmuted over time, culminating in films like “Ex Machina” and “Her” in the 21st century. 

We follow up this analysis of Pygmalion-inspired fiction with a discussion of the work of Alan Turing[^3], in the section titled Interlude: **Can Women Think?**. Even though the Turing test is now widely understood to involve a machine being mistaken for a human — any human — the original test re volved around a computer being mistaken specifically for a woman (Genova, 1994). 

We therefore argue that Turing’s thought experiment can be seen as a case of Pygmalion displacement (i.e. the humanization of AI through the dehumanization of women). As such, it serves as a noteworthy bridge between fictional and actual attempts to replace women with machines. After this ‘interlude’, we develop our Pygmalion lens (Table 1), which is described in detail in the section titled The Pygmalion lens: real myths or mythical realities?.


In a further twist of dramatic irony, as we already alluded to above, the original Turing test is another instance of Pygmalion displacement. Turing introduces his original formulation of the test by means of “a game which we call the ‘imitation game’. 

It is played with three people, a man (A), a woman (B), and an interrogator (C) who may be of either sex. [...] The object of the game for the third player (B) is to help the interrogator. The best strategy for her is probably to give truthful answers. She can add such things as ‘I am the woman, don’t listen to him!’ to her answers, but it will avail nothing as the man can make similar remarks.” (pp. 433–434) Turing (1950) then asks “‘What will happen when a machine takes the part of A [the man] in this game?’ Will the interrogator decide wrongly as often when the game is played like this as he does when the game is played between
a man and a woman? These questions replace our original, **Can machines think?** (p. 434)

This description of the second test leaves some room for interpretation (Brahnam et al., 2011). The majority of interpretations suggest that Turing intends this second game as a test of human-likeness, in general, not of gender specifically (cf. Guest & Martin, 2023, wherein related but separate problems with adopting the test uncritically in the scientific study of brain and cognition are discussed). 

[...]

Turing invites us to accept that to convince the interrogator of their humanity, human-likeness, or both, machine and woman could answer questions that probe things like their ability to play masculinised games like chess (viz. Keith, 1994), but not patriarchal female-coded characteristics. “We do not wish to penalise the machine for its inability to shine in beauty competitions” [(Turing, 1950, p. 435)](https://academic.oup.com/mind/article/LIX/236/433/986238).

In an alternative reading, however, the judge is still tasked with figuring out which player is a woman, and the computer is programmed specifically to prove it is a woman (Genova, 1994; Kind, 2022). “Turing actually said that the method of the test was by imitating gender[, thus] the function to be performed [by the machine] is the imitation of a female person” (Keith, 1994, p. 334).

If this was indeed Turing’s intention, the computer imitates a man imitating (and outsmarting) a woman, and thus still emulates masculine thinking (Brahnam et al., 2011). In both understandings of the test, the machine is arguably not required to be exactly like women (defined in terms of stereotypes), in fact it has to surpass them by reproducing masculine thinking skills (again, stereotypically defined).


---

### The Language System in the Human Brain: Parallels & Differences with LLMs
<a name="thought_LLMs"></a> 



<img width="600" src="https://github.com/senisioi/archaeology/blob/main/img/schrimpf_et_al_2021.png?raw=true">


The neuroscience of perception has recently been revolutionized with an integrative modeling approach in which computation, brain function, and behavior are linked across many datasets and many computational models. By revealing trends across models, this approach yields novel insights into cognitive and neural mechanisms in the target domain. We here present a systematic study taking this approach to higher-level cognition: human language processing, our species’ signature cognitive skill. We find that the most powerful “transformer” models predict nearly 100% of explainable variance in neural responses to sentences and generalize across different datasets and imaging modalities (functional MRI and electrocorticography). Models’ neural fits (“brain score”) and fits to behavioral responses are both strongly correlated with model accuracy on the next-word prediction task (but not other language tasks). Model architecture appears to substantially contribute to neural fit. These results provide computationally explicit evidence that predictive processing fundamentally shapes the language comprehension mechanisms in the human brain.


To evaluate model candidates of mechanisms, we use previously published human recordings: fMRI activations to short passages (Pereira et al., 2018), ECoG recordings to single words in diverse sentences (Fedorenko et al., 2016), fMRI to story fragments (Blank et al. 2014). More specifically, we present the same stimuli to models that were presented to humans and “record” model activations. We then compute a correlation score of how well the model recordings can predict human recordings with a regression fit on a subset of the stimuli.
Since we also want to figure out how close model predictions are to the internal reliability of the data, we extrapolate a ceiling of how well an “infinite number of subjects” could predict individual subjects in the data. Scores are normalized by this estimated ceiling.

So how well do models actually predict our recordings? We tested 43 diverse language models, incl. embedding, recurrent, and transformer models. Specific models (GPT2-xl) predict some of the data near perfectly, and consistently across datasets. Embeddings like GloVe do not.
The scores of models are further predicted by the task performance of models to predict the next word on the WikiText-2 language modeling dataset (evaluated as perplexity, lower is better) – but NOT by task performance on any of the GLUE benchmarks. 

- from the original 2021 [paper](https://mschrimpf.altervista.org/artificial-neural-networks-accurately-predict-language-processing-in-the-brain/)
- [Highly recommended presentation](https://www.youtube.com/watch?v=uE9AiYuCwdE) by Ev Fedorenko

---
 
### References 
<a name="thought_refs"></a> 


- [Automating Gender: Postmodern Feminism in the Age of the Intelligent Machine](https://www.jstor.org/stable/3178281), Judith Halberstam
- [Pygmalion Displacement: When Humanising AI Dehumanises Women](https://doi.org/10.31235/osf.io/jqxb6), Erscoi, L., Kleinherenbrink, A., & Guest, O.
- [Language Is a Poor Heuristic For Intelligence](https://karawynn.substack.com/p/language-is-a-poor-heuristic-for), Karawynn Long
- [Reclaiming AI as a theoretical tool for cognitive science](https://doi.org/10.31234/osf.io/4cbuv), van Rooij, I., Guest, O., Adolfi, F. G., de Haan, R., Kolokolova, A., & Rich, P.
- [The neural architecture of language: Integrative modeling converges on predictive processing](https://evlab.mit.edu/assets/papers/Schrimpf_et_al_2021_PNAS.pdf), Schrimpf, M., Blank, I., Tuckute, G., Kauf, C., Hosseini, E., Kanwisher, N., Tenenbaum, J.,  Fedorenko, E
- [Other Papers from the Brain and Language Lab](https://evlab.mit.edu/research/index.html)
- [On Chomsky and the Two Cultures of Statistical Learning](http://norvig.com/chomsky.html), debate with P. Norvig
- [Does a language model trained on “A is B” generalize to “B is A”?](https://arxiv.org/abs/2309.12288), Lukas Berglund, Meg Tong, Max Kaufmann, Mikita Balesni, Asa Cooper Stickland, Tomasz Korbak, Owain Evans
- [Unthought: the power of the cognitive nonconscious](https://ageingcompanions.constantvzw.org/books/Unthought_N._Katherine_Hayles.pdf), Katherine Hayles
- [The Future Looms: Weaving Women and
Cybernetics](https://monoskop.org/images/1/13/Plant_Sadie_1995_The_Future_Looms_Weaving_Women_and_Cybernetics.pdf), Sadie Plant

---
---


## Side-story: Estimating Parameters from Data
<a name="map_mle"></a> 

We have seen in the Federalist papers how the log-likelihood ratio has been used to make a decision rule for a classifier. You will often hear or read that probabilities for words are estimated using a maximum likelihood estimator by counting the number of occurences to the total. But what is "maximum likelihood"?


Remember the following two basic rules of probabilities:
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

Hopefully it is more clear now, that if we talk about maximum likelihood estimation, it is probably related to the likelihood term $P(B|A)$ in the above equation.

Let's start with the simplest example: we have a binary coin that returns 0, 1. We don't know at this point if the coin has been rigged and we want to use data (observed trials) to define a set of beliefes. Which one is more likely 0 or 1? Are they really equally probable? 

By common sense would say each coin has the same probability, e.g., the probability of seeing $1$ is $\theta=1/2$ and that the coin is not rigged, but we can't be sure untill we see it. Sidenote, if someone is very skilled at throwing coins, it could also trick us to see what we we expect to see; is there any way to measure that?


By seeing something, here we mean that we have some observations or some data $D = \{1,1,1,1,0\}$. We can characterize this dataset by its size $|D| = N$. We assume the data is generated randomly using a probability distribution. Given our knowledge of the world, we can make an **explicit assumption** by saying this data is made of independent events, each event being from generated with a [Bernouli distribution](https://en.wikipedia.org/wiki/Bernoulli_distribution) (iid). We could also model the data as a [Binomial distribution](https://en.wikipedia.org/wiki/Binomial_distribution), which describes the success of $N$ binary (Bernouli) independent events, each with probability $\theta$. We know the Bernouli distribution is parameterized by $\theta$ (from its definition), therefore our question is:
- what are the most likely parameters $\theta$ of the Bernouli probability distribution $P(; \theta)$ that explain the data $D = \{x_1, x_2, ..., x_N\}$? let's note this as $\hat{\theta}$

By the Maximum Likelihood Estimation, we can model $\hat{\theta}_{\text{MLE}} = \argmax_{\theta} P(D; \theta)$ since the likelihood is the most important factor in the above Bayes' rule. But there is also the Bayesian possibility of modelling the maximum a posteriori probability $\hat{\theta}_{\text{MAP}} = \argmax_{\theta} P(\theta | D)$.

### Maximum Likelihood Estimation
<a name="mle"></a> 


For our coin, we have a **parameter** $0 \leq \theta \leq 1$ that gives us the chance for the coin to give value 1:

$$
\begin{align}
P(x=1 | \theta) = \theta , \\ 
P(x=0 | \theta) = 1-\theta
\end{align}
$$

and

$$
\begin{align}
\hat{\theta} &= \operatorname*{argmax}_{\theta} p(D; \theta) \\
&= \operatorname*{argmax}_{\theta} \prod_{i=1}^{N} p(x_i| \theta) \\
&= \operatorname*{argmax}_{\theta} \prod_{i=1}^{N} \theta^{x_i}(1-\theta)^{1-x_i}   
\end{align}
$$

To maximize the function we can:

1. use log values (log-likelihood) to aid our computation (we can do this because the log is monotonic and the likelihood is positive)
1. take the derivative and equate with zero to find points of extreme
1. check the second derivative is negative to make sure it's not a point of minimum

$$
\begin{align}
\mathcal{l}({\theta}) &=  \log \theta \sum_{i=1}^{N}x_i + \log (1-\theta) \sum_{i=1}^{N}(1-x_i) 
\end{align}
$$

the sums above can be denoted as two constants defined by counts: $c = \sum_{i=1}^{N}x_i$ and $d = \sum_{i=1}^{N}(1-x_i) = N - c $,

then if we equate with zero:
$$
\frac{\partial\mathcal{l}(\theta)}{\partial \theta} = \frac{\partial c\log\theta + d\log(1-\theta)}{\partial \theta} = 0
$$
and we get
$$
c\frac{1}{\theta} - (N-c)\frac{1}{1-\theta} = 0 \\
c(1-\theta) = (N-c)\theta \\
$$
therefore
$$
\hat{\theta}_{\text{ML}} = \frac{c}{N} = \frac{\sum_{i=1}^{N}x_i}{N}
$$

which is equivalent to saying that the maximum likelihood estimator is the relative frequency of an event: the number of counts of an event divided by the total number.

### Conjugate Prior
<a name="conj"></a> 

We obtain similar estimations for the Binomial distribution which is defined by the rate of success of $N$ Bernouli trials, equiavalent to asking what is the probability of seeing $c$ successes (sum of all ones is $c$) after $N$ trials with binary probability $\theta$. If we preserve the previous notation of $c$ occurences of 1 and $d = N-c$ occurences of 0, then:

$$
Bin(c | \theta, N) = \begin{pmatrix} N \\ c \end{pmatrix} \theta^c(1-\theta)^{d}
$$
where ${\displaystyle \begin{pmatrix} N \\ c \end{pmatrix} = \frac{N!}{c!(N-c)!} = \frac{(b+c)!}{c!d!} = \begin{pmatrix} b+c \\ c \end{pmatrix}}$ represents combinations of N taken c. A constant value that we use for everything to sum up to one.
The binomial distribution is a function that depends on $k$ and the distribution parameters are $\theta$ and $N$.


In the above example with $D = \{1,1,1,1,0\}$, the maximum likelihood estimator would yield $P(x=1)=4/5$ which is not a very good estimator for what we would expect to be a real-life coin flip scenario. If by some chance, the data is small or is dominated by a single value, then the maximum likelihood estimator does not give very good predictions.

To tackle this problem, we can apply Bayesian statistics and assume that $\theta$ is drawn from a distribution $P(\theta)$, which means there are some values that we expect to be more reasonable for our event space. 

Now we can use Bayes' Theorem and say:
$$
P(\theta \mid D) = \frac{P(D\mid \theta) P(\theta)}{P(D)}
$$
For the Binomial distribution, we were looking at a distribution to give us the probability of $k$ successes, but now we need a distribution to give us the probability of a probability $\theta$.
But what distribution can we use to model the the probability of the prior $P(\theta)$?

Since $0 \leq \theta \leq 1$, we need to find a continuous probability distribution. We could use the Gaussian distribution, no? Well, according to [Bayesian statistics](https://gregorygundersen.com/blog/2019/03/16/conjugacy/), it is more feasible to choose a distribution that has the same functional form as the likelihood function $P(D|\theta)$ and when we do this we call our chosen distribution the **conjugate** to the likelihood.


The prior with the same functional form as the Binomial is called the Beta distribution given by:

$$
Beta(\theta | a,b) = B(a,b) * \theta^{(a-1)} * (1-\theta)^{(b-1)}
$$
where $a$ and $b$ are distribution (hyper)parameters and $B(a,b)$ is a coefficient that depends on $a$ and $b$ used to normalize everything between 0 and 1. 
Unlike the Binomial (where we modelled the probability of successes $c$) this distribution gives the porbability of the probability value $\theta$ and the distribution parameters are $a$ and $b$.

The constant $B(a,b)$ is similar in concept to the Binomial version and is given by the inverse of the [Beta function](https://en.wikipedia.org/wiki/Beta_function):
$$
B(a,b) = \frac{\Gamma(a+b)}{\Gamma(a)\Gamma(b)}
$$
The [$\Gamma$ function](https://en.wikipedia.org/wiki/Gamma_function#Motivation) is the extension of the factorial function: ${\displaystyle \Gamma (z)=\int _{0}^{\infty }t^{z-1}e^{-t}{\text{ d}}t,\ \qquad \Re (z)>0\,}$ for any complex number $z \in \mathbb{C}$ whose real part is strictly positive. A factorial is a function that obeys the recursive property $f(x+1) = xf(x)$.

If we set $a$ and $b$ as complementary integers $a+b = N$, we can see that the coeficient is identical to the combinations: ${\binom {a+b}{a}}$ in the Binomial distribution. You may play with the [scipy implementation](https://docs.scipy.org/doc/scipy/reference/generated/scipy.special.gamma.html) to get a hands on some examples.

### Maximum a Posteriori (MAP)
<a name="map"></a> 

Getting back to our Bayes' rule to find the best $\theta$ given the data: $P(\theta \mid D) = \frac{P(D\mid \theta) P(\theta)}{P(D)}$, we can see that this is equivalent to saying:

$$
\begin{align}
P(\theta \mid D) &= 
C(a,b,c,d) * \theta^c(1-\theta)^{d} * \theta^{(a-1)} * (1-\theta)^{(b-1)} \\
&= C(a,b,c,d) * \theta^{(c + a-1)} * (1-\theta)^{(d+ b-1)} \\
&\propto  \theta^{(c + a - 1)} * (1-\theta)^{(d + b - 1)} \\
\end{align}
$$
where $C(a,b,c,d) = B(c+a, d+b)$ is the normalizing constant.

$a$ and $b$ are hyperparameters that change the shape and assumptions of the distribution. Exercise: use scipy to plot the Beta distribution for different parameters and see which ones would fit the assumption about the coin. Alternatively, check the plots from [Gregory Gundersen](https://gregorygundersen.com/blog/2019/03/16/conjugacy/) below:

<img src="https://gregorygundersen.com/image/conjugacy/beta.png"  width="600">

Let's set the params to equal values $ a=b=2 $ for now since our knowledge of a fair coin resembles the third plot above.



Using the conjugate form is advantageous for the posterior has the same functional dependency on $\theta$ as the prior and the likelihood, which makes calculating the derivative of the above formula with respect to $\theta$ easy -- it will have the same shape as the one for Maximum Likelihood:

$$
\hat{\theta}_{\text{MAP}} = \frac{c+a - 1}{c+a -1 + d+b -1} = \frac{c+a - 1}{N + a + b -2}
$$

Given the previous dataset $D = \{1,1,1,1,0\}$, the number of successes $c=4$ and given that we set our values $a=b=2$ the $\hat{\theta}_{\text{MAP}} = \frac{5}{7} = .71$ which is a slightly smoother estimate than the $\hat{\theta}_{\text{ML}} = \frac{4}{5} = .8$

If we have no data, then the $\hat{\theta}_{\text{MAP}}= \frac{1}{2}$.

The conjugate prior is useful as a method of sequential learning because the posterior can act as prior as we see more data. Running the experiment one toss of the coin by one, we can increment $c$ and $N$ each time we have a success or we increase $d$ and $N$. Or if we fix these, we just increment $a$ and $b$ which gives meaning to these hyperparamters of the Beta distribution.

I leave the following paragraph from C Bishop's book where you can read more about Pattern Recognition and Machine Learning:

We see that this sequential approach to learning arises naturally when we adopt a Bayesian viewpoint. It is independent of the choice of prior and of the likelihood function and depends only on the assumption of i.i.d. data. Sequential methods make use of observations one at a time, or in small batches, and then discard them before the next observations are used. They can be used, for example, in real-time learning scenarios where a steady stream of data is arriving, and predictions must be made
before all of the data is seen. Because they do not require the whole data set to be stored or loaded into memory, sequential methods are also useful for large data sets. Maximum likelihood methods can also be cast into a sequential framework.


### References
<a name="map_mle_refs"></a> 

- [The Gamma Function](https://web.archive.org/web/20161112081854/http://www.plouffe.fr/simon/math/Artin%20E.%20The%20Gamma%20Function%20(1931)(23s).pdf), 1964, Emil Artin
- [The Epic Story of Maximum Likelihood](https://arxiv.org/pdf/0804.2996.pdf), Stephen M. Stiegler
- [Conjugacy in Bayesian Inference](https://gregorygundersen.com/blog/2019/03/16/conjugacy/), Gregory Gundersen
- [Pattern Recognition and Machine Learning](https://github.com/peteflorence/MachineLearning6.867/blob/master/Bishop/Bishop%20-%20Pattern%20Recognition%20and%20Machine%20Learning.pdf), Christopher Bishop, 2006
- [Probabilistic Programming and Bayesian Methods for Hackers](https://nbviewer.org/github/CamDavidsonPilon/Probabilistic-Programming-and-Bayesian-Methods-for-Hackers/blob/master/Chapter1_Introduction/Ch1_Introduction_PyMC3.ipynb)
- [Lecture Notes from ](https://www.cs.cornell.edu/courses/cs4780/2021fa/lectures/lecturenote04.html)

---
---


## Entropy
<a name="entropy"></a> 
TBA

### References
<a name="entropy_refs"></a> 

- [First Links in the Markov Chain](https://www.americanscientist.org/article/first-links-in-the-markov-chain), Brian Hayes
- [Entropia Limbii](http://dspace.bcu-iasi.ro/handle/123456789/2760), 1963, Solomon Marcus & Sorin Stati 
- [A Mathematical Theory of Communication](https://people.math.harvard.edu/~ctm/home/text/others/shannon/entropy/entropy.pdf), 1948, Claude Shannon
- [Prediction and Entropy of Printed English](https://www.princeton.edu/~wbialek/rome/refs/shannon_51.pdf), 1951, Claude Shannon
- [Easy-to-follow blog post on information theory](https://colah.github.io/posts/2015-09-Visual-Information/)

---
---

## Cybernetics
<a name="cybernetics"></a> 
TBA

### References
<a name="cybernetics_refs"></a> 

- [Cybernetic Revolutionaries ](), Eden Medina
- [Interview with Nils Gilman](https://the-santiago-boys.com/interviews/nils-gilman)


[^1]: *even a motherly eye*? worth noting a random sexist remark in an academic paper of the '60s

[^2]: ask youreself who is being tested and what game is being used. The river crossing problem is rooted in a history of [sexism, racism, and colonialism](https://pballew.blogspot.com/2022/09/a-brief-history-of-river-crossing.html). What were the missionaries doing there anyways?

[^3]: Alan Turing has been infamously [persecuted for being LGBTQ+](https://www.thepinknews.com/2023/06/06/alan-turing-gay-who-was-did-eingma-die-death-facts/); also Wittgenstein was [allegedly queer](https://www.newyorker.com/magazine/2022/05/16/how-queer-was-ludwig-wittgenstein) and [strongly mysoginistic](https://www.nordicwittgensteinreview.com/article/view/3651/9)