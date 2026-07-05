ref (`pdfs/optimizer_v4.pdf`): [[optimizer_v4.pdf]]
https://youtu.be/HYUXEeh3kwY?si=jOa9m4Y6lSXQtcPl

---
rugged: 崎嶇
**Parameter Update:** $$ \boldsymbol{\theta}_i^{t+1} \leftarrow \boldsymbol{\theta}_i^t - \frac{\eta}{\sigma_i^t} \boldsymbol{g}_i^t $$
The updates of learning rate should be **parameter and iteration **dependent.
## adagrad
$$ \sigma_i^t = \sqrt{\frac{1}{t+1} \sum_{i=0}^t (\boldsymbol{g}_i^t)^2} $$
worse then rmsprop when encoutering some complex error surfaces.
## rmsprop
Exponential Moving Average:
$$ \sigma_i^t = \sqrt{\alpha(\sigma_i^{t-1})^2 + (1 - \alpha)(\boldsymbol{g}_i^t)^2} $$
$$ 0 < \alpha < 1 $$

## Adam
Vanilla Gradient Descent with:
+ Momentum. (Please refer to note in [[Small gradient]])
+ rmsprop
## Learning rate sheduling
+ **Decay**: We do so since the step size could be smaller when we are close to destination.
+ **Warm-up**: Increase first, decrease later. 基本上就是魔法，我其實還是不太懂原理。

### To learn
- [ ] RAdam: https://arxiv.org/abs/1908.03265