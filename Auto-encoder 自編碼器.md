reference: (`pdfs/auto_v8`)
[[auto_v8.pdf]]

+ Embedding, Representation, Code 都是指 encoder output 的 vector。
+ bert 可以當成一種 De-noise auto-encoder，不過 decoder 不一定要是 linear 的

auto-encoder 中的 encoder 可以用在降維 (dimension reduction) 的任務，encoder 則是負責從 embedding 還原原本的輸入！

所以整個模型的架構會像是一個沙漏，中間會有一個 bottleneck (由 encoder 輸出維度較低的向量)。為什麼可以 work? 因為以圖片為例，不一定每個像素都會被用來判斷 pattern，因此我們大多時候不會需要用到這麼高的維度去達成還原原本圖片的任務。