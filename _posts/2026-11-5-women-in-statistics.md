---
layout: post
title: "Women In Statistics"
author: Daniel Schmidt
---

A incomplete list of influential women in statistics.

<!--more-->

## (Some) women who shaped statistics: an incomplete list

I recently suggested to my postdoc, [Dr.Sherilyn (Xueying) Long](https://github.com/xueyinglong), that she might find Dennis Lindley’s [“Bayesian thoughts”](https://doi.org/10.1111/j.1740-9713.2004.027.x) an interesting read (as he is a scientific inspiration for myself). She did so, but then asked an important follow-up question: what material from female statisticians could I recommend for her to read? There are naturally many female statisticians who have made profound contributions to our field, so my list is influenced by my own personal biases and experiences. 

With that in mind, Grace Wahba’s spline book came to mind first, followed by Sara van de Geer’s book on empirical processes and Grace Lo Yang’s book with Lucien Le Cam on asymptotics. As it was an interview article that had prompted the question, I also started looking for conversations as well. This is of course important because it is great to have professional role-models. Here are a few suggestions for people interested in reading about women who made fundamental contributions to statistics specifically, and by extension, machine learning and data science in general.

## Grace Wahba and the roots of kernel learning

I would pair Wahba’s classic book [*Spline Models for Observational Data*](https://doi.org/10.1137/1.9781611970128) with [“A Conversation with Grace Wahba”](https://doi.org/10.1214/19-STS734) in *Statistical Science*. Her interview gives a sense of how she came to the mathematics, including being introduced to reproducing kernel Hilbert spaces (RKHSs) from Emanuel Parzen.

In [a 1970 paper](https://doi.org/10.1214/aoms/1177697089), Wahba and George Kimeldorf demonstrated that a smoothing spline can arise as a Bayesian estimate under a suitable stochastic process prior. In [their 1971 paper](https://doi.org/10.1016/0022-247X(71)90184-3), they then showed how to solve a class of smoothing problems in an RKHS. The striking feature is that you can search over an infinite-dimensional function space and still express the answer using a finite span determined by the observations, which is of course, the idea behind the representer theorem.

Unfortunately, I feel that Wahba’s crucial part in this story is easy to underestimate if you first meet kernel methods through machine learning. While Schölkopf, Herbrich and Smola explicitly credit her theorem in [their 2001 generalisation](https://alex.smola.org/papers/2001/SchHerSmo01.pdf), reading the earlier work makes clear how much of the framework for regularised function estimation was already in place.

## Evelyn Fix and nearest neighbours

Anyone who has taught *k*-nearest neighbours has a reason to know Evelyn Fix’s name. In a [1951 Berkeley report](https://cs.nyu.edu/home/people/in_memoriam/roweis/csc2515-2006/readings/fix_hodges_51.pdf), Fix and Joseph Hodges studied the problem of classifying an observation when you have access to labelled examples, but don’t know the underlying class distributions. Their proposal is of course very familiar now: we can use the labels of nearby observations to decide how to label a new observation. Fix and Hodges studied when a classification rule built from such local estimates could approach the accuracy of the Bayes classifier as the training sample grew.

Fix herself came to statistics through mathematics and school teaching, and she joined Berkeley’s Statistical Laboratory during the second world war. There is a great connection to Elizabeth Scott (see below) as well: Scott was one of the colleagues who wrote Fix’s memorial, which Berkeley revisited in its [department newsletter](https://statistics.berkeley.edu/sites/default/files/news/SPRING%202021%20NEWSLETTER%20-%20STATS.pdf).

## Asymptotics and likelihood

Sara van de Geer’s [*Empirical Processes in M-Estimation*](https://assets.cambridge.org/052165/002X/description/052165002X_description.htm) is a good choice if you want to understand how the complexity of a class of functions governs what you can estimate. Her [*Estimation and Testing Under Sparsity*](https://doi.org/10.1007/978-3-319-32774-7) takes up a related set of questions in high-dimensional models.

Lucien Le Cam and Grace Lo Yang’s [*Asymptotics in Statistics: Some Basic Concepts*](https://doi.org/10.1007/978-1-4612-1166-2) has one of my favourite subtitles; “Basic” here meaning these concepts form the basis for much asymptotic statistics, rather than "elementary" :). One probably realises this quite quickly when one finds themselves comparing statistical experiments and trying to get comfortable with concepts like contiguity. I was unable to find a published interview with Yang about her own career, but she did interview her coauthor for *Statistical Science* in [“A Conversation with Lucien Le Cam”](https://doi.org/10.1214/ss/1009212249).


## Nancy Reid and profiling

Nancy Reid started out in computer science at Waterlo, then then obtained a master’s at UBC in applied mathematics. In [her conversation with Radu Craiu and Grace Yi](https://utstat.utoronto.ca/craiu/Papers/nancy_int.pdf), she recalls that her supervisor, Jim Zidek, handed her a deck of punched cards for fitting a Cox proportional hazards model and left her to see what she could learn from a set of coronary bypass data. Zidek encouraged her to apply to Stanford, where she completed her PhD in 1979. She then spent a year visiting David Cox at Imperial College, returned to UBC as a faculty member and moved to Toronto in 1986. She later chaired Toronto’s statistics department, directed the Canadian Statistical Sciences Institute and received the inaugural David R. Cox Foundations of Statistics Award in 2023. [Reid also talks about that part of her career in a CANSSI interview.](https://canssi.ca/speaking-about-statistics-a-conversation-with-nancy-reid/)

The [1987 paper with Cox on parameter orthogonality](https://academic.oup.com/jrsssb/article/49/1/1/7027797) is especially close to my own interests. They ask what happens to inference about a parameter of interest when you cannot avoid fitting nuisance parameters along the way. They reparameterise the nuisance component so that its Fisher information cross-block with the parameter of interest is zero, allowing them to derive an adjusted profile likelihood motivated by approximate conditioning.

One paper I discovered while researching this list is Reid’s [*Asymptotics and the Theory of Inference*](https://utstat.toronto.edu/reid/research/AOS201.pdf), which is based on her Wald Memorial Lectures and published in the *Annals of Statistics* in 2003. This looks like a wonderfully deep exposition on inference. The paper appears to use higher-order approximations to ask what information the data contain, and how different inferential procedures are able to extract this information. She brings likelihood, conditioning and Bayesian inference into the same discussion, including when Bayesian and frequentist tail probabilities agree. The [case studies in her book, *Applied Asymptotics*](https://www.cambridge.org/core/books/applied-asymptotics/73F7B67166213303C976456A2C6AA95F) show how that kind of refinement plays out in practice.

## Elizabeth Scott and nusiance parameters

Elizabeth Scott has a particular appeal for me because of the classic [1948 paper she wrote with Jerzy Neyman](https://doi.org/10.2307/1914288). Their incidental parameter example shows that maximum likelihood can give an inconsistent estimate of a common variance when each new group adds a nuisance mean and there are only two observations per group. It’s an exceptionally simple example of how the way we handle nuisance parameters can change what we actually end up learning.

Scott brought the same level of attention to what an analysis can reveal, or conceal, to her studies of academic pay. She pointed out that controlling for rank could hide some of the salary disparity, if women had already faced discrimination in promotion. Amanda Golbeck tells that story in [*Significance*](https://academic.oup.com/jrssig/article/14/6/38/7029369). Scott herself speaks about barriers to women in astronomy, and general life at Berkeley, in [Suzanne Riess’s oral history interview](https://digicoll.lib.berkeley.edu/record/217514?v=pdf), published in the Bancroft Library’s history of the Women’s Faculty Club.

## Ingrid Daubechies and wavelets

While not specifically a statistician, I’d also make room for Baroness Ingrid Daubechies. Her route into the story is through mathematics and physics, and in her [1988 paper](https://math.duke.edu/~ingrid/publications/cpam41-1988.pdf), she constructed compactly supported orthonormal wavelets with arbitrarily high regularity. The compact support lets you describe features in a small part of a signal, while the different scales let you pick out both fine and coarse structure.

A important connection of her work to statistics is via [Donoho and Johnstone’s work on wavelet shrinkage](https://doi.org/10.1093/biomet/81.3.425). Essentially, if you have a signal that is smooth in some places and changes abruptly in others, you can shrink small wavelet coefficients to reduce noise and retain the large ones that carry local structure, a process which yields optimal adaptive signal estimation, in a certain sense. For Daubechies’s own account of how she came to work in wavelets, there is a [video interview from CIRM](https://www.carmin.tv/en/collections/interviews-at-cirm/video/interview-at-cirm-ingrid-daubechies).

## Two more conversations

Finally, I’d also recommend [Louise Ryan’s conversation with Nan Laird](https://doi.org/10.1214/15-STS528) for the story behind some of the work on the famous expectation maximization (EM) algorithm and missing data, and [Laird’s conversation with Florence Nightingale David](https://www.dcscience.net/conversation-with-Florence-Nightingale-David.pdf) for a view of a very different era in statistics. There is a nice connection to my postdoc’s question. [Laird recalled](https://magazine.amstat.org/blog/2020/03/10/florence-n-david/) asking about women role models as a graduate student, and years later she remarked to Persi Diaconis that the *Statistical Science* interviewees were always men. He encouraged her to do an interview herself, and helped put her in touch with F.N.David.

## And beyond ...

This is just a smattering of women who have contributed to statistics, one way or another, other the years. Those who I have omitted should not be taken to be uninteresting, or unimportant -- rather the list I have pu together is a product of my own interests as much as anything else! If you have any suggestions of people I should include on this list, drop me an email!
