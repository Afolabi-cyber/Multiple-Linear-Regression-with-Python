Multiple Linear Regression using Gradient Descent
Overview
This project implements Multiple Linear Regression using Gradient Descent in pure Python (without external libraries like NumPy or Scikit-learn). The goal is to train a model that predicts an output variable based on multiple input features.

1. Understanding Multiple Linear Regression
Multiple Linear Regression models the relationship between a dependent variable 
𝑦
y and multiple independent variables 
𝑋
1
,
𝑋
2
,
…
,
𝑋
𝑛
X 
1
​
 ,X 
2
​
 ,…,X 
n
​
  using the following equation:

𝑦
=
𝑏
0
+
𝑏
1
𝑋
1
+
𝑏
2
𝑋
2
+
⋯
+
𝑏
𝑛
𝑋
𝑛
y=b 
0
​
 +b 
1
​
 X 
1
​
 +b 
2
​
 X 
2
​
 +⋯+b 
n
​
 X 
n
​
 
where:

𝑏
0
b 
0
​
  is the intercept (bias term).
𝑏
1
,
𝑏
2
,
…
,
𝑏
𝑛
b 
1
​
 ,b 
2
​
 ,…,b 
n
​
  are the coefficients (weights) for each independent variable.
The goal is to determine the best values for 
𝑏
0
,
𝑏
1
,
…
,
𝑏
𝑛
b 
0
​
 ,b 
1
​
 ,…,b 
n
​
  that minimize the prediction error.

2. Cost Function (Mean Squared Error)
To measure how well the model fits the data, we use the Mean Squared Error (MSE):

𝑀
𝑆
𝐸
=
1
𝑛
∑
𝑖
=
1
𝑛
(
𝑦
𝑖
−
𝑦
^
𝑖
)
2
MSE= 
n
1
​
  
i=1
∑
n
​
 (y 
i
​
 − 
y
^
​
  
i
​
 ) 
2
 
where:

𝑦
𝑖
y 
i
​
  is the actual value.
𝑦
^
𝑖
=
𝑏
0
+
𝑏
1
𝑋
𝑖
1
+
𝑏
2
𝑋
𝑖
2
+
⋯
+
𝑏
𝑛
𝑋
𝑖
𝑛
y
^
​
  
i
​
 =b 
0
​
 +b 
1
​
 X 
i1
​
 +b 
2
​
 X 
i2
​
 +⋯+b 
n
​
 X 
in
​
  is the predicted value.
𝑛
n is the total number of data points.
Our goal is to minimize this error.

3. Gradient Descent Optimization
Since MSE depends on 
𝑏
0
,
𝑏
1
,
…
,
𝑏
𝑛
b 
0
​
 ,b 
1
​
 ,…,b 
n
​
 , we use Gradient Descent to update them iteratively.

Computing Gradients
To minimize MSE, we compute the partial derivatives of the cost function with respect to each coefficient:

∂
𝑀
𝑆
𝐸
∂
𝑏
𝑗
=
−
2
𝑛
∑
𝑖
=
1
𝑛
𝑋
𝑖
𝑗
(
𝑦
𝑖
−
𝑦
^
𝑖
)
∂b 
j
​
 
∂MSE
​
 =− 
n
2
​
  
i=1
∑
n
​
 X 
ij
​
 (y 
i
​
 − 
y
^
​
  
i
​
 )
for each 
𝑗
=
0
,
1
,
2
,
…
,
𝑛
j=0,1,2,…,n.

When 
𝑗
=
0
j=0, 
𝑋
𝑖
𝑗
=
1
X 
ij
​
 =1 (for the bias term).
These gradients tell us how to adjust the coefficients to reduce error.
Updating Coefficients
Using the gradients, we update the coefficients iteratively:

𝑏
𝑗
=
𝑏
𝑗
−
𝛼
∂
𝑀
𝑆
𝐸
∂
𝑏
𝑗
b 
j
​
 =b 
j
​
 −α 
∂b 
j
​
 
∂MSE
​
 
where:

𝛼
α is the learning rate (step size for updates).
This process is repeated until the model converges (or for a fixed number of iterations).

📌 Summary
✅ Multiple Linear Regression extends simple linear regression to multiple features.
✅ We minimize Mean Squared Error (MSE) to find the best coefficients.
✅ Gradient Descent iteratively updates the coefficients until convergence.
✅ The learning rate 
𝛼
α determines how fast the model learns.

🚀 Happy Coding!

