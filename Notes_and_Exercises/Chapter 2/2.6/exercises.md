## Q5

(In this problem, value of $P(\mathcal{A}), P(\mathcal{B})$ is fixed. So our goal is not to construct the cases (e.g. Construct the case that $\mathcal{A}\cap \mathcal{B}=\empty$ and claim the lower bound of $P(\mathcal{A} \cap \mathcal{B})$ is $0$).)

Lower bounds:

- $P(\mathcal{A} \cup \mathcal{B})$: $\max\big(P(\mathcal{A}), P(\mathcal{B})\big)$.

- $P(\mathcal{A} \cap \mathcal{B})$: In best case, $\mathcal{B}$ should avoid overlapping with $\mathcal{A}$ as much as possible. So the smallest overlapping "area" is $P(\mathcal{B}) - (1 - P(\mathcal{A}))$. Thus, the answer is $\max\big( 0, P(\mathcal{A}) + P(\mathcal{B}) - 1 \big)$.

Upper bounds:

- $P(\mathcal{A} \cup \mathcal{B})$: $\min\big(1, P(\mathcal{A}) + (\mathcal{B})\big)$.

- $P(\mathcal{A} \cap \mathcal{B})$: $\min\big(P(\mathcal{A}), P(\mathcal{B})\big)$.

## Q6

$$
P(A, B, C) = P(A) P(B | A) P(C | A, B) = P(A) P(B | A) P(C | B) 
$$