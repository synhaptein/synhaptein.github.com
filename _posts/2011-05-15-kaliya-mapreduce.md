---
layout: post
title: Kaliya now based on mapreduce
categories: [kaliya]
tags: []
description:
---

After being a "proof-of-concept" of a hardcode md5 cracking demo, kaliya is now
a distributed javascript mapreduce engine! You only have to provide an iterator,
a job name who refere to a javascript file that contains the map and the reduce
function. It does not support fancy things like worker fail recovery or balancing
job on faster nodes, but it can do reverse indexing. More improvement will be
done soon. I put at least 10 things on my todo list related to kaliya! It's a
nice toy!
