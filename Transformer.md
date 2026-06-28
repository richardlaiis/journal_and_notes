references: (`pdfs/seq2seq_v9.pdf`)
[[seq2seq_v9.pdf]]

## P.29
Masked Self-attention: 由於 autoregressive 的設計，vector sequence 並不是一次輸入進去，而是一個一個輸入，所以計算第 i 個向量的 output 時，我們只需要考慮前面與當前的 vector！
## P.34
把 END 當成其中一個 token，當output它的機率最大時 output 他，並結束這個有點遞迴性的過程。
## P.36
AT example: [Tacotron](https://arxiv.org/abs/1703.10135)
NAT example: [Fastspeech](https://arxiv.org/abs/1905.09263)

NAT是一個大坑！而且我還不知道 Multi-modality 跟 [LSTM](https://en.wikipedia.org/wiki/Long_short-term_memory) 是什麼 qwq

## P.42
The darker square means higher attention score with a specific audio pieces (i.e. the output of encoder)

It shows an example of cross attention!

## P.43
因為 encoder 跟 decoder 都有很多層，事實上你不一定要用最後一層 encoder 的 output 當成 decoder cross attention 的 input，只是原始論文是這樣實作罷了。
## P.53~P.54
Beam search 比較適合用在較有正確答案可參考的任務中，有randomness加入的方式在較需要創造力的任務中表現較好(例如 tts)

有個小故事是，hylee的實驗室發現在seq2seq的訓練中，給decoder參考的output加入一些雜訊後，反而模型表現較好，cool

## P.55
Why not use BLEU score as a loss function design?
+ not differentiable

## P.56
(scheduled sampling)
有時訓練模型時，我們會在decoder的input中加入一些不是ground truth的部份，這樣可以改善 exposure bias，但似乎也會影響到平行化的表現 