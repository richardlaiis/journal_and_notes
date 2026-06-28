references: (`pdfs/bert_v8`)
[[bert_v8.pdf]]

## Masking input (P.12)
選擇哪些字被蓋住、mask的方法都是隨機的。

bert輸出的 vector 經過 linear 的 model (basically a matrix, much smaller than bert) 以及 softmax 的處理後，會是一個 distribution vector (如果是中文字的話，這個向量的長度會是所有方塊字的數量)，表示出每個token(?)出現的機率。最後跟 ground truth 做比較，目標是 minimize 他們之間的 cross entropy :)

## Next sentence prediction (P.13)
Yes/No 回答的問題是：兩個句子是不是相接的？

這個方法表現不好的可能原因是太簡單ㄌ XD

- [ ] 目前影片看到 13:18
