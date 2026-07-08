# Reinforcement Learning (RL)
## References
[Slides1](https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/drl_v5.pdf) [Slide2](http://speech.ee.ntu.edu.tw/~tlkagk/courses/ML_2016/Lecture/RL%20(v6).pdf) (`pdfs/drl_v5.pdf`,  [[drl_v5.pdf]] and `pdfs/RL(v6).pdf`, [[RL(v6).pdf]])
Videos:
1. [【機器學習2021】概述增強式學習 (Reinforcement Learning, RL) (一) – 增強式學習跟機器學習一樣都是三個步驟](https://www.youtube.com/watch?v=XWukX-ayIrs)
2. [【機器學習2021】概述增強式學習 (Reinforcement Learning, RL) (二) – Policy Gradient 與修課心情](https://www.youtube.com/watch?v=US8DFaAZcp4)
3. [【機器學習2021】概述增強式學習 (Reinforcement Learning, RL) (三) - Actor-Critic](https://www.youtube.com/watch?v=kk6DqWreLeU)
4. [【機器學習2021】概述增強式學習 (Reinforcement Learning, RL) (四) - 回饋非常罕見的時候怎麼辦？機器的望梅止渴](https://www.youtube.com/watch?v=73YyF1gmIus)
5. [【機器學習2021】概述增強式學習 (Reinforcement Learning, RL) (五) - 如何從示範中學習？逆向增強式學習 (Inverse RL)](https://www.youtube.com/watch?v=75rZwxKBAf0)
6. https://www.youtube.com/watch?v=W8XF3ME8G2I
## TL;DR
## Introduction
+ The environment is partially observable (recap: [POMDP](https://en.wikipedia.org/wiki/Partially_observable_Markov_decision_process))
## Policy Gradient
![[Pasted image 20260708170214.png]]
![[Pasted image 20260708170432.png]]
> Question: Why do we have the probability in the denominator of $\nabla \overline{R}_\theta$
> Answer: 為了避免說 reward 比較少但出現機率較高的 action 被特別重視 (?)
## Actor-Critic
## Reward Shaping
## No Reward: Learning from Demonstration
## 經典
+ Q-learning https://en.wikipedia.org/wiki/Q-learning
+ Deep Q https://hackmd.io/@YungHuiHsu/BJgnMHbUH6
+ A3C https://zh.wikipedia.org/zh-tw/A3C
+ Sutton RL bible https://web.stanford.edu/class/psych209/Readings/SuttonBartoIPRLBook2ndEd.pdf
+ AlphaGO
	+ model-based (Use something like [蒙地卡羅](https://en.wikipedia.org/wiki/Monte_Carlo_method))
## read it later
+ Feed-forward network en.wikipedia.org/wiki/Feedforward_neural_network
+ stochastic (A stochastic process or system is connected with random probability.)
	+ [Stochastic Gradient Descent (SGD)](https://en.wikipedia.org/wiki/Stochastic_gradient_descent)
