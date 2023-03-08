# *Banach spaces* 
We are now missing one structure element in order to get a Banach space. 

**Definition:** Consider some normed space $(V,||\cdot||)$. We say that $V$ is a complete normed space if and only if all Cauchy sequences are convergent sequences. More precisely, the existence of a sequence $(x_n)_{n\in \mathbb{N}}$ such that 

$$\lim_{n,m \to \infty} ||x_n-x_m|| =0$$ 

implies the existence of an $x\in X$, such that $x_n \to x$ with respect to $||\cdot||$. A complete normed space is said to be a *Banach space*. 

*Examples:*
1) Euclidean spaces. On $\mathbb{R}^n$, consider the norm $||x||_2 = \sqrt{\sum_{i=1}^n x_i^2}$. 
2) Sequence spaces. The space $l^p(\mathbb{R})$ consists of all sequences $x = (x_n)_{n\in \mathbb{N}}$ taking values in $\mathbb{R}$ such that $||x||_p = \Big(\sum_{n=1}^\infty |x_n|^p \Big)^{1/p}<\infty$. 
3) Space of continuous functions. Consider some compact topological space. Then, the set of continuous functions $f:K \to \mathbb{R}$ with norm given by $||f||_\infty = \sup_{x\in K}|f(x)|$ is a Banach space. 
4) Space of integrable functions. For $1 \leq p<\infty$, the space $L^p(\Omega)$ consisting of all measurable functions $f:\Omega \to \mathbb{R}$ such that $||f||_p = \Big(\int_\Omega |f|^p d\mu \Big)^{1/p}$ is a Banach space. 

It is also convenient to know the following characterizations of Banach spaces and subspaces. 

**Theorem:** Consider some normed space $(X,||\cdot||)$. Then, $X$ is a Banach space if and only if every absolutely convergent sum in $X$ is convergent in $X$, i.e. 

$$\sum_{n\geq 1} ||x_n|| <\infty \implies \exists \ x\in X: \sum_{n\geq 1} x_n =x$$

*proof:*

**Theorem:** Consider some normed space $(X,||\cdot||)$ and a subspace $Y\subset X$. Then, $Y$ is a Banach space with respect to the norm inherited from $X$ if and only if $Y$ is a closed subspace. 