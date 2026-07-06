[[classification_v2.pdf]]
https://youtu.be/O2VkP8dJ5FE?si=r3lEw3VtfTgvX5zL

---

## As a regression
不能直接將每個分類指定為一個數字，因為假設 class 1 是 1，class 2 是 2, class 3 是 3。
這樣間接假設 class 1&3 的關係較 class 1&2 遠。

所以可以用 one-hot vector represent 各個 class，這樣每個 class 之間的距離就一樣了。

這裡開始會用到 neural network 的概念，詳請可以參考先前的筆記:
[[Introduction to Deep Learning]]

**softmax** 可以將一個向量中的值挪到 0 和 1 之間，而且總和為 1。softmax 可以讓大小值的差距更明顯 (?)
+ Logit: https://en.wikipedia.org/wiki/Logit
+ In binary classification, we can directly use sigmoid function on two classes. why?

**Cross entropy** 比 MSE 更適合用於分類問題，而且可以避免 Gradient descent 時卡住。(在沒有好的 optimizer 的情況下)
+ Minimizing cross-entropy is equivalent to maximizing likelihood.
+ I don't understand so far, so I should refer to the following materials in the future:
+ http://speech.ee.ntu.edu.tw/~tlkagk/courses/MLDS_2015_2/Lecture/Deep%20More%20(v2).ecm.mp4/index.html
+ http://speech.ee.ntu.edu.tw/~tlkagk/courses/MLDS_2015_2/Lecture/Deep%20More%20(v2).pdf