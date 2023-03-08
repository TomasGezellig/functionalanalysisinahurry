# *Banach spaces* 
We are now missing one structure element in order to get a Banach space. 

**Definition:** Consider some normed space $(V,||\cdot||)$. We say that $V$ is a complete normed space if and only if all Cauchy sequences are convergent sequences. More precisely, the existence of a sequence $(x_n)_{n\in \mathbb{N}}$ such that 

$$\lim_{n,m \to \infty} ||x_n-x_m|| =0$$ 

implies the existence of an $x\in X$, such that $x_n \to x$ with respect to $||\cdot||$. A complete normed space is said to be a *Banach space*. 

**Examples:**
1) Euclidean spaces. On $\mathbb{R}^n$, consider the norm $||x||_2 = \sqrt{\sum_{i=1}^n x_i^2}$. 
2) Sequence spaces. The space $l^p(\mathbb{R})$ consists of all sequences $x = (x_n)_{n\in \mathbb{N}}$ taking values in $\mathbb{R}$ such that $||x||_p = \Big(\sum_{n=1}^\infty |x_n|^p \Big)^{1/p}<\infty$. 
3) Space of continuous functions. Consider some compact topological space. Then, the set of continuous functions $f:K \to \mathbb{R}$ with norm given by $||f||_\infty = \sup_{x\in K}|f(x)|$ is a Banach space. 
4) Space of integrable functions. For $1 \leq p<\infty$, the space $L^p(\Omega)$ consisting of all measurable functions $f:\Omega \to \mathbb{R}$ such that $||f||_p = \Big(\int_\Omega |f|^p d\mu \Big)^{1/p}$ is a Banach space. 

It is also convenient to know the following characterizations of Banach spaces and subspaces. 

**Theorem:** Consider some normed space $(X,||\cdot||)$. Then, $X$ is a Banach space if and only if every absolutely convergent sum in $X$ is convergent in $X$, i.e. 

$$\sum_{n\geq 1} ||x_n|| <\infty \implies \exists \ x\in X: \sum_{n\geq 1} x_n =x$$

**proof:** Let us begin by assuming that we have a Banach space and that we assume an absolutely convergent sum $\sum_{n\geq 1} ||x_n|| <\infty$. Now, consider the sequence of partial sum, i.e. $\Big( \sum_{i=1}^n x_i \Big)_{n\geq 1}$. Consider some $n>m$ and notice that 

$$ \Big|\Big| \sum_{i=1}^n x_i - \sum_{i=1}^m x_i \Big|\Big| = \Big|\Big| \sum_{i=m+1}^n x_i  \Big|\Big| \to 0, \quad m,n\to \infty $$

Hence the sequence of partial sums is a Cauchy sequence. Since $X$ is Banach we conclude that the sequence of partial sums has a limit, and so $\sum_{n\geq 1} x_n$ converges. This proves one implication. Now, assume that every absolutely convergent sum converges in $X$, and consider some Cauchy sequenc $(x_n)_{n\geq 1}$ in $X$. We'd like to prove that $(x_n)_{n\geq 1}$ has a limit. Since the sequence is Cauchy we can pick indices $n_1 < n_2 < n_3 <...$ such that $||x_i-x_j|| <2^{-k}$ for $i,j \geq n_k$. This way $x_{n_1} + \sum_{k \geq 1} (x_{n_{k+1}} - x_{n_k})$ is an absolutely convergent series. Indeed, 

$$ \sum_{k \geq 1} ||x_{n_{k+1}} - x_{n_k}|| \sum_{k \geq 1} \frac{1}{2^k} < \infty  \leq $$

Thus, we can use our assumption to conclude that the partial sums have a limit, i.e. there is an $x\in X$ such that

$$ x = \lim_{m \to \infty} \Big( x_{n_1} + \sum_{k = 1}^m (x_{n_{k+1}} - x_{n_k})\Big) = \lim_{m\to \infty} x_{n_m}$$

This way we conclude that the subsequence $(x_{n_k})_{k\geq 1}$ has limit equal to $x$. To conclude that the entire sequence converges to $x$ simply notice that $||x-x_m|| \leq ||x - x_{n_m}|| + ||x_{n_m} - x_m|| \to 0$. The first term goes to zero because the subsequence converges, and the second term goes to zero as $m\to \infty$ because $(x_n)_{n\geq 1}$ is a Cauchy sequence by hypothesis. 


**Theorem:** Consider some normed space $(X,||\cdot||)$ and a subspace $Y\subset X$. Then, $Y$ is a Banach space with respect to the norm inherited from $X$ if and only if $Y$ is a closed subspace. 

**proof:** Assume $Y$ is Banach and consider some convergent sequence in $Y$. Since $Y$ is Banach the limit of the sequence lies necessarily inside $Y$. But this means that $Y$ contains all its limit points, hence it's closed. Now, assuming that $Y$ is closed. Consider some Cauchy sequence in $Y$. Then, since $X$ is Banach the sequence has a limit. And, since $Y$ is closed the limit lies inside $Y$. Therefore, $Y$ is a Banach space itself.  