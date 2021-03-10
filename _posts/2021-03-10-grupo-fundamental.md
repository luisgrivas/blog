---
layout: post
title: "El grupo fundamental"
date: 2021-03-01 11:00:00
categories: posts
tags: topologia, topologia-algebraica
---



![](https://upload.wikimedia.org/wikipedia/commons/a/a4/Fundamental_group_torus2.png)

---

**Definición.** Sea $X$ un espacio. Decimos que un **camino** en $X$ es un mapeo continuo $f: I \rightarrow X$. Los puntos $p = f(0)$ y $q = f(1)$ se les llaman **punto inicial** y **punto final** respectivamente. 



**Definición.** Sean $X$ y $Y$ espacios topológicos y sea $A \subset X$. Una [homotopía](https://www.luisgrivas.com/blog/posts/2021/02/28/homotopia.html) $H$ entre mapeos $f, g: X \rightarrow Y$ es **estacionaria** en $A$ si 
$$
H(x, t) = f(x) \ \ \ \ \text{para todo } x\in A, t\in I. 
$$
Si existe tal homotopía deficmos que $f$ y $g$ son **homotópicas relativas con** $A$ y $H$ es también llamada **homotopía relativa con** $A$.

**Definición.** Sean $f$ y $g$  caminos en $X$. Una **homotopía de caminos** de $f$ a $g$ es una homotopía estacionaria en el conjunto $\{0, 1\} \subset I$. Si existe una homotopía de caminos entre $f$ y $g$ decimos que son **homotópicos por caminos** y escribimos $f \sim g$. 

Siendo específicos, si $f$ y $g$ son caminos de $p$ a $q$, estos son homotópicos por caminos si existe una función continua $H: I \times I \rightarrow X$ tal que
$$
\begin{eqnarray}
H(s, 0) &=& f(s) \ \ \ & \forall s\in I,\\
H(s, 1) &=& g(s) \ \ \ & \forall s \in I,\\
H(0, t) &=& p \ \ \ & \forall t \in I,\\
H(1, t) &=& q \ \ \ & \forall t \in I.
\end{eqnarray}
$$


**Teorema.** Sea $X$ un espacio topológico. Para cualesquiera puntos $p, q\in X$, la homotopía de caminos es una relación de equivalencia en el conjunto de caminos en $X$ de $p$ a $q$. 

**Definición.** Un lazo en un espacio $X$ es un camino $f$ en $X$ tal que $f(0) = f(1)$. Al punto $p = f(0)$ le decimos **punto base** de $f$ y decimos que el lazo **está basado en** $p$. El conjunto de todos los lazos basados en un punto $p$ lo denotamos como $\Omega(X, p)$. 

**Definición.** Una reparametrización de un camino $f: I \rightarrow X$ es un camino de la forma $f \circ \phi$ donde $\phi: I \rightarrow I$ es un mapeo continuo que fija a $0$ y a $1$.

**Proposición.** Cualquier reparametrización de un camino $f$ es homotópico por caminos a $f$.

**Definición.** El Teorema (tal) establece que la homotopía por caminos es una relación de equivalencia en el conjunto $\Omega(X, p)$. Al conjunto de clases de equivalencia de $\Omega(X, p)$ lo denotaremos por $\pi_1(X, p)$ y lo llamamos como **el grupo fundamental de** $X$ **basado en ** $p$.

