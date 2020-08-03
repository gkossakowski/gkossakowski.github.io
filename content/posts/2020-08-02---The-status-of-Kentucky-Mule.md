---
title: The status of Kentucky Mule (faster Scala compiler)
date: 2020-08-03T05:57:11.651Z
template: post
draft: false
slug: status-kentucky-mule-faster-scala-compiler
category: compilers
tags:
  - compilers
  - scala
  - performance
description: 'Occasionally, someone on the internet comes across Kentucky Mule and I receive an email asking its status.'
---

Occasionally, someone on the internet comes across Kentucky Mule and I receive an email asking about its status. I thought I would write about it publicly.

The summary is Kentucky Mule served its purpose as a research vehicle and reached an inflection point where the next logical step would be to turn research
ideas into practice. That step never happened.

I started working on Kentucky Mule out of frustration and ambition. I was deeply frustrated by Scala's compilation speed and saw it as the top problem hindering
the adoption of the language. Slow compilation speed is a high tax on a programmer and chips away at the joy of programming. I worked on various
performance-related projects for the Scala compiler before, and I knew it's a hard problem. Solving it would be the most ambitious engineering task I have ever worked on.

I thought of Kentucky Mule as both a free-spirited exploration of less treaded ideas in compiler construction and a platform for a quantitative assessment of the performance gap between today's reality and what's possible. As a project, Kentucky Mule was as much about writing prototype code as coming up with smart experiments. For example, fairly early
on, I came up with the idea of benchmarking the compilation speed of Scala and Java code side-by-side. Scala code was of "Java in Scala syntax" flavor to make the comparison
apples-to-apples. I.e. no advanced Scala features were in use. It turned out that the Scala compiler is around 7x slower than Java compiler at compiling an equivalent code. That convinced me the opportunity for the improvement was very large.

The other aspect was the search for better compiler architecture. I was particularly intrigued by the idea of using task queues for tackling the fundamental
problem of scheduling compiler operations in the right order. I've written about this problem [here](https://medium.com/@gkossakowski/kentucky-mule-limits-of-scala-typechecking-speed-6a44bd520a2f) and [here](https://medium.com/@gkossakowski/on-kentucky-mule-a-transcript-d11ab2920c95). I genuinely believe that task queues are a better foundation for compiler construction. Later on, [Dmitry Petrashko](https://twitter.com/darkdimius) pointed out that the idea of using task queues has a history in various research projects. The trick is how to convince practitioners to switch to these ideas? None of the mainstream compilers I'm familiar with use task queues.

There's no other practical way than just go and build it and show its worth. I estimated that taking ideas and insights from Kentucky Mule and proving them in a setting of a real compiler would require 2-3 full time, top-notch engineers working for at least 6 months. I wrote a hypothetical [project brief](https://medium.com/@gkossakowski/from-kentucky-mule-to-faster-scala-compiler-project-brief-d878495cad3b) with detailed milestones. And then life hit me with a brick, and I had to focus on my health, immediately. I switched from playing offense to playing defense. At the same time, I decided to take a break from systems programming and jump on the deep learning bandwagon as an ML practitioner. And that was it. The project got shelved. To this day, I like to think of the work and insight that went into Kentucky Mule to be one of the best
pieces of work I have ever done. It's the project I'm most proud of that never shipped.

If you're reading this and find the idea of vastly improving the state-of-the-art in compiler construction with the focus on performance intriguing, feel free to contact me. I still like chatting about it.
