references: (`pdfs/bert_v8`)
[[bert_v8.pdf]]

## Masking input (P.12)
選擇哪些字被蓋住、mask的方法都是隨機的。

bert輸出的 vector 經過 linear 的 model (basically a matrix, much smaller than bert) 以及 softmax 的處理後，會是一個 distribution vector (如果是中文字的話，這個向量的長度會是所有方塊字的數量)，表示出每個token(?)出現的機率。最後跟 ground truth 做比較，目標是 minimize 他們之間的 cross entropy :)

## Next sentence prediction (P.13)
Yes/No 回答的問題是：兩個句子是不是相接的？

這個方法表現不好的可能原因是太簡單ㄌ XD

SOP 是指說給定兩個本就相接的句子，但是順序不知道，機器需要去預測。
### P.14
訓練出 bert 的過程稱作 pre-train，微調去達成各種 downstream tasks 的過程稱作 fine-tuning。
## P.16
Q. 為什麼要有人類的分數？
A: 因為不同 metric 無法直接比較。

## How to use BERT – Case 2 (P.20)
The parameters in the BERT part are ramdomly initialization. (it's already found in the pre-train)

## Case 3 (P.21)
NLI (aka textual entailment): https://en.wikipedia.org/wiki/Textual_entailment

entailment: the relationship between two statements when for one to be true, the other must also be true.

## Case 4 - QA (P.23~P.25)
+ s: 開始的 index
+ e: 結束的 index

橙色的向量是開始位置的 query，藍色向量則是結束位置的 query。(這裡黃色向量可以被當成是 key(?))，因為他們都是 random initialized 的，所以需要經過訓練。

