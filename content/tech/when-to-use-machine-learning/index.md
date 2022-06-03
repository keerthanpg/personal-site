---
title: "When to use machine/deep learning to solve a problem?"
date: 2019-05-25T17:37:56-07:00
draft: false

Categories: ["Technology"]
---
Originally posted [here](https://medium.com/%E0%B4%95%E0%B5%81%E0%B4%B1%E0%B4%BF%E0%B4%AA%E0%B5%8D%E0%B4%AA%E0%B5%81%E0%B4%95%E0%B5%BE/when-to-use-machine-deep-learning-to-solve-a-problem-66a46abeb53e?source=---------0-----------------------)

Sometimes it can save a lot of time to stop and think if ML/DL is indeed the right approach to solve your problem rather than realising that after throwing a ton of data at a network without getting anywhere and potentially being outperformed by a simple classical algorithm. Here’s where ML shines:

1.  When the inputs are noisy
2.  When the solution cannot be described in human defined rules
3.  When the problem cannot be entirely defined and your solution needs to scale for diverse scenarios and edge cases
4.  When you can generate large amounts of data that is representative of your problem space
5.  When safety considerations allow redundancy for multiple methods to concur

Otherwise, don’t. Stick with classical approaches as they may be better suited if you’re worried about the best solution. ML is only cool when used appropriately. ☺

- I’d mention black box nature/ opacity and vulnerability to adversarial attacks but I’m positive that’ll change with more DL research and are a current limitation but not fundamental flaws of the method.
