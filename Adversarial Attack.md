## Introduction
Here, $e$ means cross entropy. If $y$ and $\hat{y}$ has almost the same distribution, the cross entropy should be low.
![[Pasted image 20260716160307.png]]
+ $d$ usaully uses L-infinity in the scenario of image classification
+ **Fast** Gradient Sign Method only runs one iteration, the learning rate is set as $\varepsilon$. 
+ *Iterative* **FGSM** run more than one iterations, the learning rate is often smaller than $\varepsilon$. This method seems to perform better than FSGM (one iteration)
+ We know the parameters of the model when calculating the gradient, so **FGSM** is one kind of **white box attack**.
![[Pasted image 20260716160618.png]]
## Blackbox attack
+ Some times we don't have the model, even the training data
+ **Network Proxy**: the network we try to obtain (we "predict" what the actual model is).
+ What if we don't have training data? We can still generate the training data by ourselves, and get the corresponding output. 用這成對的資料去訓練一個 proxy network :)
+ Black box attack performs better on **non-targeted** task.
![[Pasted image 20260716165253.png]]
上圖想表達什麼呢？
+ 較上面的表格：對角線是 white box attack，所以可以讓 attacked model 的準確率是0。proxy 基本上就是我們預測 attacked model 是哪一種
+ 較下方的表格：側欄一樣是 proxy，上欄一樣是 attacked model。減號代表的是 5 個 model 的 [[Ensemble]]，去掉減號後方的模型。所以對角線變成了 blackbox attack，不過我們可以看到整體的準確率非常高。