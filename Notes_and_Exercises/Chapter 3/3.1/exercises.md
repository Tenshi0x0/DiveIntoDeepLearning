## Q1

1.

The goal can be considered as the parabola w.r.t. $b$.

Hence, the point of minimum is $\frac{\sum x_i}{n}$.

2.


Assume a Gaussian noise model
$$
x_i = b + \varepsilon_i,\quad \varepsilon_i \stackrel{iid}{\sim} \mathcal N(0,\sigma^2),
$$

then the likelihood of (b) is
$$
p(x_1,\dots,x_n\mid b)=\prod_{i=1}^n \frac{1}{\sqrt{2\pi\sigma^2}}
\exp\left(-\frac{(x_i-b)^2}{2\sigma^2}\right).
$$

So, maximizing this likelihood over $b$ is equivalent to minimizing $\sum (x_i-b)^2$.

3.

Notice that for a single term $|x_i - b|$, the gradient w.r.t. $b$ is $-1$ when $b < x_i$ and $1$ when $b>x_i$. To make the sum of graidient $0$, $b$ should be the median of $\{x_i\}$.

Thus, $b^\star$ is **any median** of $\{x_i\}$.

## Q4

1.

When $X^\top X$ is **singular**, the closed-form formula
$$
\hat\beta=(X^\top X)^{-1}X^\top y
$$
does not exist.

2.

Some fixes:

(1) Use the pseudoinverse.

(2) Add regularization

...

For add a small amount of coordinate-wise independent Gaussian noise：

It can bias the fitted model because the data matrix changed.

3.

Here,

$$
\tilde X = X + E,\quad E_{ij}\sim \mathcal N(0,\sigma^2)\ \text{i.i.d.}
$$

We have

$$
\tilde X^\top \tilde X = (X+E)^\top (X+E)=X^\top X + X^\top E + E^\top X + E^\top E.
$$

And,

$$
\mathbb E[X^\top E]=0,\quad \mathbb E[E^\top X]=0,\quad \mathbb E[E^\top E] = n\sigma^2 I_d.
$$

Hence,

$$
\mathbb E[\tilde X^\top \tilde X] = X^\top X + n\sigma^2 I_d\
$$

4.

The objective is not strongly convex (Hessian is only positive semidefinite), then we lose the nice linear convergence guarantees.