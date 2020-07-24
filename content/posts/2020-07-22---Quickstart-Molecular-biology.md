---
title: Quickstart Molecular Biology
date: 2020-07-23T04:34:18.952Z
template: post
draft: false
slug: quickstart-molecular-biology
category: biology
tags:
 - biology
description: A crash course in molecular biology on 160 pages if you need one.
---

I've picked up [a book](https://www.amazon.com/gp/product/1621820343) on molecular biology that promises to be an introduction geared for STEM people. (aside: book price has skyrocketed since I bought it and later it went out of stock - my guess is it's due a surge in interest in molecular biology due to COVID-19).

I've been dabbling with data-oriented problems in cell biology with particular attentiveness to tasks that might be cracked or better solved with the recent advancements
in deep learning. I've been pretty oblivious to even basics of biology, though. My qualification in the field is at the middle school level. The trick I have been relying on
to fill in my knowledge gaps has been either grabbing lunches with biologists (pre-pandemic) or by side-stepping them altogether by sticking to problems with an easy formulation and a difficult technical solution. The data analysis in cytometry falls into that category.

Going back to the book - it's great. At 160 pages, it provides a concise crash course on terms (e.g., various kinds of RNA) of molecular biology and its techniques (e.g., now-famous PCR used for coronavirus detection). I won't go into summarizing the book because it's already dense. Instead, I'm sharing a few observations.

## Biologists love indirection and tagging

From DNA sequencing to cell classification, most of the observations done in molecular biology employ clever tricks and indirections. Modern DNA sequencing relies on attaching a complementary base pre-tagged with a pyrophosphate (a chemical compound). Once the base finds its complement in the DNA, the pyrophosphate is released. An enzyme coming from fireflies converts pyrophosphate into a light that is detected by a camera. Once the light is observed, the next complementary base is attached, and the cycle repeats. Noting the presence of a piece of DNA
involves a tag (pyrophosphate), and detection of a light signal (indirection) for binding of complementary bases.

A similar combo of tagging and indirection is typical in cytometry (cell analytics). For example, if you want to find out if cells of a particular kind are present in your sample, you do not look via microscope at all cells and somehow recognize the ones you look for. Instead, you find an antibody (tag) that binds to the cell kind you're looking for and attach to the antibody something observable - a chemical compound either reflecting laser light or emitting its own light. You then spray all cells with such tags, wash them out, and look for places the tags stuck. Plenty of indirection to spot a cell.

The use of indirection is common in RNA detection via micro assays and in protein detection.

This reminds me of a famous quote by David Wheeler:

> All problems in computer science can be solved by another level of indirection

It's dubbed as a fundamental theorem of software engineering. My version for molecular biology: in molecular biology, you observe with a tag and an indirection.

## What's your representation?

Throughout the book, I've developed the impression that molecular biology requires a large variety of representations for its data and knowledge. DNA and RNA are both sequences. Cellular structures are commonly captured via image data. Protein interactions form complicated graphs (or networks as biologists like to call them).

The central dogma of molecular biology says that information flows from DNA to RNA to proteins. The information flow is knotty, though. E.g., transcription factors that are proteins themselves regulate RNA's interpretation and its translation into other proteins. A good model for expressing knowledge in molecular biology requires different representations and a way of joining them.

The theme throughout the book that I noticed is the non-binary nature of most facts in molecular biology. The underlying reasons are either our inability to measure processes precisely, which introduces noise or inherent stochasticity of what we're looking at. Thus, traditional discrete graph knowledge graphs (as in old-school AI systems) seem to not an optimal fit for molecular biology.

This observation brings about the concept of dense representations central to deep learning. The idea is to represent information as vectors of numbers with numbers participating in the encoding of the data. The attractive property of dense representations is that they have a natural measure of similarity: it's just a distance in vector space. That gives a way of encoding and processing information that's non-binary. Deep learning's success in computer vision, sequence modeling
(for language), and, less famously, on graphs matches the molecular biology's shape of information. Neural networks offer a natural way of joining, e.g., vision and sequence data, which has been traditionally an uncrackable problem. That observation is not particularly novel, and
people are working on applying deep learning to biology. However, I wanted to write it down to show how even causal reading about biology brings to mind parallels between needs in biology and recent progress in computing.

## Foreign invaders

I'll close with two fun facts about biological invaders I learned from the book. The first is that mitochondria are the only organelle in the cell to carry their own DNA. It's explained by mitochondria being a residual of an ancient bacteria assault on primitive cells. Mitochondria are the energy-producing equipment of the cell and are core to life. I was surprised to learn that living as we know it might depend on a happy version of invasion.

Another invader is the virus, which is on everyone's mind in 2020, obviously. A virus is a foreign piece of RNA or DNA that hijacks the regular "software" of an invaded cell. I knew that part, but it was fun to learn how the invasion can work in the context of cell processes. If there's nothing else you want to learn from molecular biology, I recommend the first 2-3 chapters to help you understand all the terms required for reading about the science behind coronavirus. You can be part of the club.
