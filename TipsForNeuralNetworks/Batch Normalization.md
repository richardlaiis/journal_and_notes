references(`pdfs/normalization_v4.pdf`): [[normalization_v4.pdf]]
Link: https://youtu.be/BABPWOkSbLE?si=OJ8ZRW4cXVilSOs5

---
![[Pasted image 20260706100042.png]]

 **Page 2**
 (假設 $\Delta w_1$ 跟 $\Delta w_2$ 的變化差不多) 因為 x1 基本上都是很小的值，$\Delta L$ 的變化也會很小。不過 x2 的值都蠻大的，所以在 Loss surface $w_2$ 方向會比較 steep，有沒有方法讓這個 surface 看起來比較均衡呢？就是讓他在各個方向看起來差不多陡峭？ (i.e. 讓 x1, x2 有相同的數值範圍)

**Page 5**
基本上 normalization 要放在 activation function 之前或之後都可以。(不過如果是 sigmoid 的話，推薦在 z 那層做，原因未知)

**Page 7**
因為 variance, mean 都會受到每個 sample vector 的影響，所以他們變得不再獨立。只要改變一個向量的值，就會改變其它向量在各層的輸出，以及normalize過後的值。

+ What is benchmark corpus?: https://hackmd.io/@Jaychao2099/gen-ai-8

## key
+ batch nornalization 就是本來需要看全部的資料才能得到 mean, variance 現在只需要每次看一個 batch
+ moving average for each batch obtained in training can be used in testing/inference (yeah, testing and inference have the same meaning)
+ serendipitous hehe
