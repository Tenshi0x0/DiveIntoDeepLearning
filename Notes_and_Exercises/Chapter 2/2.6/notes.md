## Expectations

Consider covariances of vector random variables.

$$
\boldsymbol{\Sigma} \stackrel{\textrm{def}}{=} \textrm{Cov}_{\mathbf{x} \sim P}[\mathbf{x}]
= E_{\mathbf{x} \sim P}\!\left[(\mathbf{x} - \boldsymbol{\mu})(\mathbf{x} - \boldsymbol{\mu})^\top\right].
$$

That is,

$$
\boldsymbol{\Sigma}_{ij}
= E\!\big[(x_i-\mu_i)(x_j-\mu_j)\big]
= \mathrm{Cov}(x_i,x_j).
$$

We can use $\boldsymbol{\Sigma}$ to compute the variance for any linear function of $\mathbf{x}$.

Starting from the definition:

$$
\boldsymbol{\Sigma} = E\!\left[(\mathbf{x}-\boldsymbol{\mu})(\mathbf{x}-\boldsymbol{\mu})^\top\right].
$$

Thus,

$$
\begin{aligned}
\mathbf{v}^\top \boldsymbol{\Sigma}\,\mathbf{v}
&= E\!\left[\mathbf{v}^\top (\mathbf{x}-\boldsymbol{\mu})(\mathbf{x}-\boldsymbol{\mu})^\top \mathbf{v}\right] \\
&= E\!\left[\big((\mathbf{x}-\boldsymbol{\mu})^\top \mathbf{v}\big)\big(\mathbf{v}^\top(\mathbf{x}-\boldsymbol{\mu})\big)\right].
\end{aligned}
$$

Note that $(\mathbf{x}-\boldsymbol{\mu})^\top \mathbf{v}$ is a scalar and equals $\mathbf{v}^\top(\mathbf{x}-\boldsymbol{\mu})$. Therefore,

$$
\mathbf{v}^\top \boldsymbol{\Sigma}\,\mathbf{v}
= E\!\left[\big(\mathbf{v}^\top(\mathbf{x}-\boldsymbol{\mu})\big)^2\right].
$$

On the other hand,

$$
\begin{aligned}
\mathrm{Var}(\mathbf{v}^\top \mathbf{x})
&= E\!\left[\big(\mathbf{v}^\top \mathbf{x} - E[\mathbf{v}^\top \mathbf{x}]\big)^2\right] \\
&= E\!\left[\big(\mathbf{v}^\top(\mathbf{x}-\boldsymbol{\mu})\big)^2\right].
\end{aligned}
$$

Hence, $\mathrm{Var}(\mathbf{v}^\top \mathbf{x})=\mathbf{v}^\top \boldsymbol{\Sigma}\,\mathbf{v}$.


## Discussion

> Proof of Chebyshev's inequality: https://en.wikipedia.org/wiki/Chebyshev%27s_inequality

