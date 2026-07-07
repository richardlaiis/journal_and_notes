# CNN (Convolutional Neural Network)
## References
Slides (`pdfs/cnn_v4.pdf`, [[cnn_v4.pdf]]): https://speech.ee.ntu.edu.tw/~hylee/ml/ml2021-course-data/cnn_v4.pdf
Video: https://youtu.be/OP5HcXJg2Aw?si=g5NI7J1I5ZjMD6fu
## TL;DR
CNN consists of three important features:
+ Receptive fields
+ Filters (Shared parameters among neurons)
+ Pooling (Optional since it may affect the performance)
## Convolution layer
![[Pasted image 20260707160337.png]]

After each convolution layer (the image went through all **filters**), we obtain a **feature map**, it can be viewed as a image, but the channel number may increase.

In this example, if we have 64 filters, the feature map is a `4*4*64` tensor, and the filters in the next convolution layer should have the shape of `3*3*64` instead of `3*3*1`.

![[Pasted image 20260707160720.png]]

Can CNN see larger regions? YES!!! In this example, the filter in the second convolution layer is still three times three, but the actual region it process is five times five. :)

## Spatial Transformer Layer
CNN 沒辦法處理經過縮放、旋轉過後的圖片，因此我們需要這個技術，影片如下：
https://www.youtube.com/watch?v=SoCywZ1hZak