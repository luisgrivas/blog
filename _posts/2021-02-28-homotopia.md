---
layout: post
title: "Homotopía"
date: 2021-02-28 12:00:00
categories: posts
tags: [topologia, topologia-algebraica]
---

![](https://upload.wikimedia.org/wikipedia/commons/2/26/Mug_and_Torus_morph.gif)

---

En lo siguiente, $X, Y$ y $Z$ son espacios topológicos. Denotamos al intervalo $[0, 1]$ por $I$. Todos los mapeos considerados son continuos.

**Definición.** Dos mapeos $f, g: X \rightarrow Y$ son **homotópicos** si existe un mapeo continuo $F: X \times I \rightarrow Y$ tal que $F(x, 0) = f(x)$ y $F(x, 1) = g(x)$ para toda $x \in X$. Si dos mapeos $f$ y $g$ son homotópicos escribimos $f \simeq g$. Decimos que el mapeo $F$ es una homotopía entre $f$ y $g$.

![](/blog/assets/images/homotopia.png)

**Ejemplo 1.** Sean $f: \mathbb{R} \rightarrow \mathbb{R}^2$ y $g: \mathbb{R} \rightarrow \mathbb{R}^2$ mapeos definidos como $f(x) = (x, x^3)$ y $g(x) = (x, x)$. Entonces el mapeo $H(x, t) = g(x)(1 - t) + f(x)t = (x, (1 - t)x + tx^3)$ es una homotopía entre $f$ y $g$.

**Ejemplo 2**. Si $X$ es un espacio topológico con un solo punto, entonces $[X, Y]$ es el conjunto de componentes conexas por caminos de $Y$. 

## Clases de homotopía

**Teorema 1.** La relación $f$ es homotópico a $g$ es una relación de equivalencia entre todos los mapeos de $X$ en $Y$. Denotamos a las clases de homotopía de mapeos continuos de $X$ en $Y$ como $[X, Y]$.

*Demostración:* Sea $f: X \rightarrow Y$ un mapeo. Entonces $F(x, t) = f(x)$ es una homotopía entre $f$ y $f$. Por tanto $f \simeq f$.

Si $f \simeq g$, sea $H$ la homotopía entre $f$ y $g$. Entonces $F(x, t) = H(x, 1- t)$ es una homotopía entre $g$ y $f$.

Si $f \simeq g$ y $g \simeq h$, sea $F$ la homotopía entre $f$ y $g$ y sea $G$ la homotopía entre $g$ y $h$. Entonces la función


$$
H(x, t) := \cases{F(x, 2t) \ \text{ si } t\in [0, 1/2] \\  G(x, 2t-1) \ \text{ si } t \in [1/2, 1],}
$$


es una homotopía entre $f$ y $h$: es claro que $H(x, 0) = F(x, 0) = f(x)$ y $H(x, 1) = G(x, 1) = h(x)$ para toda $x \in X$. Para demostrar que es continua, véanse los resultados de la sección Lema del pegado. $\blacksquare$

**Teorema 2.** La homotopía se preserva mediante composición: Si $f_0, f_1: X \rightarrow Y$ y $g_0, g_1: Y \rightarrow Z$ son mapeos continuos y $f_0 \simeq f_1$ y $g_0 \simeq g_1$, entonces $g_0\circ f_0 \simeq g_1 \circ f_1.$

*Demostración:* Sea $F$ la homotopía entre $f_0$ y $f_1$ y sea $G$ la homotopía entre $g_0 $ y $g_1$. Definamos $H: X \times I \rightarrow Y$ como 


$$
H(x, t) = G(F(x, t), t).
$$


Es claro que $H$ es una homotopía entre $g_0 \circ f_0$ y $g_1 \circ f_1$. $\blacksquare$

**Teorema**. Si $f, g: X \rightarrow Y$ son homotópicas, entonces 
$$
f \mid_A \simeq g \mid_A,
$$
para cualquier $A \subset X$.

*Demostración:*

**Teorema.**  $f,g: X \rightarrow \Pi_\alpha Y_\alpha$ son homotópicas si y solo si $\pi_\alpha \circ f \simeq \pi_\alpha \circ g $ para toda $\alpha$.

*Demostración:*

## Lema del pegado

**Definición.** Una familia $\{A_\alpha: \alpha \in \mathcal{A} \}$ de conjuntos de $X$ es **localmente finita**, si cada punto de $X$ tiene una vecindad $V$ tal que $V \cap A_\alpha \neq $ para a lo más un número finito de índices $\alpha$.

**Lema.** Sea  $\{A_\alpha: \alpha \in \mathcal{A} \}$ una familia de conjuntos que cubren a $X$. Supóngase que (a) todos los subconjuntos $A_\alpha$ son abiertos o (b), todos son cerrados y forman una familia localmente finita. Entonces $B$ es abierto (o cerrado) si y solo si todo $B \cap A_\alpha$ es abierto (o cerrado) en $A_\alpha$.

*Demostración:* Caso (a) $(\Rightarrow)$ Si $B$ es abierto, entonces $B\cap A_\alpha$ es abierto por definición de la topología relativa de $A_\alpha$. 

Caso (a) $(\Leftarrow)$ Si $B \cap A_\alpha$ es abierto en $A_\alpha$ para toda $\alpha$, entonces $B = \bigcup_\alpha B \cap A_\alpha = \bigcup_\alpha V_\alpha \cap A_\alpha$, donde $V_\alpha$ es un abierto en $X$ para toda $\alpha$. Esto muestra que $B$ es abierto en $X$.

Caso (b) $(\Rightarrow)$. Si $B$ es abierto, entonces $B\cap A_\alpha$ es abierto por definición de la topología relativa de $A_\alpha$. 

Caso (b) $(\Leftarrow)$ Si $B \cap A_\alpha $ es abierto en $A_\alpha$ para toda $\alpha$ y $A_\alpha$ es cerrado, entonces existe ...

**Lema del pegado.** Sea  $\{A_\alpha: \alpha \in \mathcal{A} \}$ una familia de conjuntos que cubren a $X$. Supóngase que (a) todos los subconjuntos $A_\alpha$ son abiertos o (b), todos son cerrados y forman una familia nbd-finite. Para cada $\alpha \in \mathcal{A}$, sea $f_\alpha: A_\alpha \rightarrow Y$ continua y supóngase que $f_\alpha \mid_{A_\alpha \cap A_\beta} = f_\beta \mid_{A_\alpha \cap A_\beta}$ para toda $(\alpha, \beta) \in \mathcal{A} \times \mathcal{A}$. Entonces existe una extensión continua única $f: X \times Y$ tal que $f \mid_{A_\alpha} = f_\alpha$ para toda $\alpha$.

*Demostración:* sea $U$ abierto en $Y$. Entonces $f^{-1}(U) \cap A_\alpha = f_\alpha^{-1}(U)$ y por tanto es abierto en $A_\alpha$ para toda $\alpha$. Por el Lema anterior, esto implica que $f^{-1}(U)$ es abierto en $X$. 

**Corolario.** La función $H$ descrita en el Teorema 1 es continua. 

## Espacios contraibles

**Definición.** Si  $f: X \rightarrow Y$ es homotópico a un mapeo constante, entonces decimos que $f$ es **homotópicamente nulo**.

**Ejemplo.** Sea $X$ cualquier espacio y sea $D$ es disco unitario en $\mathbb{R}^2$. Entonces todo mapeo $f: X \rightarrow D$ es homotópicamente nulo. Considere el mapeo $F: X \times I \rightarrow D$  definido como $F(x, t) = f(x)(1 - t)$. Esto muestra que $f$ es homotópico al mapeo constante $c(x) = 0$.

**Ejemplo.** Generalizando el ejemplo anterior, sea $Y$ un espacio topológico *convexo* y sea $X$ cualquier espacio. Entonces todo mapeo $f: X \rightarrow Y$ es homotópicamente nulo utilizando la **homotopía de línea recta.** Sea $y_0$ un punto en $Y$ y definamos $F(x, t) = f(x)(1 - t) + t y_0$.  

**Ejemplo.** Si $X$ es convexo y $Y$ cualquier espacio, entonces cualquier mapeo $f: X \rightarrow Y$ es homotópicamente nulo. Sea $x_0 \in X$ y definamos $F(x, t): X \times I \rightarrow Y$ como $F(x, t ) = f(x(1 -t) + x_0t)$. Esta es una homotopía entre $f$ y el mapeo constante $g(x) = f(x_0)$.

**Definición.** Un espacio topológico $X$ es **contraible** si el mapeo identidad $1: X\rightarrow X$ es homotópicamente nulo.

**Ejemplo.** Todo espacio convexo es contraible. Esto es inmediato del ejemplo anterior.

**Teorema.** Si $X$ es un espacio topológico y si $f,g : X \rightarrow S^n$ son mapeos tal que para toda $x\in X$,  $f(x)$ y $g(x)$ **no son antipodales**,  entonces $f \simeq g$. En particular, un mapeo $f: X \rightarrow S^n$ no sobreyectivo es homotópicamente nulo.

*Demostración:* Definamos $F(x, t): X \times I \rightarrow S^n$ como 
$$
F(x, t) = \frac{f(x)(1 - t) + g(x)t}{\lvert f(x)(1 - t) + g(x)t \lvert}.
$$


Como $f(x)$ y $g(x)$ no son antipodales para toda $x$, $F$ es continua. Por tanto $F$ es una homotopía entre $f$ y $g$. $\blacksquare$

**Teorema.** Sea $Y$ un espacio topológico. Un mapeo $f: S^n \rightarrow Y$ es homotópicamente nulo si y solo si existe una extensión continua $F: B^{n+1} \rightarrow Y$.

*Demostración:* $(\Rightarrow)$ Sea $G(x, t)$ la homotopía entre $f$ y el mapeo constante $c: S^n \rightarrow \{y_0\} \subset Y$. Entonces $F: B^{n+1} \rightarrow Y$ definida como $F(x) = G(\frac{x}{\lvert x \lvert}, \lvert x \lvert)$ si $x \neq 0$ y $F(0) = c(x) = y_0$... ?

Recordemos que el **cono**  $CX$ de un espacio $X$ es el [espacio cociente](https://www.luisgrivas.com/blog/posts/2021/01/18/topologia-cociente.html) como $X \times I /\sim$ donde $\sim$ es la relación de equivalencia en $X \times I$ definida como $(x, 1) \sim (x', 1)$ para toda $x, x^\prime \in X$.

**Teorema.** Sea $X$ un espacio, y sea $CX$ el cono sobre $X$. Un mapeo $f: X \rightarrow Y$ es homotópicamente nulo si y solo si $f$ tiene una extensión continua 
$$
F: CX \rightarrow Y.
$$
*Demostración:* Sea $q: X \times I \rightarrow CX$ el mapeo cociente. Es claro que $X$ y $X \times \{0\}$ son homeomorfos. Además, $q\mid_{X \times \{0\}}$ es un. homeomorfismo entre $X \times \{0\}$ y $q(X \times \{0\})$; esto muestra que $X$ y $q(X \times \{0\})$ son homeomorfomos. $(\Leftarrow)$ Si $F: CX \rightarrow Y$ es una extensión continua de $f$, entonces el mapeo $H: X \times I \rightarrow Y$ definido como $H(x, t) = F(q(x, t))$ es una homotopía entre $f$ y una contante $F(q(x, 1))$. Por tanto $f$ es homotópicamente nula. 

$(\Rightarrow)$. Suponga $f$ es homotópica a una función constante $c: X \rightarrow \{y_0\} \subset Y$ y sea $H$ la homotopía entre ellas. Entonces $H \circ q^{-1}$ *es una extensión continua de * $f$. ? $\blacksquare$ 

**Definición.** Dos espacios $X,Y$ son **homotópicamente equivalentes** ($X \simeq Y$) si existen mapeos continuos $f: X \rightarrow Y$ y $g: Y \rightarrow X$ tales que $f\circ g \simeq 1_Y$ y $g \circ f \simeq 1_X$. Dos espacios homotópicamente equivalentes se dice que son del mismo **tipo de homotopía**.

**Ejemplo.** Consideremos el espacio topológico $X = \mathbb{R}^n - \{0\}$. Sea $i: S^{n-1} \rightarrow X$ el mapeo inclusión y sea $r: X \rightarrow S^{n-1}$ el mapeo definido como $r(x) = \frac{x}{\lvert x \lvert}$. Observe que $r \circ i = 1_{S^{n-1}}$ e $i \circ r = r \simeq 1_X$, ya que el mapeo $H: X \times I \rightarrow S^{n-1}$ definido como $H(x, t) = tx + (1 - t) \frac{x}{\lvert x \lvert}$ es una homotopía entre $r$ y $1_X$. Por tanto $S^{n-1}$ y $X$ son del mismo tipo de homotopía. 

**Observación:** Es claro que la relación $X$ homotópicamente equivalente a $Y$ es una relación de equivalencia en el conjunto de espacios topológicos.  Dos espacios homeomorfos pertenecen a la misma clase de homotopía: si $\phi: X \rightarrow Y$ es un homeomorfismo, entonces $\phi \circ \phi^{-1} = 1_X$ y $\phi^{-1} \circ \phi = 1_Y$.

**Teorema.** Un espacio $X$ es contraible si y solo si $X$ es del mismo tipo de homotopía que el espacio de un solo punto. 

*Demostración:* $(\Rightarrow)$ Si $X$ es contraible, el mapeo identidad $1: X \rightarrow X$ es homotópico a un mapeo constante $c: X \rightarrow \{x_0\} \subset X$. Consideremos al espacio $Y = \{x_0\}$ y al mapeo $g: Y \rightarrow X$ definido como $g(x) = x_0$. Entonces, $g \circ c = c \simeq 1_X$ y $c \circ g = 1_{Y} \simeq 1_{Y}$. Esto muestra que $X$ es del mismo tipo de homotopía que el espacio de un solo punto.

$(\Leftarrow)$ Suponga que $X \simeq Y= \{y_0\}$, es decir, existen mapeos $f: X \rightarrow Y $ y $g: Y \rightarrow X$ tales que $f \circ g \simeq  1_Y$ y $g \circ f \simeq 1_X$. Sea $c: X \rightarrow \{g(y)\}$ el mapeo constante. Entonces $c = g \circ f \simeq 1_X$, lo que muestra que $X$ es contraible. $\blacksquare$

**Ejemplo.** Como $\mathbb{R}^n$ es convexo, este es contraible. Luego este es del mismo tipo de homotopía que el espacio de un solo punto. Asi pues, visto desde el punto de vista homotópico, el espacio $\mathbb{R}^n$ es trivial.

## Retractos

**Definición.** Un subconjunto $A$ de un espacio $X$ es un **retracto** de $X$ si existe un mapeo continuo $r: X \rightarrow X$ llamado **retracción** tal que $r(X) = A$ y $r(a) = a$ para toda $a \in A$.

De manera equivalente, decimos que $A \subset X$ es un retracto de $X$ si la función identidad $1: A \rightarrow A$ puede ser extendida a una función continua $r: X \rightarrow A$.

**Ejemplo.** En el Ejemplo (tal), la función $r: X \rightarrow S^{n-1}$ es una retracción. Por lo que $S^{n-1}$ es un retracto de $X$. 

*Intuitivamente hablando, si $A \subset X$ es un retracto, todo agujero de $A$ es un agujero de $X$.*

**Proposición.** Si $X$ es Hausdorff y $A \subset X$ es un retracto de $X$, entonces $A$ es cerrado en $X$.





**DRAFT**

---

 **Referencias**

* Dugundji
* Lee