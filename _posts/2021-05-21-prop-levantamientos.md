---
layout: post
title: "Propiedades de levantamientos"
date: 2021-05-21 10:50:00
categories: posts
tags: topologia-algebraica
---

Cuando calculamos el grupo fundamental de $\mathbb{S}^1$ hacemos uso de diversas propiedades de la función exponencial $\omega(s) = e^{2\pi i s}$. En específico, utilizamos el hecho de que es un [mapeo cubriente](https://www.luisgrivas.com/blog/posts/2021/03/04/espacios-cubrientes.html) y su relación con los levantamientos de funciones continuas en $\mathbb S^1$.

**Definición.** Sean $q: E \rightarrow X$ un mapeo cubriente y $\phi: Y \rightarrow X$ un mapeo continuo. Un **levantamiento de** $\phi$ es un mapeo continuo $\widetilde \phi: Y \rightarrow E$ tal que $q \circ \widetilde \phi = \phi$. En otras palabras, el siguiente diagrama conmuta:

![](/blog/assets/images/levantamiento.png)

**Teorema 1 (Unicidad de levantamiento).** Sea $q: E \rightarrow X$ un mapeo cubriente. Suponga que $Y$ es conexo, $\phi: Y \rightarrow X$ es un mapeo continuo y que $\widetilde\phi_1, \widetilde\phi_2: Y \rightarrow E$ son levantamientos de $\phi$ que coinciden en un punto de $Y$. Entonces $\widetilde \phi_1$ es igual a $\widetilde \phi_2$.

*Demostración:* Sea $A = \{y\in Y: \widetilde \phi_1 (y) = \widetilde \phi_2(y) \}$. Demostraremos que $A$ es abierto y cerrado. Puesto que $Y$ es conexo y por hipótesis $A\neq \emptyset$, esto implicaría que $A = Y$.  

Primero, sea $a \in A$. Entonces $e = \widetilde \phi_1(a) = \widetilde \phi_2 (a)$. Hagamos $x = q(e) = q(e)$. Sea $U$ la componente de $q^{-1}(V)$



**Teorema 2 (Levantamiento de Homotopía).** Sea $q: E \rightarrow X$ un mapeo cubriente y sea $Y$ un espacio localmente conexo. Suponga que $\phi_0, \phi_1 : Y \rightarrow X$ son mapeos continuos, $H: Y \times I \rightarrow X$ una homotopía de $\phi_0$ en $\phi_1$ y $\widetilde \phi_0: Y \rightarrow E$ un levantamiento de $\phi_0$. Entonces existe un único levantamiento de $H$ a una homotopía $\widetilde H$ que satisface que $\widetilde H_0 = \widetilde \phi_0$. Si $H$ es estacionaria en un subconjunto $A\subset Y$, entonces también lo es $\widetilde H.$

*Demostración:*



**Corolario (Levantamiento de caminos).** Sea $q: E \rightarrow X$ un mapeo cubriente. Sea $f: I \rightarrow X$ un camino y $e \in E$ un punto en la fibra de $q$ sobre $f(0)$. Entonces existe un único levantamiento $\widetilde f : I \rightarrow E$ de $f$ tal que $\widetilde f(0) = e$.

*Demostración:*  Considere el espacio de un solo punto $Y=\{y\}$. Entonces $f$ puede verse como una homotopía entre los mapeos continuos $y \mapsto f(0) $ y $y \mapsto f(1)$. Como el mapeo $y \mapsto f(0)$ puede levantarse al mapeo $y \mapsto e$, por el Teorema 2,  $f$ se puede levantar a una única homotopía $\widetilde f$ tal que $\widetilde f(0) = $ e.



**Teorema 3 (de Monodromía).**. Sea $q: E \rightarrow X$ un mapeo cubriente. Sean $f$ y $g$ caminos en $X$ con el mismo punto inicial y mismo punto final. Sean $\widetilde f_e, \widetilde g_e$ levantamientos de $f$ y $g$ respectivamente con el mismo punto inicial $e \in E$. Entonces

(a) $\widetilde f_e \sim \widetilde g_e$ si y solo si $f \sim g$.

(b) Si $f \sim g$, entonces $\widetilde f_e(1) = \widetilde g_e (1)$.

*Demostración:* (a) Si $\widetilde f_e \sim \widetilde g_e$, entonces existe una homotopía de caminos $\widetilde H: I \times I \rightarrow E$ de $\widetilde f_e$ en $\widetilde g_e$.  Como $\widetilde f_e $ y $\widetilde g_e$ son levantamientos de $f$ y $g$ respectivamente, se tiene que $H: I \times I \rightarrow X$ definida como $H = q \circ \widetilde H$ es una homotopía de $f$ en $g$. Por el Teorema 2, existe un levantamiento de homotopía de caminos $\widetilde H$ de $H$ tal que $\widetilde H_0 = \widetilde f_e$. Como $\widetilde H_1$ es un levantamiento de $g$ con punto inicial $e$,  por el Teorema $1$,  $\widetilde H_1 = \widetilde g_e$. Por tanto $\widetilde f_e \sim \widetilde g_e$. 

(b) Finalmente, si $f \sim g$, sus levantamientos correspondientes $\widetilde f_e$ y $\widetilde g_e$ son homotópicos (por (a)), por lo que tienen el mismo punto final.



<img src="https://upload.wikimedia.org/wikipedia/commons/b/b9/Monodromy_action.svg" style="zoom:150%;" />



**Teorema de inyectividad**. Sea $q: E \rightarrow X$ un mapeo cubriente. Para cualquier punto $e \in E$, el homomorfismo inducido $q_\ast: \pi_1(E, e) \rightarrow \pi_1(X, q(e))$ es inyectivo. El subgrupo imagen $q_\ast \pi_1(E, e)$ en $\pi_1(X, x_0)$ consiste en todos los lazos basados en $q(e)$ cuyos levantamientos en $E$ que comienzan en $e$ son lazos.

*Demostración:* Sea $[f] \in Ker(q_\ast)$. Entonces $q \circ f \sim c_{q(e)}$. Por el Teorema de Monodromia, los levantamientos $\widetilde{q \circ f}$ y $\widetilde{c_{q(e)}}$ son homotópicos. Ahora bien, $f$ es el levantamiento de $q \circ f$ y $c_e$ es el levantamiento de $c_{q(e)}$. Por lo anterior, $f \sim c_e$. Por tanto, el único elemento en el kernel de $q_\ast$ es $[c_e]$.  Esto implica que $q_\ast$ es inyectivo. $\blacksquare$

Consideremos el mapeo cubriente $q_n: S^1 \to S^1$ definido como $q_n(z) = z^n$, con $n \in \mathbb N$. Sea $y_0$ un punto en el espacio cubriente y $z_0$ un punto en el espacio base. Si $[f] \in \ker {q_{n}}_\ast$, entonces $[q_n \circ f] = [c_{z_0}]$. Por lo que $c_{z_0} \sim q_n \circ f$.



Como sabemos,  $\pi_1(S^1, y_0) \simeq \langle [\omega]\rangle$, para algún lazo $\omega $ en $S^1$ basado en $y_0$. Por definición, $(q_n)_\ast ([\omega]) = [q_n \circ \omega] = q_n(\omega) = [\omega^n] = [\gamma]^n.$ Así pues, $(p_n)_\ast \pi_1(\mathcal S^1, y_0) \simeq$



**Teorema (Criterio de levantamiento)**. Sea $q: E \rightarrow X$ un mapeo cubriente. Sea $Y$ un espacio conexo y localmente conexo por caminos y sea $\phi: Y \rightarrow X$ un mapeo continuo. Dados cualesquiera dos puntos $y_0\in Y$ y $e_0 \in E$ tales que $q(e_0) = \phi(y_0)$, el mapeo $\phi$ tiene un levantamiento $\widetilde{\phi}: Y \rightarrow E$ satisfaciendo que $\widetilde{\phi}(y_0) = e_0$ si y solo si el subgrupo $\phi_\ast \pi_1(Y, y_0)$ de $\pi_1(X, \phi(y_0))$ está contenido en $q_\ast \pi_1(E, e_0)$.

*Demostración:* Si $\widetilde \phi$ es un levantamiento de $\phi$ tal que $\widetilde \phi(y_0) = e_0$, entonces $\phi_\ast \pi_1(Y, y_0) = q_\ast \circ \widetilde \phi_\ast \pi_1(Y, y_0) \subset q_\ast \pi_1(E, e_0)$.

Definamos el mapeo $\widetilde \phi: Y \rightarrow E$  como $\widetilde \phi (y) = \widetilde{(\phi \circ f)}_{e_0}(1)$, donde $f$ es un camino entre $y_0$ y $y$. En primer lugar, es necesario demostrar que el valor de $\widetilde \phi(y)$ es independiente del camino $f$ seleccionado. Para esto, sean $f$ y $f^\prime$ dos caminos de $y_0$ en $y$. 

---

**Draft:**
