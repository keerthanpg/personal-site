---
title: "Embodiment is Indispensable for AGI"
description: ""
images: ["/tech/embodiment-agi/bot_reading.jpeg"]
date: 2022-06-07T00:00:01-00:00
draft: false

Categories: ["Random"]
---

There are many paths on the road to AGI. Nando de Freitas recently wrote that “Scale is all you need” following the release of Deepmind’s Gato paper. Larger and larger transformers, with language interfaces doing supervised learning on large datasets is one such touted path. While Gato trains and evaluates on data from physical robots, there is a larger paradigm on getting to AGI that fully bypasses embodiment or robotics. This is the path pursued by OpenAI/Anthropic, who once famously [disbanded their robotics team](https://www.therobotreport.com/openai-abandons-robotics-research/). I recently found myself in a car ride with a friend who was a “member of technical staff” at OpenAI and he asked “Do you think solving embodied AI is required for AGI or is it enough to be digital?” I have thought a lot about that question since.


**Language as the end-all of intelligence**\
When it comes to conversations around AGI, language is often the start and end all of intelligence. From an evolutionary perspective, however, intelligence has not arised/existed outside of embodied agents and language itself evolved as a tool for multiagent communication. Language and structured coordination of agents helps with reward maximization in an environment, and could pose as an evolutionary byproduct of intelligence in line with the [Reward is Enough](https://www.sciencedirect.com/science/article/pii/S0004370221000862) hypothesis. Language certainly does encode a huge wealth of human knowledge and is a promising and defacto hammer to solve intelligence. But is it enough for AGI?


**What is AGI?**\
It all comes to answering the question of what constitutes an AGI. [Andrej Karpathy says it is a feeling](https://twitter.com/karpathy/status/1532894698439774208?ref_src=twsrc%5Etfw). Several Anthropic researchers define it, weirdly so, as ‘that which would make the world a weird place’. [Nick Bostrom](https://nickbostrom.com/superintelligence) defines AGI as “an intellect that is much smarter than the best human brains in practically every field”. [Wikipedia](https://en.wikipedia.org/wiki/Artificial_general_intelligence) defines it as “the ability of an intelligent agent to understand or learn any intellectual task that a human being can.” [Open Philanthrophy](https://docs.google.com/document/d/1IJ6Sr-gPeXdSJugFulwIpvavc0atjHGM82QjIfUSBGQ/edit?fbclid=IwAR3W3XVgKok3caD2TY6zSxqFr2CFSmqpOKX-gObOjup-o5nSJEdWEx2fy3o#) describes “transformative AI” with an economic definition as that which would 10x the Gross World Product by bringing about as much difference as agriculture or the industrial revolution. There’s also the idea, embraced in OpenAI circles, that if you can hire a remote worker and they’re as good as a human, that is AGI. If an AI can work like a physicist or researcher and make scientific breakthroughs and write papers without ever moving a literal finger, is that AGI? Steve Wozniak proposed a coffee test for AGI: a machine figures how to make coffee in an unseen human kitchen.

Ultimately, answering the question of whether embodiment is required for AGI depends on what definition of AGI you adopt. For this essay, I’ll pick _that which is as good or better than a human in every aspect_ as a baseline. There are several useful things to do in the physical world and transforming those would require embodied AI. 


![alt_text](./bot_reading.jpeg "image_tooltip")
"Vintage robot gives book reading in 1950s beat cafe." 
Generated by DALLE and prompted by [@Merzmensch](https://twitter.com/Merzmensch)


In relation to embodiment, there are broadly three paradigms to get to AGI:
1. Have an AI trained on vision and language and that which exists only on the internet. 
2. An AI trained on vision and language tasks but can do embodied tasks
3. An AI trained on vision, language and control, is embodied and is quite intelligent and physically capable as a human.


**Visual language AI that is completely digital is not AGI**\
In 1996, Deep Blue won against Garry Kasporov, becoming the most competitive chess player in the world. At that time, excelling at chess was considered the pinnacle of human intelligence. Today, AI is better at several video games, language and image generation tasks. But asking if solving non-embodied AI is enough for AGI is akin to asking if an AI that can only play chess and Go is AGI. Specialized AI is already better than humans at certain tasks but that is not general enough. It can obviously do wonderful things, such as automate several software engineering jobs, run a scientific lab, publish papers and invent breakthrough technologies, and write magnificent prose and poetry. Even if software engineer jobs are automated, ex-software engineers still use food, clothes,  laptops and have their stuff delivered. This AI would not sufficiently serve several industries such as - manufacturing, construction, driving, logistics, energy and mining, agriculture -  basically almost every industry that predates the internet. This is not AGI.

Similarly, going by the definition I adopted, 3 unambigiously is AGI. Let’s talk about 2. 


**What is the strongman version of an AGI paradigm that removes embodiment?**\
It is the hypothesis that one could train a really intelligent AI that does not collect data from robots but is trained on visual and language datasets and can zero-shot approximate the actuator parameters of any robot and operate it at least as well as a human teleoperating the robot if not comparable to an expert policy trained on the robot.


**If an AI can manage chefs, but a human chef does the physical act of cooking, is that AGI?**\
One needs embodiment to do embodied tasks, that is a tautology. However, can a non-embodied AI guide the actuators of an embodied worker? If every chef in the world is equipped with a superintelligent AI that takes visual language input and could tell them what to do in classic Ratatouille fashion, is it AGI? Thinking further in this framework, an AI would never reach its full economic value and be transformative on account of an inability to 10x physical productivity without embodiment. AI here would be bottlenecked on a purely mechanical axis. Additionally, an AGI involving the human embodiment in its closed feedback loop is still embodied AI?

For this proposition to even work, that is for a non-embodied AGI to guide a robot, there are a few caveats:


1. **Data from embodied agents:** It needs to be trained on data from embodied agents, their sensors as input and their actuators as outputs. This is a little like offline learning where you expose a network to tons of Youtube videos which have humans or other agents demonstrating how to do tasks, that the model then maps to a morphologically similar sensor/actuator configuration. If an AGI is predisposed to depend on data collected by embodied agents, would that make it an embodied AI? In my opinion, I’d say if the agent is human, no. But if it needs data from learned or teleoperated robots, then yes. This is a purely subjective line that I’m drawing. [Deepmind’s Gato](https://arxiv.org/pdf/2205.06175.pdf) by that subjective definition is embodied because it attempts to do robotics using supervised learning demos from real robots and simulated agents, and evaluates on real robots.
2. **Mapping morphology:** A second consideration is the effectiveness of an AI that learns from human demonstrations but executes on a robot and how good it can get at generalizing for morphology from a cross-embodied agent demonstration. [This paper](https://arxiv.org/pdf/2106.03911.pdf) gives some baselines on where we are at now, formulated in an RL, rather than supervised learning setting. Another close example is [quadruped robots learning](https://arxiv.org/pdf/2004.00784.pdf) to walk from dogs, who have very similar morphology.
3. **Offline learning:** A third aspect is the effectiveness of AI that only learns from policies executed by other agents. Such as AI would still be unable to model counterfactuals and learn self correcting behavior. For example, when you learn to surf, your awareness of your own agility and inabilities factor into your decision making, in addition to your learning experiences conditioned on your physical parameters. While [flamingo](https://www.deepmind.com/blog/tackling-multiple-tasks-with-a-single-visual-language-model) attempts to few-shot a few visual learning tasks, this is not done for control yet.
4. **Sim2Real:** Domain adaptation using simulated agents is one way to add embodiment without adding the physical aspect of it. However, sim2real is still an an active area of robotics research because agents exposed to only simulations cannot, yet, [transfer very well](https://arxiv.org/pdf/2006.09001.pdf) to the real world. 


**Robotics is an AGI problem, but more importantly, AGI is a robotics problem**\
AI research that primarily focuses on language ignores several problems that require intelligence, especially ones that concern 3D spatial imagery and decision making under partial observability. For example, simultaneous mapping and localization, that you’d need to explore a new city, a maze in a video game or even to drive require skills that are beyond the realm of language based formulation. Predicting the movement of dynamic agents while walking on the streets or the mechanisms of control that you’d need to learn to surf on a chaotic ocean require an understanding of structure from motion, of full body coordination, which again, is not a problem you’ll encounter or learn to solve by using language. 

Even after you add vision to language, there are still aspects of precise control and how it relates to intrinsic variables of embodiment that remain left-out. _Solving robotics requires solving vision ( sensory perception, 3d reasoning), speech ( instruction and contextual reasoning) and control ( manipulation and navigation)._


**Agent/Environment cannot be abstracted away from Intelligence**\
Lifetime learning over several episodes has encoded data in our genes, so much that a baby understands structured motion and the physics of the world around her before she understands and comprehends language. What is intelligent is deeply tied to what gives a survival advantage in an environment. For example, aquatic animals have [visual systems that are much better](https://www.wildlifeonline.me.uk/questions/answer/how-can-marine-mammals-see-underwater-but-we-cant#:~:text=Human%20eyes%20have%20evolved%20to,eyes%20with%20the%20aid%20of) at seeing underwater because they’re evolved to accommodate for the refraction by water in a way that humans are not. Our sensors that attempt to emulate our visual range, and the data we’ve collected on that basis, including YouTube videos, suffers from being overfit to our domain of visual capability. In [patients who have had their cataracts removed](https://www.science.org/content/article/feature-giving-blind-people-sight-illuminates-brain-s-secrets?cookieSet=1) allowing them to see for the first time, it was seen that despite spending an entire life in a 3d world, they lacked understanding of spatial imagery because their sensors didn’t have that input. In essence, environment and agent cannot be subtracted from the definition of intelligence. 

The last decade of AI research has led to the rise of large transformers that are very good at multi-task speech and vision benchmarks. A language first AI would be susceptible to the [failure modes](https://arxiv.org/pdf/2109.05014.pdf) of a blind agent, beyond the visual context it receives from a training corpus gathered from humans who can see. It logically extends that a visual language model would suffer from an inability to approximate actuator params inherent to performing precise control of an embodied agent. Reasoning about the real world require not just thinking about methodological spaces and language, but to be [grounded in real world context](https://arxiv.org/pdf/2204.01691.pdf). 

In a world built by and designed for humans, an intelligence that is agnostic to sensory-motor dynamics is going to be suboptimal, and superhuman skills beckon physical agency and universal control. Embodiment is absolutely indispensable for AGI.

\
\
_I’d like to acknowledge Ben Mann, Otavio Good, Jared Kaplan and Vivek Aithal for valuable discussions and Kanishka Rao, Vincent Vanhoucke and Alex Zirbel for providing feedback and proofreading._
\
_To engage with my ideas, add me on [Twitter](https://twitter.com/keerthanpg)._

{{< disqus >}}