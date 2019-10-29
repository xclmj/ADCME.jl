# Overview

**Inverse modeling** (IM) identifies a certain set of parameters or functions with which the outputs of the forward analysis matches the desired result or measurement. IM can usually be solved by formulating it as an optimization problem. But the major difference is that IM aims at getting information not accessible to forward analysis, instead of obtaining an optimal value of a fixed objective function and set of constraints. In IM, the objective function and constraints can be adjusted, and prior information of the unknown parameters or functions can be imposed in the form of regularizers, to better reflect the physical laws. 

For example, given an image $x\in\mathbb{R}^{1024\times 1024}$, the forward analysis is given by $y = F(x) = \sum_{i,j} x_{i,j}$, i.e., the summation of all pixel values. One possible IM problem requires you to estimate $x$ given the measurement $y$. It can be formulated an optimization problem $\min_x (F(x)-y)^2$, which is underdetermined. However, if we have the prior that the image is a pure color image, then the inverse problem is well-defined and has a unique solution. There are many ways to impose this prior as contraints to the optimization problem, but the IM problem itself may not be described as an optimization problem. 

![](./asset/im.png)