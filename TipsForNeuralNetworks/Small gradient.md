[[small-gradient-v7.pdf]]

---

## Local minima and saddle point
https://youtu.be/QW6uINn7uGk?si=yekcwHQ6KuBTfF1g
+ 到 Saddle point 或是 local minima 時 gradient 都是 0，但可以去看 hessian matrix 的性質，如果是 positive definite 則為 local minima; 若為 negative definite 則為 local maxima; 否則就是 saddle point.
+ 到 saddle point 時仍然有逃脫的可能，因為負的 eigenvalue 所對應的 eigen vector，就是降低 cost 正確的更新方向
+ 高維度來看許多 local minima 其實是 saddle point。

---

## Batch and momentum
https://youtu.be/zzbr1h9sF54?si=cPMkQau9_yCsMOWx
