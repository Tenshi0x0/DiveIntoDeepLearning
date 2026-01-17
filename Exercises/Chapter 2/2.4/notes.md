## Partial Derivatives and Gradients

Given $f: \mathbb{R}^n \to \mathbb{R}$ and vector $\mathbf{x} = [x_1, x_2, \dots, x_n]$.

We have: 

- For all $\mathbf{A} \in \mathbb{R}^{m \times n}$, then $\nabla_{\mathbf{x}} \mathbf{A} \mathbf{x} = \mathbf{A}^\top$ and $\nabla_{\mathbf{x}} \mathbf{x}^\top \mathbf{A} = \mathbf{A}$.
    > Because we define that $dy = (\nabla_x y)\top dx$, so $\nabla_x y = J^T$ and $J$ is the Jacobian matrix.

- And for square matrix $\mathbf{A} \in \mathbb{R}^{n \times n}$, $\nabla_{\mathbf{x}} \mathbf{x}^\top \mathbf{A} \mathbf{x} = (\mathbf{A} + \mathbf{A}^\top)\mathbf{x}$.
    > Let $f(\mathbf x)=\mathbf x^\top \mathbf A\mathbf x$. \
    > Then, $df = (d\mathbf x^\top)\mathbf A\mathbf x + \mathbf x^\top \mathbf A (d\mathbf x).$  \
    > We can transpose $(d\mathbf x^\top)\mathbf A\mathbf x$ since it is scalar. So we have $df = \mathbf x^\top (\mathbf A+\mathbf A^\top) d\mathbf x$. \
    > According to the definition, $df = (\nabla_{\mathbf x} f)^\top d\mathbf x.$ \ 
    > Finally, $\nabla_{\mathbf x} f = (\mathbf A+\mathbf A^\top) \mathbf x$ holds.

    ## Chain Rule

    $\frac{\partial y}{\partial x_{i}} = \frac{\partial y}{\partial u_{1}} \frac{\partial u_{1}}{\partial x_{i}} + \frac{\partial y}{\partial u_{2}} \frac{\partial u_{2}}{\partial x_{i}} + \ldots + \frac{\partial y}{\partial u_{m}} \frac{\partial u_{m}}{\partial x_{i}} \ \textrm{ and so } \ \nabla_{\mathbf{x}} y =  \mathbf{A} \nabla_{\mathbf{u}} y$. 

    Here $\mathbf{A} \in \mathbb{R}^{n\times m}$ is actually $J^\top$ ($J_{ji} = \frac{\partial u_j}{\partial x_i}$).