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