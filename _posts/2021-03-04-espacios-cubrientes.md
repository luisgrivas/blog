---
layout: post
title: "Espacios cubrientes"
date: 2021-03-04 9:00:00
categories: posts
tags: [topologia, topologia-algebraica]
---

En lo siguiente, todos los espacios en cuestión son arco-conexos y localmente arco-conexos.

**Definición.** Sean $E$, $B$ espacios topológicos. Decimos que un mapeo $p: E \to B$ es un **mapeo cubriente**, si $p$ es continuo y sobreyectivo y si para todo $x \in B$ existe una vecindad $U$ tal que $p^{-1}(U)$ es la unión de abiertos disjuntos en $E$, cada uno mapeado homeomorfamente por $p$ sobre $U$. Es decir,
$$
p^{-1}(U) = \bigsqcup_\alpha V_\alpha
$$
con $V_\alpha \in E$ y $p\mid_{V_\alpha}: V_\alpha \to U$ homeomorfismo para toda $\alpha$. En este caso, decimos que $U$ es **regular**. Al espacio $E$ lo llamamos **espacio cubriente** y al espacio $B$ le llamamos **espacio base.** Los abiertos $V_\alpha$ que son mapeados por $p$ homeomorfamente les llamamos las **hojas** de $E$ sobre $U$.

Existe una relación estrecha entre los espacios cubrientes y un espacio base y sus grupos fundamentales. Esto los discutiremos en notas posteriores. 

**Ejemplo 1.** Sean $E = \mathbb R$ y $B = \mathbb S^1$, la círcunferencia en el plano complejo. El mapeo $\omega(s) = e^{2\pi i s}$ es un mapeo cubriente. Es claro que este mapeo es continuo y sobreyectivo. Para ver que es cubriente, considere los conjuntos $X_+ := \{z \in \mathbb S^1: Re(z) > 0 \}$, $X_{-} := \{z\in \mathbb S^1: Re(z) < 0 \}$, $Y_+ := \{z\in \mathbb S^1 : Im(z) > 0\}$ y $Y_{-}:= \{z \in \mathbb S^1: Im(z) < 0 \}$. Estos forman una cubierta abierta de $B$. Además, cada uno de estos es regular. Por ejemplo, 


$$
\omega^{-1}(X_+) = \bigcup_{n\in \mathbb Z} (n -1/4, n + 1/4 ).
$$
Podemos imaginar que el mapeo $\omega$ enrolla a la recta real en forma de hélice sobre la circunferencia. 

<img src="https://upload.wikimedia.org/wikipedia/commons/5/54/Covering_map.png" style="zoom:65%;" />



**Ejemplo 2.** Sean $E = B = \mathbb S^1$ y $p_n: \mathbb S^1 \to \mathbb S^1$ el mapeo definido como $p_n(z) = z^n$ para $n \in \mathbb N$. Este es un mapeo cubriente para toda $n$. 

**Ejemplo 3.** Sea $E = \mathbb S^n$ y $B = \mathbb{RP}^n$, el espacio proyectivo real de dimensión $n$. Sea $p: E \to B$  el mapeo que asigna a cada punto $x \in \mathbb S^n$ la recta que pasa por el origen y $x$.



**Teorema.**  $p: E \rightarrow B$ y $p^\prime: E^\prime \rightarrow B^\prime$ son mapeos cubrientes, entonces $p \times p^\prime: E \times E^\prime \rightarrow B \times B,$ es un mapeo cubriente.

*Demostración:*



**Teorema.** Para todo mapeo cubriente $p: E \to B$, la cardinalidad de las fibras $p^{-1}(x)$ es la misma para todas las fibras.

*Demostración:*



**Teorema.** Sea $p: E \rightarrow B$ un mapeo cubriente. Si $B_0$ es unb subespacio de $B$, y si $E_0 = p^{-1}(B_0)$, entonces el mapeo $p_0: E_0 \rightarrow B_0$ obtenido restringiendo $p$ a $E_0$ es un mapeo cubriente.



