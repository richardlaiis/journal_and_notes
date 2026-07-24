https://www.geeksforgeeks.org/machine-learning/ml-locally-weighted-linear-regression/

# Locally weighted regression
## Approach
We try to minimize the cost function in locally weighted regression.
$$J(\theta) = \sum_{i=1}^{m} w^{(i)}(\theta^T x^{(i)} - y^{(i)})^2$$

What is the weight for each data point? ($x$ is the query point)
$$w^{(i)} = \exp\left(-\frac{(x^{(i)} - x)^2}{2\tau^2}\right)$$
We can find the closed form solution that minimize $J(\theta)$ using the following formula:
$$\theta = (X^T W X)^{-1} X^T W y$$
## 原理
越靠近 query point 的點我們給與的權重越接近 1，有點像是我們只對 query point 附近的點做 linear regression。不過缺點顯而易見，這個方法沒有一個global model，運算量肯定會太大，儘管可以應對非線性的問題。
