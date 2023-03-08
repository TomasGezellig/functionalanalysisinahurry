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