---
title: Drug repurposing with an algorithm and COVID-19
date: "2020-04-08T00:40:21"
template: "post"
draft: false
slug: "drug-repurposing-with-an-algorithm-covid-19"
category: "precision medicine"
tags:
  - "covid-19"
  - "machine learning"
  - "programming languages"
  - "precision medicine"
description: "Programmers will recognize in drug repurposing a hack. Of great significance, though."
# socialImage: "/media/image-2.jpg"
---

- [The algorithm for Precision Medicine](#the-algorithm-for-precision-medicine)
- [What's drug repurposing](#whats-drug-repurposing)
- [New AI](#new-ai)
- [COVID-19](#covid-19)
- [Closing](#closing)
- [Further reading](#further-reading)

With tremendous human cost of COVID-19, I’ve been wondering if there’s anything I could contribute to mitigating or solving this emergency, especially given my interest in the intersection of machine learning and biology. Coincidentally, I’ve heard of drug repurposing in a TV interview. Marcin Drąg, a professor of biochemistry, was talking about his recent research on a key enzyme related to the coronavirus.
He was explaining (to the extent a TV environment enables it) how his research has a chance to contribute significantly to the development of a vaccine for the coronavirus. “But that’s at least 18 months away. Short-term, I think the most promising direction is to take these results and try to repurpose existing drugs” - he said in the interview. I’ve never encountered the “drug repurposing” term before, but upon looking it up I considered it a neat idea. That kicked off a small research project on drug repurposing I’m summarizing here and relating with what I already know.

_NOTE: I’m using COVID-19 term where SARS-CoV-2 is more appropriate. I’m yielding to the common trend of using “coronavirus”, “COVID-19” and “SARS-CoV-2” interchangeably by the public._

## The algorithm for Precision Medicine
I mentioned to [Nada Amin](https://twitter.com/nadamin) my interest and asked her casually if she knew anybody working in that area. She immediately told me to check out Matt Might’s work. A quick search revealed some interesting blog posts by Matt but only once I stumbled upon his [keynote](https://www.youtube.com/watch?v=JTU3JYp3JYc), it clicked for me how _spot on_ Nada’s recommendation was. At 548 views (at the time of writing this), I think this might the most underrated talk I have ever seen on YouTube. It’s a well-established practice to give variants of the same talk repeatedly, and possibly one of them got more widespread attention. But until I see a more popular version, I’ll stick to the most underrated label. The talk has all the good ingredients of a keynote: inspiration, a new perspective, simplicity, and fun. If you have an hour on your hands, just go [watch it](https://www.youtube.com/watch?v=JTU3JYp3JYc).

Instead of trying to rehash the talk, I’m publishing my notes and highlights from the keynote that drew my attention.

There’re a few things that particularly stood out for me in this talk. Let’s start with the twist: it’s a medical talk given at an academic conference on programming languages (PL)research. My background in programming languages (and compilers) always felt like a strange badge: among programmers, it’s seen obscurely elite but I saw it myself as an extreme niche I stepped into by a mix of fluke and happy curiosity.
When I made my decision to shift my focus from systems programming (under which compilers fall) to machine learning and its applications in biology, I was sure I earnestly waved goodbye to programming languages’ underpinnings. The bigger the surprise is to watch a former PL researcher explain how he applied ideas from relational programming to model biological knowledge and surface previously unknown applications of existing drugs. 
Matt Might’s talk starts with an interesting tidbit I didn’t know: Alan Turing is a famous biologist (!). His second most widely cited paper is not on the theory of computation but [structure formation](https://scholar.google.com/citations?user=VWCHlwkAAAAJ#d=gs_md_cita-d&u=%2Fcitations%3Fview_op%3Dview_citation%26hl%3Den%26user%3DVWCHlwkAAAAJ%26citation_for_view%3DVWCHlwkAAAAJ%3Au5HHmVD_uO8C%26tzom%3D-120) arising from biological cells. This a reminder that the interplay between computer science and biology has a long history.
Past the trivia, we get to the central claim of the talk: data is the greatest drug of the 21st century. You can deliver data as a drug with precision medicine, Matt Might argues. The rest of the talk gives a compelling case to back that claim up with rare genetic diseases serving as the case study.

## What’s drug repurposing?

Drug repurposing is about finding a novel way of applying an existing drug or a whole cocktail of them. This often involves discovering or exploiting a side effect. This is like how great hacks in programming work: you bend some system to behave in a way the original designer didn’t think of. How do you do that for drugs? If you have a search problem, you can go about it at least two ways: a) “try all of them” known as brute-force search b) more principled exploration. 
If you hear about brute force search, you immediately need to think of how many distinct cases you need to consider. And here comes a surprise: there’re only 2-3 thousand approved drugs. For some reason, I thought the number would be much larger. For the brute force approach, you need also criteria that tell you if the drug works. You need a model of a disease and a way of manipulating it with drugs and observing their effects. You can get a biological model by growing a population of cells with the disease (e.g. genetic modification), applying drugs to cells and observing their effects using e.g. high-resolution microscopy. The challenge with this approach is both in the cost of growing cells and then analyzing all the data from thousands of experiments. 
The other way is to model the underlying mechanism of the disease and connect it with all of humanity’s knowledge about how disease biology works. Matt Might talks about how logic programming can be used for ingesting protein reactions biologists have already studied and for inferring new reaction chains that connect the signature of the disease to a signature of a potential treatment. From there, you can look for drugs that match the signature, again using similar inference chains. What stroke me was how relatively basic techniques are hugely effective. This is an old-school Artificial Intelligence people used to work on in the 80s and proves to be useful for finding previously unknown therapies.

## New AI
An immediate reaction one should have: what if we used methods from the 2010s, i.e. deep learning? In the talk, Matt Might, repeatedly stressed the importance of a proof: you need to give logical reasoning behind trying an unproven drug or no doctor will take you seriously. I think that’s a very good and non-obvious point about the practical reality of taking a computer-generated recommendation and handing it to a domain expert, i.e. a doctor. Accompanying the actual suggestion with proof is a natural strength of logic-based AI. So why would you reach out for newer modeling methods that struggle with explainability? The downside of logic-based AI is that it deals poorly with noisy or non-structural data. The logical inference Matt Might described in his talk works on top of a knowledge graph mined from 30 million of medical and biological publications. To extract the knowledge about proteins, enzymes and other building biological building blocks, he mentioned the use of Natural Language Processing. Matt Might didn’t comment directly on what flavor of NLP he used but indirectly I gathered it’s again an old-school, rule-based NLP (based on “parsing” remark) that most people have moved on from. I worked on a large-scale, modern NLP project and, in practice, NLP is always a mix of modeling and heuristics that everyone is embarrassed about. In fact, Matt suggested NLP as one of the areas that would use improvement. In any case, if you are mining 30 million medical papers written by people working in natural sciences, you’re working with a highly uncurated dataset and you’ll have noise or wrong data in the output of the NLP processing step. I’m curious how Matt’s group is dealing with this problem given the next step is highly sensitive to bogus relationships being rules- and not statistics-based.
If we accept that the knowledge graph itself is imperfect and noisy (e.g. some relations are bogus), can we work with it effectively? Yes, with statistical approaches that made great strides in recent years in tackling tasks in the knowledge base domain.
I think the first thing to try would be to see if graph embeddings could be up for the task. Practically, I would take the existing graph Matt Might’s group already has and use something like [PyTorch-BigGraph](https://github.com/facebookresearch/PyTorch-BigGraph) for knowledge graph processing and inference. BigGraph specifically achieves State-of-The-Art results on common knowledge base tasks and offers great scalability, which is often a challenge when working with graphs. I applied BigGraph to a large graph where, according to my back-on-envelope estimates, 50% of input data in the graph was garbage. The challenge was that I didn’t know which 50% of edges were bogus (not contributing anything to the task I was trying to solve) and still I get surprisingly good results. This is something not commonly known: deep learning methods are robust against noise as long as it’s unbiased. I think it would be tremendously interesting to compare the results of graph embeddings (new AI) and old-school logic programming. In summary, you could try to apply “new AI” in two areas:


1. Mining medical and biological publications to form the knowledge graph
2. Solving particular tasks (e.g. link prediction) on the knowledge graph itself

The talk didn’t go technical enough for me to gauge whether these two make sense. I know that especially 2. would be problematic for the “Must come with a proof” argument. However, my mind is set on the topic that everyone is thinking about, COVID-19.

## COVID-19
Could the system Matt Might described be readily applied to drug repurposing in a rush to minimize the damage of coronavirus on people’s health and the economy? The answer is yes, and Matt Might is admirably open on Twitter about his progress. To the extent, a frantic pace of work on COVID-19 allows, though. Even though the system was fine-tuned for rare genetic diseases, there’s no fundamental reason why it couldn’t be.. repurposed for viral infections. The two problems are closer to each other than one might think. Genetic disease is a mutation of our DNA, a viral infection is about having a foreign piece of DNA (or RNA) interfering with how our cells metabolize and what proteins they produce. From what I understand, one big piece of work is to ingest new data: besides papers on genetic diseases, papers focused on viral diseases need to be incorporated so the knowledge graph has a more complete and accurate representation of them.

In applying this system to COVID-19 some assumptions are up for revision, though. I suspect the importance of the proof accompanying recommendations for repurposing drugs plays a lesser role. If you’re dealing with a rare genetic disease, the economics are important. You’re working with a problem a few people have and you can’t afford to examine puzzling recommendations a computer-generated before convincing yourself and the doctor to try them. There’s hardly any study group you can rely on. COVID-19 is a top priority for the entire world and it’s safe to assume it will remain so until we find an effective vaccine. We can and absolutely should look at as many promising drug candidates even if the system that churns them out can’t explain itself. The big advantage of deep learning methods in the COVID-19 case is that they would most likely be much faster to iterate on - they require less manual heuristics and have the potential to deal with partial or noisy data more robustly. You might be trading explainability for speed and robustness of the system. One can imagine that people can then backtrack a particularly promising drug/molecule candidate. Given the human and economic cost of COVID-19, prioritizing speed above everything else is [worth](https://marginalrevolution.com/marginalrevolution/2020/03/the-speed-premium-in-an-exponentially-growing-pandemic-world.html) [doing](https://fastgrants.org).

## Closing

There’re three main take-aways I have on drug repurposing from Matt Might’s talk and reading I’ve done around it:

1. Relatively straightforward ideas from computer science can have a real impact on drug repurposing. You don’t need a PhD in molecular biology to work on it.
2. But to work in this field, you need to _team up_ with the domain experts: biologists and medical doctors. What you would bring to the table is not only computer science chops but also a different way of thinking compared to the baseline in the field.
3. Thanks to Matt Might group’s work we have solid technical underpinnings for software-aided drug repurposing for COVID-19.

## Further reading

If you’re interested in what’s being currently (as of early April) done in drug repurposing for COVID-19, I found these two articles worth reading:

1. The Atlantic has a very [approachable overview](https://www.theatlantic.com/science/archive/2020/04/what-coronavirus-drug-will-look-like/609661/) of drug repurposing for COVID-19
1. [An article in Nature](https://www.nature.com/articles/d41587-020-00005-z) going deep into vaccines development for the current pandemic but starts with drug repurposing and its relation to the computational tools
