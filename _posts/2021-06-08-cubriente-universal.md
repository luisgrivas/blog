---
layout: post
title: "Cubriente Universal"
date: 2021-06-08 12:00:00
categories: posts
tags: topologia-algebraica
---

Recordemos el [teorema de inyectividad](https://www.luisgrivas.com/blog/posts/2021/05/21/prop-levantamientos.html) de espacios cubrientes. 

**Teorema de Inyectividad**. Sea $p: E \rightarrow X$ un mapeo cubriente. Para cualquier punto $e \in E$, el homomorfismo inducido $p_\ast: \pi_1(E, e) \rightarrow \pi_1(X, q(e))$ es inyectivo. 

Este teorema nos dice que podemos asociar a cada cubriente $p: E \to X$ un subgrupo del grupo fundamental de $X$. Es natural preguntarse si esta asociación es sobreyectiva, es decir, si podemos asociar a todo subgrupo $H$ de $\pi_1(X, x_0)$, un espacio cubriente $p: E \to X$, de tal manera que $p_\ast \pi_1(E, e) = H$. En estas notas trataremos sobre un caso particular: asociar al subgrupo trivial un espacio cubriente. 

En primer lugar, si este espacio cubriente $p: E \to X$ existiera, tendríamos que $p_\ast \pi_1(E, e) = 0$. Pero por el Teorema de Inyectividad, $p_\ast$ es inyectivo, por lo que $\pi_1(E, e) = 0$. Así pues, $E$ es simplemente conexo. Si $p: E \to X$ es un mapeo cubriente y $E$ es simplemente conexo, diremos que $E$ es **el cubriente universal** de $X$. Este nombre surge del hecho de que $E$ cubre a cualquier otro espacio cubriente de $X$ (esto lo veremos en notas posteriores).

Como cabe esparar, no todo espacio $X$ tiene un cubriente universal. Es necesario imponer ciertas condiciones al espacio $X$ para asegurar su existencia.

**Definición:** Decimos que un espacio $X$ es **localmente simplemente conexo** si tiene una base de abiertos simplemente conexos. 

**Teorema (Existencia del Espacio Cubriente Universal).** Todo espacio topológico arco-conexo, localmente arco-conexo y localmente simplemente conexo tiene un espacio cubriente universal. 

*Demostración:* Sea $X$ un espacio que satisface las hipótesis del teorema y sea $x_0 \in X $ un punto base. Definamos $\widetilde{X}$ como el conjunto de todas las clases de caminos en $X$ que comienzan en $x_0$. Sea $p: \widetilde{X} \rightarrow X$ el mapeo definido como $p([f]) = f(1)$. Demostraremos que $q$ es un mapeo cubriente y que $\widetilde{X}$ es simplemente conexo.

El primer paso consiste definir una topología para $\widetilde X$ a partir de una base.  Para cada $[f] \in \widetilde{X}$ y para cada abierto simplemente conexo $U \subset X$ que contenga a $f(1)$, definamos el conjunto $U_f$ como 



$$
U_f = \{[f\cdot a]: a \text{ es un camino en } U \text{ que comienza en } f(1)\}.
$$

Demostraremos que $\mathcal B$, el conjunto de todos los $U_f$, es una base para una topología. Sean $U_f$, $V_g$ elementos de $\mathcal B$ y sea $[h] \in \widetilde X$ en $U_f \cap V_g$. Entonces $h \sim f \cdot a  \sim g\cdot b$, donde $a$ y $b$ son caminos en $U$ y $V$ que comienzan en $f(1)$ y $g(1)$ respectivamente. Por hipótesis, existe una vecindad de $h(1)$ simplemente conexa contenida en $U \cap V$. Sea $c$ un camino en $W$ que comienza en $h(1)$. Como $W \subset U$ y $h \sim f \cdot a$ , entonces $h \cdot c \sim f \cdot a \cdot c$, lo que implica que $[h \cdot c] \in U_f$. De manera similar, $[h\cdot c] \in V_g$. Por tanto, $W_h \subset U_f \cap V_g$. Esto muestra que $\mathcal B$ es una base para una topología de $\widetilde X$.

El siguiente paso consiste en demostrar que $\widetilde X$ es conexo por trayectorias (de esta manera podremos definir su grupo fundamental). Sea $[f] \in \widetilde X$ un elemento arbitrario y sea $[c_{x_0}]\in \widetilde X$ la clase del lazo constante en $x_0$. Para toda $t \in [0, 1]$, definamos el mapeo $f_t : I \to X$ como 



$$
f_t(s) = f(ts).
$$
Dado que $f_t(0) = f(0) = x_0$ y $f_t(1) = f(t)$, $f_t$ es un camino de $x_0$ hasta $f(t)$. Definamos $\widetilde f: I \to \widetilde X$ como 


$$
\widetilde f(t) = [f_t].
$$
Observe que $\widetilde f(0) = [c_{x_0}]$ y $\widetilde f(1) = [f ]$. Por lo que si demostramos que $\widetilde f$ es continua, implica que $\widetilde f$  es un camino de $[c_{x_0}]$ hasta $[f]$. Para esto, sea $t_0 \in I $  y sea $U_h$ un elemento básico tal que $\widetilde f(t_0) \in U_h$.  Por definición, esto implica que $f_{t_0} \sim h \cdot a$, para algún camino $a$ en $U$ que comienza en $h(1)$. 

...

**Ejemplo 1.** Es claro que el espacio $\mathbb S^1$ es arco-conexo y localmente arco-conexo. Una base para la topología de $\mathbb S^1$ (que es la de subespacio considerando a $\mathbb S^1$ como subconjunto de $\mathbb C$) es el conjunto de todos los arcos abiertos. Estos son homeomorfos al conjunto $\mathbb R$,  que es simplemente conexo. Por tanto, $\mathbb S^1$ es localmente simplemente conexo. Así pues, el teorema anterior nos asegura que $\mathbb S^1$ tiene un cubriente universal. Recordando las [notas sobre mapeos cubrientes](https://www.luisgrivas.com/blog/posts/2021/03/04/espacios-cubrientes.html), el mapeo $\omega: \mathbb R \to \mathbb S^1$ es un mapeo cubriente. Como $\mathbb R$ es simplemente conexo, este es el cubriente universal de $\mathbb S^1$.

**Ejemplo 2.** El mapeo $\omega \times \omega: \mathbb R^2 \to T$ es un mapeo cubriente. El espacio $\mathbb R^2 $es simplemente conexo, por lo que es el cubriente universal del toro $T$.

**Ejemplo 3.** En las mismas notas, se demuestra que el mapeo $\mathbb S^n \to \mathbb{RP}^n$ que asigna a cada punto $z \in \mathbb S^n$ la recta que pasa por el origen y $x$ es un mapeo cubriente. Para $n > 1$, $\mathbb S^n$ es simplemente conexo, por lo que es el cubriente universal del espacio proyectivo real de dimensión $n$.

**Ejemplo 4.** Consideremos el espacio $\mathbb S^1 \vee \mathbb S^1$. 

![](https://upload.wikimedia.org/wikipedia/commons/6/65/Wedge_of_Two_Circles.png)

El cubriente universal de $\mathbb S^1 \vee \mathbb S^1$ se aprecia en la figura de abajo.

<img src="/blog/assets/images/ucwedge.png" style="zoom:60%;" /> 

---

**DRAFT**



