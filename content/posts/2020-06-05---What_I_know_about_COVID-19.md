---
title: What I know about COVID-19
date: "2020-06-06T00:01:00"
template: "post"
draft: false
slug: "what-i-know-about-covid-19"
category: "covid-19"
tags:
  - "covid-19"
description: "Like many people, I’ve been glued to the news over COVID-19. In many ways a perfect distraction: it’s an endless source of news, there’s a lot of inherent uncertainty and drama and it’s full of numbers."
socialImage: "/photo.jpg"
---

- [Exponential processes are really dramatic](#exponential-processes-are-really-dramatic)
- [“This is like flu”](#this-is-like-flu)
- [“Many people had it already”](#many-people-had-it-already)
- [Viral load](#viral-load)
- [Economy: “Ignore that pile of bodies in the corner”](#economy-ignore-that-pile-of-bodies-in-the-corner)
- ["There is such a thing as society”](#there-is-such-a-thing-as-society)
- [Twitter, used responsibly, is an excellent source of information](#twitter-used-responsibly-is-an-excellent-source-of-information)
- [Test, test, trace and isolate](#test-test-trace-and-isolate)
- [Predictions and final thoughts](#predictions-and-final-thoughts)

Like many people, I’ve been glued to the news over COVID-19. In many ways a perfect distraction: it’s an endless source of news, there’s a lot of inherent uncertainty and drama and it’s full of numbers. Back in February, I thought I’d research the topic a little bit, make up my mind about what’s going on, assess associated risks, and move on. In particular, I wanted to resist the urge to immerse myself in this subject. However, the reality is that COVID-19 is a bigger story than anything else, affecting everything about everyone’s life.

I've been keeping notes on links to resources I found particularly useful as the pandemic evolved and with it, our understanding of it. I've decided to turn them into a blog post you're reading.


## Exponential processes are really dramatic

In the early days of the outbreak, the epidemic follows an exponential process and it’s really dramatic. This is a trivial observation but still hard for me to have an intuitive feel of how this plays out in real life. You can be versed in basic mathematics underlying the spread of the disease and deal with data for living as I do and still under-appreciate how explosive the exponential growth is.
The exponential growth only works as an *early* approximation of viral spread. And we’re still early into this in most places. Even the worst-hit NYC has an estimate of 20% (wide uncertainty around this number) of people catching COVID-19 already. The rest of the world is definitely behind NYC so the exponential growth is a good approximation of what’s going on.

What fewer people realize is that exponential growth is very fragile. If you tweak the growth parameter a little bit, you get vastly different outcomes. For example, if you reduce the growth factor of the virus by 33% you have 3 times (300%) less infected people in 5 days. After 20 days, the comparison is more dramatic, you have 148x (14800%) less infected. In absolute numbers, after 20 days you have 22 thousand infected people vs only 148 if growth factor is one-third of the original. The exponential process is not only fragile in its growth but dies equally dramatically. Imagine if the entire world stayed at home so nobody is meeting and spreading the virus. After 3-4 weeks COVID-19 would go from above 2.5 million infected (at the time of writing this) to zero and simply disappear. The COVID-19 would dismiss itself as a global problem and we would return to the true normal we remember from 2019. Obviously, we can’t do that but if we could, this would be an example of a drastic exponential decline. It’s non-intuitive that the virus can grow and shrink so quickly but that’s the nature of exponential growth.

Bill Gates speculated in his, now-famous, talk that we were lucky with previous viruses. His talk is about tweaking the parameters of the virus so it’s more contiguous than previous examples and imaging what could happen. [The talk](https://www.ted.com/talks/bill_gates_the_next_outbreak_we_re_not_ready) is from 2015 and feels eerily prescient when watched in 2020.

It's been widely shared by this point but I wanted to include it for the idea of tweaking the vital parameters and seeing through consequences. It's not that Bill Gates was a prophet, the epidemic was predictable and not a surprise.

This video by Grant Sanderson explains visually the mechanics of the exponential growth: [https://www.youtube.com/watch?v=Kas0tIxDvrg](https://www.youtube.com/watch?v=Kas0tIxDvrg).
It’s the best resource I have seen explaining both why exponential growth is so dramatic, why is it inevitable in case of a viral disease. Go watch it, Grant Sanderson is a real American treasure.




## “This is like flu”

This virus has been systematically underestimated by the world. First, it was seen as a Chinese problem and an oddity. Back in January, Twitter was circulating videos of the Chinese government erecting hospitals in a matter of days. When the virus broke out firmly in Europe, it was still dismissed as not more dangerous than the seasonal flu. Very few at the time thought to themselves “wait, nobody is frantically assembling hospitals for flu”. This dismissal, that I understand, let the virus show its innate rate of transmission. We’ve learned painfully that the virus is far more contiguous than we thought. It infects more people than we thought and infects them faster than we thought.

As governments went for extreme lockdowns and emergency measures not seen since The Second World War we stopped underestimating the virus.

Unfortunately, that shift in perception about the coronavirus had to be painfully lived through again across the world. An E.R doctor from New York has kept her diary that has been [published in the New York Times](https://www.nytimes.com/2020/04/14/magazine/coronavirus-er-doctor-diary-new-york-city.html). It’s beautifully written and it’s the best personal account of COVID-19 I have read. It articulates the disbelief about what's been happening in Italy can happen in the US. If you can, check out the audio recording linked at top of the article.

Could it be that we swung too far and we overestimate the danger of the virus? Some people argue exactly that but I disagree. None of the data published so far suggests that estimates of how quickly the virus can spread when left alone and how lethal it is weren’t that much off. As we sit at homes, it might feel like the whole thing was overblown because we don’t see the pictures of military trucks taking bodies out of hospitals as we saw in March in Italy. That’s because we sit on our butts. We also understand the disease a little bit more so fewer mistakes like infecting people through medical workers are done compared to two months ago when we were shooting in the dark.

## "Many people had it already"

The other popular argument that started gaining traction is that many more people have been infected than we know about. This was fueled by the discovery of significant number asymptomatic carriers - people infected and infecting other people but feeling fine.

Asymptomatic carriers are a big deal for two reasons:
  1. They are spreading the disease unknowingly making it much harder to contain
  2. We might be underestimating the number of people who unknowingly had COVID-19 already which has implications on how we should think of the risk of catching it. One might think: maybe I had it already too and I can skip precautions?

The latter argument is the one I have heard within my social circles. It was spurred by early serological studies like, a widely-shared Stanford study. When I saw the surosurvey-based claim of 50x-80x more cases within Santa Clara county's population than the official case numbers indicated, my eyebrows raised. We all know that case numbers undercount real infections but most estimates where at 4-10x undercounting.

Balaji S. Srinivasan, who as early as in January correctly appreciated the danger of COVID-19 (at the time he sounded alarmist to most people), was quick to [dismantle](https://medium.com/@balajis/peer-review-of-covid-19-antibody-seroprevalence-in-santa-clara-county-california-1f6382258c25) the study and point out severe data collection and analysis weaknesses. In short, that study was of dubious quality.

Later on, France and Spain carried out serological tests of larger (and representative) samples of their populations and [found around 5%](https://twitter.com/hsalje/status/1260606369805320195) had COVID-19 already.

The key issue with anti-body tests available as of June is their false positive rate. The test might indicate a positive result for someone who never had the virus. Now, the interesting bit is that the lower prevalence of the virus within the population, the worse serological tests are in their performance. In the extreme case of very low number of people who had COVID-19 you might end up with more false positives than true positives. All you'll learn from such study is noise.

I developed a rule of thumb to be skeptical of any population anti-body tests of below than 20 thousand people. You _might_ go lower than that but then check with authors of the study how they carefully manage the complexity around the false positive rate and the sampling strategy. If they don't acknowledge this to be a very hard problem, the whole study needs to find its way to trash.


## Viral load

We tend to talk about infections in binary form: you either caught the virus or you’re healthy. What if the “poison” can have a dosage? And what if you’re exposed to a lot of the virus, your disease will be much worse? Pre-COVID-19, my understanding of viruses was at “there are biological viruses and there are computer viruses”-level so I didn’t know whether viral load made sense.

I found [this NYT article](https://www.nytimes.com/2020/04/01/opinion/coronavirus-viral-dose.html) interesting with quotes I want to highlight:

> The importance of viral dose is being overlooked in discussions of the coronavirus. As with any other poison, viruses are usually more dangerous in larger amounts. Small initial exposures tend to lead to mild or asymptomatic infections, while larger doses can be lethal.
>
> [...]
>
> It would be unethical to experimentally manipulate viral dose in humans for a pathogen as serious as the coronavirus, but there is evidence that dose also matters for the human coronavirus. During the 2003 SARS coronavirus outbreak in Hong Kong, for instance, one patient infected many others living in the same complex of apartment buildings, resulting in 19 dead. The spread of infection is thought to have been caused by airborne viral particles that were blown throughout the complex from the initial patient’s apartment unit. As a result of greater viral exposure, neighbors who lived in the same building were not only more frequently infected but also more likely to die. By contrast, more distant neighbors, even when infected, suffered less.

I haven’t seen much discussion of this important concept. I wonder if viral load for COVID-19 is a thing and then if we let the virus grow to a large number of cases, people not only have a higher chance to be infected but also receive a higher dose of the virus and have a more severe disease? You would have this double stacking of threat: a high infection chance and an elevated chance of a really bad infection. I don’t know if that’s true and I haven’t seen resources or researcher pointing in either way. If we assumed that viral load was a thing then taking a twelve-hour flight might not be an appealing prospect to anyone until the vaccine is found.

It’s blatantly clear that tourism will be hit by the current crisis. If the viral load is a thing, remote, exotic tourist destinations are toast. I’d love to learn more about it.

## Economy: “Ignore that pile of bodies in the corner”

At the time of really rapid growth, we didn’t know much about the virus. Waiting for more information to arrive means letting exponential growth run its dramatic course. Given the vast potential cost, we had to act immediately. That sent shockwaves through economies, led to unemployment and suffering. Naturally, people start to scratch their heads whether such cost was proportionate and whether we should open up right away.

> Hey, keep going to restaurants, go buy new houses, ignore that pile of bodies over in the corner. We want you to keep spending because there’s maybe a politician who thinks [gross domestic product] GDP growth is what really counts. - Bill Gates

Gates rightfully ridiculed the notion that, if the virus is rampant in its spread, you can have a working economy. We have an economic crisis because we have a public health crisis. When people are afraid to go out or travel, you don’t have a working economy no matter what the government decides. 

All public debate should be not whether the choice is whether we continue lockdowns or have a resemble of a working economy. That’s a false dichotomy. We locked down because the viral spread was uncontrolled. We got it under control (except perhaps the US amongst developed countries) but the virus didn’t disappear. We merely hit a reset button. The real debate should be about what we do with the time the lockdowns are buying us and how we reopen.

The painful reality is that nobody knows how to strike the balance between keeping the virus at bay and a working economy. I found this [Science Magazine](https://www.sciencemag.org/news/2020/04/ending-coronavirus-lockdowns-will-be-dangerous-process-trial-and-error) article to be a pretty interesting of choices and dilemmas involved:

> Most researchers agree that reopening society will be a long haul, marked by trial and error. “It’s going to have to be something that we’re going to have to take baby steps with,” says Megan Coffee, an infectious disease researcher at New York University.
>
> [...]
>
> Choosing a prudent path is difficult, Buckee says, in part because no controlled experiments have compared the effectiveness of different social distancing measures. “Because we don’t have really strong evidence,” she says, “it’s quite hard to make evidence-based policy decisions about how to go back.” But Lipsitch says that as authorities around the world choose different paths forward, comparisons could be revealing. “I think there’s going to be a lot of experimentation, not on purpose, but because of politics and local situations,” he says. “Hopefully the world will learn from that.”

Where I am sitting today (Poland), people accept the lifting of restrictions with the expectation that this is the end of the story. The public accepts the "trial" and turns deaf on the "error" part. That's a failure of political leadership but I suspect it's not confined to just one country. It's a universal challenge on how to communicate with people about policies with wide uncertainty.

## “There is such a thing as society”

Boris Johnson, who famously caught COVID-19, declared there’s such a thing as a society while bunkering in self-isolation. Viral diseases are social problems and so are our responses to them. Nurses and doctors caring for sick people are a display of the best of society at work.

Getting the infection from another person is also a reminder that we live in societies.

I want to borrow that quote for another purpose, though. There's a wide-spread confusion about the personal and societal angle to discussions around the coronavirus. Using masks serves as the prime example. Early on, masks were dismissed as ineffective personal protection against respiratory disease. WHO and many health experts actively discouraged people from wearing them to the point of ridiculing them. I observed this both in Europe and in the US. But Asian nations insisted on their use. Was that just an unscientific superstition? No, WHO and doctors were right narrowly and wrong broadly.

Simple masks do not guarantee adequate protection against infection for someone at risk of high exposure like in a hospital setting. That's the vantage point WHO and many experts held. However, simple masks seem to be effective at preventing an infected person from spreading it to others. The asymmetry is an interesting phenomenon: the same mask prevents "exhalation" of the virus to the surrounding people but is much less effective at preventing "inhalation" of the virus once it's already in the environment. That is counter-intuitive but that's what the evidence suggests.

Jeremy Howard has been particularly vocal about mask-wearing, advocating it early on, and actively arguing with health authorities like WHO or American CDC. One of his earlier posts based on the combination of research paper reviews _and_ common sense [ends with](https://www.fast.ai/2020/04/13/masks-summary/):

> Whilst not every piece of scientific evidence supports mask-wearing, most of it points in the same direction. Our assessment of this evidence leads us to a clear conclusion: keep your droplets to yourself – wear a mask.

The canonical source of All Things Masks is a follow-up post, [Masks - FAQ for Skeptics](https://www.fast.ai/2020/04/20/skeptics-masks/). It contains probably more information than you need. The takeaway here is that you wearing a mask is a service to the society, to the people around you. Your protection depends not on your mask, but on mask-wearing of others. It's a great example of a social problem and my prediction is that public buy-in for mask-wearing will depend on really old-school tools: good education and transparency.

Mask wearing might be the single most effective and cheapest tool for reducing the spread and avoiding potential periodic lockdowns.


## Twitter, used responsibly, is an excellent source of information

Back in February, I noticed that the issues discussed like mandatory mask-wearing were discussed a week or two ahead of mainstream media in Poland where I currently reside. Some issues that I felt were important never percolated to mainstream media.

The people I found offering really insightful commentary on the research and the news:

- [https://twitter.com/CT_Bergstrom](https://twitter.com/CT_Bergstrom) - (US) virology
- [https://twitter.com/trvrb](https://twitter.com/trvrb) - (US) virology and epidemiology
- [https://twitter.com/zeynep](https://twitter.com/zeynep) - (US) writer, policy, research (including epidemiology), combination of excellent writing grounded in solid data analysis
- [https://twitter.com/jburnmurdoch](https://twitter.com/jburnmurdoch) - (UK) data, stats and beautiful charts around COVID-19
- [https://twitter.com/AdamJKucharski](https://twitter.com/AdamJKucharski) - (UK) epidemiology
https://twitter.com/jeremyphoward - (US) data science, one of the primary leaders #masks4all campaign; previously focused down-to-earth deep learning, temporarily shifted to down-to-earth public health

I'm also mantaining a [COVID-19 Twitter list](https://twitter.com/i/lists/1242085677434638336) of people I like to follow on science and policy takes related to COVID-19. All people mentioned above are part of that list, of course.


## Test, test, trace and isolate

One of the most promising exit strategies from lockdowns is reducing the R - effect reproduction number to the level where the virus is no longer growing as rapidly. As mentioned at the beginning, the exponential growth is really fragile so driving down its key parameter will put to return to a life that's close to normal. An important element of that strategy is quickly identifying infected and potentially infected people and isolating them before they have a chance to infect more people.

Grant Sanderson, again, is excellent at explaining how this can be done without turning our countries into Big Brother states: [https://www.youtube.com/watch?v=D__UaR5MQao&t=327s](https://www.youtube.com/watch?v=D__UaR5MQao&t=327s)

Why is isolating so important? Grant covered this topic in an earlier video on simulating epidemic scenarios: [https://www.youtube.com/watch?v=gxAaO2rsdIs](https://www.youtube.com/watch?v=gxAaO2rsdIs)

The real world is more complicated than computer simulations but the basic laws of how the virus spreads and what is effective at stopping it are well captured by simulation like Grant's.

## Predictions and final thoughts

COVID-19 is the biggest story of 2020 and will shape most events and policies of this year, either directly as a public health crises or indirectly as a fallout of the economic crisis.

Exponential growth, which still (in June) approximates the development of the epidemic, is both dramatic and fragile. If left alone, it will exploit the virus's innate transmission rate and explode as it did in Northern Italy or NYC. Controlling its spread is difficult. A combination of universal mask-wearing and testing, tracing and isolating seems to be the most promising path forward. Western societies will struggle with both mask-wearing and contact tracing. They require deep changes to how we live and the more we succeed in implementing the more they will feel unnecessary.

My baseline prediction is, unfortunately, we're in for cycling through the pain of uncontrolled spread which will convince people the threat is real, to suppressing the virus with great effort, getting people exhausted, and bouncing back to an uncontrolled spread. Having said that, I don't expect reoccurring nation-wide lockdowns. National epidemic is always a collection of more local outbreaks and I expect local partial lockdowns to be reintroduced across Europe.

The more optimistic route is that people's increased awareness, hygiene, and altered habits will be enough to reduce the growth rate of the virus to the level where it's controllable or even shrinking. Switzerland might the only example where this appears to be happening.

A lot of discussions have been focused on the economic cost of the health crisis and lockdowns that many governments introduced. I'm more worried about second-order consequences. This virus will get politicized and the urge to do so will be the stronger the less capable given government is at managing the crisis. I think the next few months will surprise us with social unrests, not necessarily directly linked to the disease. I'm also deeply worried about the misinformation pandemic that we're likely to experience, with its own local outbreaks.

I'm trying to work out the shape of my productivity for the rest of the year. One thing clear to me - long, intercontinental trips can't be part of the formula for the rest of the year. The rest will be determined by the high volatility of life and I think I will have to just roll with it.
