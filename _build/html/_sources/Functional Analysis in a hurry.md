In these notes, I will briefly go through the basic notions of Functional Analysis. To put it briefly, I will synthetise? the concepts I consider to be fundamental to the working mathematian. These include: Banach spaces, linear bounded operators and Hilbert spaces. So, only the very basic and some useful results in the scope of these concepts. I'll aim for brevity and clarity. 

**Prerequisites:** Knowledge about vector spaces. 

### *Normed spaces* 
One can arrive at Banach spaces by imposing more structure into the general notion of a vector space. To do so, we may begin by equipping the space with a very neat function: *a norm*. 

**Definition:** Consider some vector space $V$ over the scalar field $\mathbb{K}$. A norm is a function $||\cdot||:V \to \mathbb{R}^+_0$ with the following properties:
1) Positivity: $||v|| = 0 \Leftrightarrow v=0$ for all $v\in V$
2) Homogeneity: $||\alpha v|| = |\alpha|\cdot ||v||$ for all $\alpha \in \mathbb{K}$ and $v\in V$
3) Triangle inequality: $||v + w ||\leq ||v|| + ||w||$ for all $v,w \in V$ 

Intuitively, a norm is simply a measure of the magnitude of a vector, i.e. an element of the vector space. More importantly, a norm allows us to relate two vectors via a *metric*, i.e. a distance function. 

**Definition:** Let $V$ be some vector space. A *metric* will be a map $d: V\times V \to \mathbb{R}_0^+$ with the following properties:
1) Positivity: $d(v,u)>0$ for $u\neq v\in V$ and $d(u,v)=0 \Leftrightarrow u=v$
2) Symmetry: $d(u,v) = d(v,u)$ for all $u,v \in V$
3) Triangle inequality: $d(u,w) \leq d(u,v) + d(v,w)$ for all $u,v,w\in V$

**Definition:** Let $(V,||\cdot||)$ be a vector space equipped with a norm. We say it is a *normed space*. 

*Example:* The usual Euclidean space $\mathbb{R}^n$ with the $2-$norm, i.e. the norm given by $||x||_2 = \sqrt{\sum_{i=1}^n x_i^2}$. 

**Remark:** The same vector space can have different norms. A quick search on Wikipedia about Euclidean space will confirm this xD. 

Anyways, now we have a normed space! Which, in its turn, is a metric space. More structure, more possibilities... Observe that we now can make rigorous the notion of closeness. And, if one talks about closeness between elements of a vector space, one inevitably ends up talking about convergence of sequences. 

**Definition:** Consider some normed space $(V,||\cdot ||)$ and a sequence of elements $\{v_n\}_{n\in \mathbb{N}}$ in $V$. We say that $v_n$ converges to $v$, and denote it by $v_n\to v$ if and only if $||v-v_n|| \to 0$. 

Quite reasonable. 

### *Completeness*
Completeness is just one of those things that any math student ought to know. To motivate the concept one can reason as follows:

- Let's consider the real line for simplicity. And, take some convergent sequence $(x_n)_{n\in \mathbb{N}}$ of real numbers, i.e. $x_n \to x$ for some $x\in \mathbb{R}$. 
- Since the sequence converges, there is an integer $N$ such that for all $n>N$ we have $|x-x_n|<\epsilon$, where $\epsilon$ is some arbitrarily small positive constant. 
- This then implies that, at least from a certain point onwards, consecutive elements of the sequence get closer and closer, i.e. the distance between consecutive elements decreases and becomes arbitrarily small as well.  
- Therefore, a convergent sequence has the peculiarity that from a certain point onwards, its elements get arbitrarily closer. 

A sequence with this property is said to be a Cauchy sequence.

**Definition:** Consider some normed space $(V,||\cdot||)$ and a sequence $(v_n)_{n\in \mathbb{N}}$. Then, the sequence is said to be a Cauchy sequence if $||v_n-v_m|| \to 0$ as $m,n \to \infty$. Or, more precisely, if $$\forall \epsilon>0,\exists N\in \mathbb{N}: \forall m,n>N, \ ||x_n-x_n||<\epsilon$$ 
Taking into account the reasoning above, the opposite question emerges: Do all Cauchy sequences converge? We saw that convergent sequences are Cauchy, and now we're interested in knowing whether all Cauchy sequences are convergent. Well..... No! It depends on the space under consideration. More specifically, it depends on the underlying set of the space under consideration.

*Example:* Consider the rationals $\mathbb{Q}$ as a vector space over the field $\mathbb{Q}$ and the usual operations. Now, take the following sequence: $$x_n = \text{approximation to the nth decimal place of} \ \pi$$ Then, $x_1 = 3.1, x_2 = 3.14, x_3 = 3.141,...$ This sequence is composed of rational numbers, but its limit is $\pi$, which does not belong in $\mathbb{Q}$. 


Talvez este texto esteja a ficar demasiado abebezado... 

*"""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""""*

In these notes, I will briefly go through the basic notions of Functional Analysis. To put it briefly, I will synthetise? the concepts I consider to be fundamental to the working mathematian. These include: Banach spaces, linear bounded operators and Hilbert spaces. So, only the very basic and some useful results in the scope of these concepts. I'll aim for brevity and clarity. 

**Prerequisites:** Knowledge about vector spaces. Cauchy sequences.  

### *Normed spaces* 
One can arrive at Banach spaces by imposing more structure into the general notion of a vector space. To do so, we may begin by equipping the space with a very neat function: *a norm*. 

**Definition:** Consider some vector space $V$ over the scalar field $\mathbb{K}$. A norm is a function $||\cdot||:V \to \mathbb{R}^+_0$ with the following properties:
1) Positivity: $||v|| = 0 \Leftrightarrow v=0$ for all $v\in V$
2) Homogeneity: $||\alpha v|| = |\alpha|\cdot ||v||$ for all $\alpha \in \mathbb{K}$ and $v\in V$
3) Triangle inequality: $||v + w ||\leq ||v|| + ||w||$ for all $v,w \in V$ 

*Remark:* Continuity of norm?

Intuitively, a norm is simply a measure of the magnitude of a vector, i.e. an element of the vector space. More importantly, a norm allows us to relate two vectors via a *metric*, i.e. a distance function. 

**Definition:** Let $V$ be some vector space. A *metric* will be a map $d: V\times V \to \mathbb{R}_0^+$ with the following properties:
1) Positivity: $d(v,u)>0$ for $u\neq v\in V$ and $d(u,v)=0 \Leftrightarrow u=v$
2) Symmetry: $d(u,v) = d(v,u)$ for all $u,v \in V$
3) Triangle inequality: $d(u,w) \leq d(u,v) + d(v,w)$ for all $u,v,w\in V$

**Definition:** Let $(V,||\cdot||)$ be a vector space equipped with a norm. We say it is a *normed space*. 

*Example:* The usual Euclidean space $\mathbb{R}^n$ with the $2-$norm, i.e. the norm given by $||x||_2 = \sqrt{\sum_{i=1}^n x_i^2}$. 

**Remark:** The same vector space can have different norms. A quick search on Wikipedia about Euclidean space will confirm this xD. 

Anyways, now we have a normed space! Which, in its turn, is a metric space. More structure, more possibilities... Observe that we now can make rigorous the notion of closeness. And, if one talks about closeness between elements of a vector space, one inevitably ends up talking about convergence of sequences. 

**Definition:** Consider some normed space $(V,||\cdot ||)$ and a sequence of elements $\{v_n\}_{n\in \mathbb{N}}$ in $V$. We say that $v_n$ converges to $v$, and denote it by $v_n\to v$ if and only if $||v-v_n|| \to 0$. 

A rather reasonable definition if I may say so. 

### *Banach spaces*

We are now missing one structure element in order to get a Banach space. 

**Definition:** Consider some normed space $(V,||\cdot||)$. We say that $V$ is a complete normed space if and only if all Cauchy sequences are convergent sequences. More precisely, the existence of a sequence $(x_n)_{n\in \mathbb{N}}$ such that $$\lim_{n,m \to \infty} ||x_n-x_m|| =0$$ implies the existence of an $x\in X$, such that $x_n \to x$ with respect to $||\cdot||$. A complete normed space is said to be a *Banach space*. 

*Examples:*
1) Euclidean spaces. On $\mathbb{R}^n$, consider the norm $||x||_2 = \sqrt{\sum_{i=1}^n x_i^2}$. 
2) Sequence spaces. The space $l^p(\mathbb{R})$ consists of all sequences $x = (x_n)_{n\in \mathbb{N}}$ taking values in $\mathbb{R}$ such that $||x||_p = \Big(\sum_{n=1}^\infty |x_n|^p \Big)^{1/p}<\infty$. 
3) Space of continuous functions. Consider some compact topological space. Then, the set of continuous functions $f:K \to \mathbb{R}$ with norm given by $||f||_\infty = \sup_{x\in K}|f(x)|$ is a Banach space. 
4) Space of integrable functions. For $1 \leq p<\infty$, the space $L^p(\Omega)$ consisting of all measurable functions $f:\Omega \to \mathbb{R}$ such that $||f||_p = \Big(\int_\Omega |f|^p d\mu \Big)^{1/p}$ is a Banach space. 

It is also convenient to know the following characterizations of Banach spaces and subspaces. 

**Theorem:** Consider some normed space $(X,||\cdot||)$. Then, $X$ is a Banach space if and only if every absolutely convergent sum in $X$ is convergent in $X$, i.e. $$\sum_{n\geq 1} ||x_n|| <\infty \implies \exists \ x\in X: \sum_{n\geq 1} x_n =x$$ *proof:*

**Theorem:** Consider some normed space $(X,||\cdot||)$ and a subspace $Y\subset X$. Then, $Y$ is a Banach space with respect to the norm inherited from $X$ if and only if $Y$ is a closed subspace. 

### *Linear Operators*
As it is often the case in Mathematics, now that we have a class of spaces with a reasonable structure, i.e. normed spaces and, in particular, Banach spaces, we can concern ourselves with mappings between these spaces. 

**Definition:** Consider two normed spaces $X$ and $Y$. The map $T:X\to Y$ is said to be a linear bounded operator if it is linear, i.e. $$T(\alpha x_1 + \beta x_2) = \alpha T(x_1) + \beta T(x_2)$$ for all $x_1,x_2\in X$ and scalars $\alpha,\beta$, and if there is a finite constant $C>0$ such that $$||Tx||\leq C||x||, \quad \forall x\in X$$ The infimum of all admissible constants $C$ is itself admissible and is given by $$\sup_{x\in X,x\neq0}\frac{||Tx||}{||x||}$$ This number is said to be the norm of the operator $T$ and is denoted by $||T||$. 

*Observation:* In the characterisation of boundedness, notice that the norm on the RHS of the inequality corresponds to the norm of $X$, whereas the norm on the LHS of the inequality corresponds to the norm of $Y$! 

It is not hard to come up with reasons why boundedness is a desirable property for an operator. To begin with, any bounded operator will be continuous, and continuity is always welcomed. 

**Proposition:** Consider two normed spaces $X$ and $Y$. The following assertions are equivalent:
1) The linear operator $T:X \to Y$ is bounded.
2) The linear operator $T:X \to Y$ is continuous.
3) The linear operator $T:X \to Y$ is continuous at a given point $x_0 \in X$. 







