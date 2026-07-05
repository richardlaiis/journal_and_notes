references (`pdfs/regression (v16).pdf`):  [[regression (v16).pdf]]
## Summary
+ We could use **activation functions/neurons** (**Sigmoid or ReLU**) to simulate any function in **piecewise** manner (Take the linear combinations of the functions)
+ Optimize the parameters (e.g. weights, bias) using **gradient descent** and the loss decreases.
+ The training data can be separated into several **batches**, each update (of gradient descent) takes one batch. We call one **epoch** elapsed after all batches are seen. (e.g. N=10000, Batch size B=10, then in 1 epoch we have 10000/10=1000 updates)
	+ Why do we need batch setting? Please see [[Small gradient]], this setting will have lower cost on both training data and testing data.

![[Pasted image 20260703111637.png]]

![[Pasted image 20260703111746.png]]

![[Pasted image 20260703112134.png]]


We can doooo this for many layers, just repeat the process... Tadaaaa! This is a **neural network**.
![[Pasted image 20260703112608.png]]
## Related materials
- [ ] Back propagation
- [ ] [[General Guidance of ML]]