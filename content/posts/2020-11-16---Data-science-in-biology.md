---
title: Data science in biology
date: 2020-11-16T19:47:24.630Z
template: post
draft: false
slug: data-science-biology
category: biology
tags:
  - biology
  - datascience
description: As a study of life's fundamentals, microscale biology is going through a paradigm shift. Data science is at the center of it.
---

An adage says you'll use the vocabulary from other areas you already know to
describe what you're learning whenever you approach a new field. I've been
experiencing this viscerally while diving into methods people use in microscale
biology (at the molecular and cellular level) with an eye for improvements in
the field's productivity via better software[0]. As an outsider, the first thing
you'll notice is biologists' overall excitement with high throughput methods.
The idea is to use automation to go from 1 to N experiments simultaneously and
exploit the massive parallelization as a new way of studying life. The prominent
feature of that approach is using computing and statistics for making sense of
enormous data produced by automated experiments.

High throughput methods are one of the pillars of biology subfield called
systems biology that I just learned about from System Biology by Eberhard Voit.
From A Very Short Introduction series, the book is great at giving a crash
course on the subject.

My impression from learning about systems biology is that its existence is both
an admission of the Microscale Biology Complexity Behemoth and a scheme of how
to slay it. Your primary weapon is a firehose of data.

After the book

> It has turned the tried-and-true scientific method on its head. The central
> position of a strong hypothesis has vanished, and the new mindset is
> _exploratory data analysis_, which here translated into the lax mandate:
> "let's see what's out there, and then we'll try to figure out what it means."

To anyone working in the tech industry, this must sound familiar to "let's
collect lots of data and later figure out what it all means."

A cool recent example of mapping biology this way is from the [COVID19
study](https://twitter.com/EricTopol/status/1320105387064918016). At a high
level, the idea is to grow thousands of lung cells' variants, each with
CRISPR-modified DNA, and infect them with coronavirus and leave for a while so
the disease can develop. Then you go over all cells' appearance and work out
whether a DNA modification influenced the disease's course. Once you identify
promising DNA hits, you can drill in more and leverage existing, extensive
biology maps (e.g. of gene-protein relationships). Put all together, you can quickly identify key factors in COVID19 development. An important thing to
remember is that life is messy, so the best you can hope to observe shotgun-like experiments are noisy
clues rather than hard facts, and that's where data science kicks in. It's a
method of fishing for significance out of a sea of raw data. Here's how Voit
describes it from a pure *science* perspective:

> Of greatest importance is that the research process no longer begins with a
> specific hypothesis, but rather with the automated extraction of relatively
> small amounts of significant information from huge datasets.

Why is data science and not statistics? Some argue that data science is just a
pop-culture term for statistics. I disagree. I define data science as a triple:
statistics, programming, and an intimate possession of domain-specific knowledge
working in concert. The widespread use of programming is a significant and relatively new phenomenon in biology[1].

Naturally, I wondered whether I'm hallucinating thinking an entire field of
microscale biology is adding programming to its core toolbox, at equal footing
with a microscope. I asked around a bunch of biologists, and all shared the same
sentiment:

> Nowadays, you can't get a PhD in biology without doing some serious R or
> Python.

I didn't expect it! I want to learn more and write what I find. In the meantime,
I recommend Voit's
[book](https://www.amazon.com/Systems-Biology-Short-Introduction-Introductions/dp/0198828373/).
It's a short, content-packed book that circles data science throughout its
course.

PS. Surprisingly, there isn't something like GitHub for biologists.

[0] Contrary to most working in this area, I have a hunch that R&D in microscale
biology rather than medical diagnosis is the good _first_ bet for applying deep
learning to life sciences.

[1] I would argue that bioinformatics should be called genomeinformatics - it's constrained to one application area
