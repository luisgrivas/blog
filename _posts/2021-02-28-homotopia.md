---
layout: post
title: "Homotopía"
date: 2021-02-28 12:00:00
categories: posts
tags: [topologia, topologia-algebraica]
---

En lo siguiente, $X, Y$ y $Z$ son espacios topológicos. Denotamos al intervalo $[0, 1]$ por $I$. Todos los mapeos considerados son continuos.

**Definición.** Una **homotopía** de mapeos de $X$ en $Y$ es un mapeo $F: X \times I \rightarrow Y$.

**Definición.** Dos mapeos $f, g: X \rightarrow Y$ son **homotópicos** si existe una homotopía $F: X \times I \rightarrow Y$ tal que $F(x, 0) = f(x)$ y $F(x, 1) = g(x)$ para toda $x \in X$. Si dos mapeos $f$ y $g$ son homotópicos escribimos $f \simeq g$. 

**Proposición 1.** La relación $f$ es homotópico a $g$ es una relación de equivalencia entre todos los mapeos de $X$ en $Y$.

*Demostración:* Sea $f: X \rightarrow Y$ un mapeo. Entonces $F(x, t) = f(x)$ es una homotopía entre $f$ y $f$. Por tanto $f \simeq f$.

Si $f \simeq g$, sea $H$ la homotopía entre $f$ y $g$. Entonces $F(x, t) = H(x, 1- t)$ es una homotopía entre $g$ y $f$.

Si $f \simeq g$ y $g \simeq h$, sea $F$ la homotopía entre $f$ y $g$ y sea $G$ la homotopía entre $g$ y $h$. Entonces la función
$$
H(x, t) := \cases{F(x, 2t) \ \text{ si } t\in [0, 1/2] \\  G(x, 2t-1) \ \text{ si } t \in [1/2, 1],}
$$
es una homotopía entre $f$ y $h$: es claro que $H(x, 0) = F(x, 0) = f(x)$ y $H(x, 1) = G(x, 1) = h(x)$ para toda $x \in X$. Para ver que es continua, véanse las siguientes definiciones y lemas. $\blacksquare$

**Nota:** A las clases de homotopía de funciones continuas de $X$ en $Y$ lo denotaremos por $[X, Y]$.

**Definición.** Una familia $\{A_\alpha: \alpha \in \mathcal{A} \}$ de conjuntos de $X$ es **nbd-finite**, si cada punto de $X$ tiene una vecindad $V$ tal que $V \cap A_\alpha \neq $ para a lo más un número finito de índices $\alpha$.

**Lema.** Sea  $\{A_\alpha: \alpha \in \mathcal{A} \}$ una familia de conjuntos que cubren a $X$. Supóngase que (a) todos los subconjuntos $A_\alpha$ son abiertos o (b), todos son cerrados y forman una familia nbd-finite. Entonces $B$ es abierto (o cerrado) si y solo si todo $B \cap A_\alpha$ es abierto (o cerrado) en $A_\alpha$.

*Demostración:* Caso (a) $(\Rightarrow)$ Si $B$ es abierto, entonces $B\cap A_\alpha$ es abierto por definición de la topología relativa de $A_\alpha$. 

Caso (a) $(\Leftarrow)$ Si $B \cap A_\alpha$ es abierto en $A_\alpha$ para toda $\alpha$, entonces $B = \bigcup_\alpha B \cap A_\alpha = \bigcup_\alpha V_\alpha \cap A_\alpha$, donde $V_\alpha$ es un abierto en $X$ para toda $\alpha$. Esto muestra que $B$ es abierto en $X$.

Caso (b) $(\Rightarrow)$. Si $B$ es abierto, entonces $B\cap A_\alpha$ es abierto por definición de la topología relativa de $A_\alpha$. 

Caso (b) $(\Leftarrow)$ Si $B \cap A_\alpha $ es abierto en $A_\alpha$ para toda $\alpha$ y $A_\alpha$ es cerrado, entonces existe ...

**Lema del pegado.** Sea  $\{A_\alpha: \alpha \in \mathcal{A} \}$ una familia de conjuntos que cubren a $X$. Supóngase que (a) todos los subconjuntos $A_\alpha$ son abiertos o (b), todos son cerrados y forman una familia nbd-finite. Para cada $\alpha \in \mathcal{A}$, sea $f_\alpha: A_\alpha \rightarrow Y$ continua y supóngase que $f_\alpha \mid_{A_\alpha \cap A_\beta} = f_\beta \mid_{A_\alpha \cap A_\beta}$ para toda $(\alpha, \beta) \in \mathcal{A} \times \mathcal{A}$. Entonces existe una extensión continua única $f: X \times Y$ tal que $f \mid_{A_\alpha} = f_\alpha$ para toda $\alpha$.

*Demostración:* sea $U$ abierto en $Y$. Entonces $f^{-1}(U) \cap A_\alpha = f_\alpha^{-1}(U)$ y por tanto es abierto en $A_\alpha$ para toda $\alpha$. Por el Lema anterior, esto implica que $f^{-1}(U)$ es abierto en $X$. 

**Corolario.** La función $H$ descrita en la proposición 1 es continua. 

**Proposición.** La homotopía se preserva mediante composición: Si $f_0, f_1: X \rightarrow Y$ y $g_0, g_1: Y \rightarrow Z$ son mapeos continuos y $f_0 \simeq f_1$ y $g_0 \simeq g_1$, entonces $g_0\circ f_0 \simeq g_1 \circ f_1.$

*Demostración:* Sea $F$ la homotopía entre $f_0$ y $f_1$ y sea $G$ la homotopía entre $g_0 $ y $g_1$. Definamos $H: X \times I \rightarrow Y$ como 

$$ H(x, t) = G(F(x, t), t).$$ 

Es claro que $H$ es una homotopía entre $g_0 \circ f_0$ y $g_1 \circ f_1$. $\blacksquare$

**Definición.** Si  $f: X \rightarrow Y$ es homotópico a un mapeo constante, entonces decimos que $f$ es **homotópicamente nulo**.

**Ejemplo.** Sea $X$ cualquier espacio y sea $D$ es disco unitario en $\mathbb{R}^2$. Entonces todo mapeo $f: X \rightarrow D$ es homotópicamente nulo. Sea $F: X \times I \rightarrow D$ un mapeo definido como $F(x, t) = f(x)(1 - t)$. 

**Ejemplo.** Generalizando el ejemplo anterior, sea $Y$ un espacio topológico *convexo* y sea $X$ cualquier espacio. Entonces todo mapeo $f: X \rightarrow Y$ es homotópicamente nulo utilizando la **homotopía de línea recta.** Sea $y_0$ un punto en $Y$ y definamos $F(x, t) = f(x)(1 - t) + t y_0$.  

**Ejemplo.** Si $X$ es convexo y $Y$ cualquier espacio, entonces cualquier mapeo $f: X \rightarrow Y$ es homotópicamente nulo. Sea $x_0 \in X$ y definamos $F(x, t): X \times I \rightarrow Y$ como $F(x, t ) = f(x(1 -t) + x_0t)$. Esta es una homotopía entre $f$ y el mapeo constante $g(x) = f(x_0)$.

**Definición.** Un espacio topológico $X$ es **contraible** si el mapeo identidad $1: X\rightarrow X$ es homotópicamente nulo.

**Ejemplo.** Todo espacio convexo es contraible. Esto es inmediato del ejemplo anterior.

**Teorema.** Si $X$ es un espacio topológico y si $f,g : X \rightarrow S^n$ son mapeos tal que para toda $x\in X$,  $f(x)$ y $g(x)$ **no son antipodales**,  entonces $f \simeq g$. En particular, un mapeo $f: X \rightarrow S^n$ no sobreyectivo es homotópicamente nulo.

*Demostración:* Definamos $F(x, t): X \times I \rightarrow S^n$ como 
$$
F(x, t) = \frac{f(x)(1 - t) + g(x)t}{\lvert f(x)(1 - t) + g(x)t \lvert}.
$$
Como $f(x)$ y $g(x)$ no son antipodales para toda $x$, $F$ es continua. Por tanto $F$ es una homotopía entre $f$ y $g$.

**Teorema.** Sea $Y$ un espacio topológico. Un mapeo $f: S^n \rightarrow Y$ es homotópicamente nulo si y solo si existe una extensión continua $F: B^{n+1} \rightarrow Y$.

*Demostración:* $(\Rightarrow)$ Sea $G(x, t)$ la homotopía entre $f$ y el mapeo constante $c$. Entonces $F: B^{n+1} \rightarrow Y$ definida como $F(x) = G(\frac{x}{\lvert x \lvert}, \lvert x \lvert)$ si $x \neq 0$ y $F(0) = c(x)$.

**DRAFT**

 **Referencias**

* Dugundji
* Lee