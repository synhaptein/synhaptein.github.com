---
layout: post
title: Best Technical Talks Week 17
categories: [talks]
tags: [git,cpu caching,idris,total functions,microservices]
description:
---

For week 17, I'm a bit late on my schedule, but I still manage to get a selection of 4 talks about CPU caching optimization, git, total functions and microservices architecture.

### Type-driven Development of Communicating Systems in Idris

Edwin Brady offers us a presentation about total functions, why they are important and the kind of benefits you get from writing them. Probably the most interesting part to me is when he explains how to "describe looping programs as a stream of IO actions" in order to be able to use total functions.

Edwin Brady at Lambda World Cadiz 2016 [(Watch)](https://www.youtube.com/watch?v=IQO9N0Y8tcM){:target="_blank"}

### Building systems that are #neverdone

James Lewis offers us a pretty interesting view of microservices architecture (w/o the BS) and how the tools and practices we used to relied on (TDD, YAGNI, KISS, GRASP, DRY, etc) are still valid with this new architecture, but sometimes in a slightly different way.

James Lewis at DEVOX Poland 2015 [(Watch)](https://www.youtube.com/watch?v=R_tWgcPYgRs){:target="_blank"}

### Caching in - understand, measure, and use your CPU Cache more effectively

Richard Warburton offers us a very understandable explanation of how the CPU caches work on Intel Hardware, how to measure the caching behavior and how to tune java program performance with optimization related to CPU caching. For some of you it may be a good reminder, but for others it will be a pretty good introduction to the impact of bad unaligned memory access. 

Richard Warburton at DEVOX UK 2013 [(Watch)](https://www.youtube.com/watch?v=7QD9fQRQ_l0){:target="_blank"}

### Linus Torvalds on Git

Linus Torvalds gives pretty harsh treatment to centralized source control like CVS, SVN and perforce, then explains why he created git and why a decentralized VCS is the way to go. I was told it was a classic presentation and was not disappointed! 

Linus Torvalds at Google Tech Talk 2007 [(Watch)](https://www.youtube.com/watch?v=4XpnKHJAok8){:target="_blank"}