[[classification_v2.pdf]]
https://youtu.be/O2VkP8dJ5FE?si=r3lEw3VtfTgvX5zL

---

## As a regression
不能直接將每個分類指定為一個數字，因為假設 class 1 是 1，class 2 是 2, class 3 是 3。
這樣間接假設 class 1&3 的關係較 class 1&2 遠。

所以可以用 one-hot vector represent 各個 class，這樣每個 class 之間的距離就一樣了。

這裡開始會用到 neural network 的概念，詳請可以參考先前的筆記:
[[Introduction to Deep Learning]]

