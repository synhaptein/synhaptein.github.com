---
layout: post
title: Best Technical Talks Week 16
categories: [talks]
tags: [rust,category theory,functional programming,deep learning,formal verification]
description:
---

For week 16, my selection includes 5 talks about rust, category theory, deep learning and formal verification and analysis of software.

### Category Theory for the Working Hacker

Philip Walder offers us a great introduction to category theory using simple code samples to illustrate the basics of the modeling of products and sums, then he explores the more complex concept of modeling functions (lambda calculus). I suggest you watch it till the end, there's a surprising ending!

Philip Wadler at Lambda World 2016 [(Watch)](https://www.youtube.com/watch?v=V10hzjgoklA){:target="_blank"}

### Why you can't afford to ignore deep learning

Jeremy Howard offers us a short intro to deep learning and then lightly explore the bleeding edge of the field (2016) regarding image generation, speech recognition, etc. He then makes a very interesting observation by pointing out that a lot of the best models in the last couple of years have been created by people that were not domain expert and that augmenting our domain experts with those models would probably get us better results in certain fields.

Jeremy Howard at Scala By The Bay 2016 [(Watch)](https://www.youtube.com/watch?v=sMBce-0psyY){:target="_blank"}

### Functional programming guerilla in the land of Rust

Tomasz Barański offers us a good introduction to rust abilities to program in a function style using type inference, immutable data, traits (as type class), enums (as algebraic types) and pattern matching. The talk ends on a short intro of rust's macro and performance implication.

Tomasz Barański at Lambda Days 2017 [(Watch)](https://www.youtube.com/watch?v=y9ONOUm62_A){:target="_blank"}

### Let’s Get Lazy — The Real Power of Functional Programming 

Venkat Subramaniam offers us a pretty clear and simple explanation of why laziness is an important concept of functional programming and why he thinks it is probably the most important feature of FP using Java, C#, Scala and Haskell. He explains what is the difference between application order and normal order, eager vs lazy evaluations and why purity of function become very important when dealing with laziness. 

Venkat Subramaniam at NDC London 2017 [(Watch)](https://vimeo.com/213571882){:target="_blank"}

### Move Fast to Fix More Things

Peter O'Hearn offers us the story of Monoidics being acquired by Facebook and how a group of academics with a tool to do analysis of 10kLOC programs created a more advance solution to analysis programs with >1MLOC. He explains how they had to change their mindset from "Move Slow And Break Almost Nothing" to "Move Fast And Break Things" to fit the culture of the company. By making the process of program verification faster and worrying less about false positive, they were able to fit more closely the culture of the company and have a bigger impact. Very interesting how a simple change (process-wise) from nightly bug reports to a solution that piggyback an existing process (code reviews) change drastically the impact they now have.

Peter O'Hearn at CurryOn 2016 [(Watch)](https://www.youtube.com/watch?v=xc72SYVU2QY){:target="_blank"}