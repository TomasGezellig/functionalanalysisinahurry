### *Linear Operators*
As it is often the case in Mathematics, now that we have a class of spaces with a reasonable structure, i.e. normed spaces and, in particular, Banach spaces, we can concern ourselves with mappings between these spaces. 

**Definition:** Consider two normed spaces $X$ and $Y$. The map $T:X\to Y$ is said to be a linear bounded operator if it is linear, i.e. 

$$T(\alpha x_1 + \beta x_2) = \alpha T(x_1) + \beta T(x_2)$$ 

for all $x_1,x_2\in X$ and scalars $\alpha,\beta$, and if there is a finite constant $C>0$ such that 

$$||Tx||\leq C||x||, \quad \forall x\in X$$ 

The infimum of all admissible constants $C$ is itself admissible and is given by 

$$\sup_{x\in X,x\neq0}\frac{||Tx||}{||x||}$$ 

This number is said to be the norm of the operator $T$ and is denoted by $||T||$. 

**Observation:** In the characterisation of boundedness, notice that the norm on the RHS of the inequality corresponds to the norm of $X$, whereas the norm on the LHS of the inequality corresponds to the norm of $Y$! 

It is not hard to come up with reasons why boundedness is a desirable property for an operator. To begin with, any bounded operator will be continuous, and continuity is always welcomed. 

**Proposition:** Consider two normed spaces $X$ and $Y$. The following assertions are equivalent:
1) The linear operator $T:X \to Y$ is bounded.
2) The linear operator $T:X \to Y$ is continuous.
3) The linear operator $T:X \to Y$ is continuous at a given point $x_0 \in X$.

**proof:**

$1) \implies 2):$ Simply notice that $||Tx - Tx_0|| = ||T(x-x_0)|| \leq ||T|| \cdot ||x-x_0||$, so following the $\epsilon-\delta$ definition of continuity one only has to pick $\delta = \epsilon/||T||$ 

$2) \implies 3):$ Obvious. 

$3) \implies 1):$ 

Now, guess what... The set of all linear bounded operators from $X$ to $Y$ forms a vector space as well! Indeed, scalar multiplication and addition are defined in a very natural way by taking 

$$(cT)x := c(Tx) \quad \land \quad (T+T')x := Tx+T'x$$ 

We denote this vector space by $\mathcal{L}(X,Y)$. In addition, we can equip it with a norm. What norm? Well, it would be reasonable to consider the operator norm from the Definition above as the norm of the space. Observe that 

$$\begin{align*}&||(c T)x||_Y = ||c(Tx)||_Y=|c|\cdot ||Tx||_Y \leq |c|\cdot ||T||_{\mathcal{L}(X,Y)} \cdot ||x||_X \implies||cT||_{\mathcal{L}(X,Y)} \leq |c|\cdot ||T||_{\mathcal{L}(X,Y)}\end{align*}$$ 

As a matter of fact, 

$$\sup_{||x||\neq 0}\frac{||cTx||}{||x||} = |c|\cdot ||T||,$$ 

so $||(cT)|| = |c|\cdot ||T||$, corresponding to the homogeneity property of norms. Notice that the norms are indexed according to their space! The common practise is to simply write $||\cdot||$ because the space is implicitly understood. One can also easily prove the triangle inequality for the norm in $\mathcal{L}(X,Y)$. Note that 

$$||(T+T')x|| = ||Tx + T'x|| \leq ||Tx|| + ||T'x|| \leq  (||T|| + ||T'||)\cdot ||x||$$ 

and the result follows by taking the supremum on both sides. Positivity is also clear, and we can then conclude that the norm of an operator can be taken as a norm in the space $\mathcal{L}(X,Y)$. One additional remark is given by the following theorem.

**Theorem:** Consider two normed space $X$ and $Y$. If $Y$ is a Banach space, then $\mathcal{L}(X,Y)$ is a Banach space.

*proof:* Of course, if we want to show that $\mathcal{L}(X,Y)$ is a Banach space, then the reasonable starting point is to assume one has a Cauchy sequence of operators $(T_n)_{n\geq 1}$, i.e. $||T_n - T_m||\to 0$ as $m,n\to \infty$. Now, consider some $x\in X$. Notice that $||T_nx - T_mx|| = ||(T_n-T_m)x||\leq ||T_n-T_m||\cdot ||x|| \to 0$, which means that $(T_n x)_{n\geq 1}$ is a Cauchy sequence in $Y$. And, $Y$ is a Banach space! Hence there is a limit for this sequence. Let us denote the limit by $Tx$, i.e. $T_n x \to Tx$ in $Y$. By linearity of the operators $T_n$ we conclude that $x\mapsto Tx$ is also linear. In addition, $||Tx|| = \lim_n ||T_n x|| \leq M ||x||$, where $M = \sup_n ||T_n||$, so $T$ is bounded and thus $T \in \mathcal{L}(X,Y)$. Notice that $M<\infty$ since $(T_n)_{n\geq 1}$ is a Cauchy sequence by assumption. Hence, the only thing left to show is that $||T-T_n|| \to 0$ in $\mathcal{L}(X,Y)$. But this follows from the fact that, for all $x\in X$ we have 

$$||T_nx-T_mx|| \leq \epsilon \implies ||T_n x - Tx||\leq \epsilon, \quad \text{by taking} \ m\to \infty$$ 

Therefore $||T-T_n||\leq \epsilon$.  

**Observation:**In the particular case when $Y=\mathbb{K}$, i.e. it coincides with the scalar field (usually $\mathbb{R}$ or $\mathbb{C}$), we have that $\mathcal{L}(X,\mathbb{K})$ is a Banach space and we call it the **dual space** of $X$.  

We end this section with arguably the most used and elementary result about bounded linear operators. This result goes by the name "*density argument*" and its usefulness comes from the fact that it is often the case in analysis that a given property, which can be written in the form of an operator, is more easily proved to be true for a specific collection of objects. If we then show that this collection is dense on a given space, we can use the density argument to generalise the property to the whole space. 

**Theorem:** Consider some normed space $X$ and a Banach space $Y$. Assume that $X_0$ is a dense subspace of $X$. If $T_0:X_0 \to Y$ is a bounded linear operator, then there exists a unique bounded linear operator $T:X\to Y$ that extends $T_0$, i.e. $T|_{X_0} = T_0$. Moreover, $||T|| = ||T_0||$. 

**proof:** Let us consider some $x\in X$. Then, by density of $X_0$ we have a sequence $(x_n)_{n\geq 1} \subset X_0$ such that $x_n \to x$. Now, notice that 

$$||T_0 x_n - T_0 x_m|| = ||T_0(x_n-x_m)|| \leq ||T_0|| \cdot ||x_n-x_m|| \to 0, \quad n,m\to \infty$$ 

Therefore, $(T_0 x_n)_{n\geq 1}$ is a Cauchy sequence. Now, since $Y$ is a Banach space we conclude that $T_0 x_n \to y$ for some $y\in Y$. Will this limit lead to a well-defined operator? Well, let us assume that we had another sequence $(x_n')_{n\geq 1}$ such that $x_n' \to x$. Then, by the same argument as before we would have $T_0x_n'\to y'$ for some $y' \in Y$. We only need to show that $y'=y$. Indeed, 

$$||y-y'|| = \lim_{n\to \infty }||T_0 x_n - T_0 x_n'|| \leq \lim_{n\to \infty} ||T_0||\cdot (||x-x_n|| + ||x-x_n'||)\to 0$$ 

So, we can denote the common limit $y=y'$ by $Tx$ and we can clearly see that this operator $x\mapsto Tx$ is linear and extends $T_0$. About the norm of $T$, I'll leave as an exercise to the reader to show that $||T|| = ||T_0||$. Sorry. But the temptation is too big and I'm weak. 