---
layout: post
title: "Propiedades de levantamientos"
date: 2021-05-21 10:50:00
categories: posts
tags: topologia-algebraica
---



**Definición.** Sean $q: E \rightarrow X$ un mapeo cubriente y $\phi: Y \rightarrow X$ un mapeo continuo. Un **levantamiento de** $\phi$ es un mapeo continuo $\widetilde \phi: Y \rightarrow E$ tal que $q \circ \widetilde \phi = \phi$. En otras palabras, el siguiente diagrama conmuta:

![](/blog/assets/images/levantamiento.png)

**Teorema (Unicidad de levantamiento).** Sea $q: E \rightarrow X$ un mapeo cubriente. Suponga que $Y$ es conexo, $\phi: Y \rightarrow X$ es un mapeo continuo y que $\widetilde\phi_1, \widetilde\phi_2: Y \rightarrow E$ son levantamientos de $\phi$ que coinciden en un punto de $Y$. Entonces $\widetilde \phi_1$ es igual a $\widetilde \phi_2$.

*Demostración:* Sea $A = \{y\in Y: \widetilde \phi_1 (y) = \widetilde \phi_2(y) \}$. Por hipótesis, $A$ es no vacío. Demostraremos que $A$ es abierto y cerrado. Puesto que $Y$ es conexo, esto implicaría que $A = Y$.  

Primero, sea $a \in A$. Entonces $\widetilde \phi_1(a) = \widetilde \phi_2 (a)$. Hagamos $x = q(\widetilde \phi_1(a)) = q(\widetilde \phi_2(a))$. Como $x$ está bien cubierto, existe vecindad  $U$ de $x$ y vecindad $V$ de $\widetilde \phi_1(a)$ tal que $q \mid_V$ es un homeomorfismo de $U$ sobre $V$.



**Teorema. (Levantamiento de Homotopía)** Sea $q: E \rightarrow X$ un mapeo cubriente y sea $Y$ un espacio localmente conexo. Suponga que $\phi_0, \phi_1 : Y \rightarrow X$ son mapeos continuos, $H: Y \times I \rightarrow X$ una homotopía de $\phi_0$ en $\phi_1$ y $\widetilde \phi_0: Y \rightarrow E$ un levantamiento de $\phi_0$. Entonces existe un único levantamiento de $H$ a una homotopía $\widetilde H$ que satisface que $\widetilde H_0 = \widetilde \phi_0$. Si $H$ es estacionaria en un subconjunto $A\subset Y$, entonces también lo es $\widetilde H.$





**Corolorario (Levantamiento de caminos).** Sea $q: E \rightarrow X$ un unampeo cubriente. Sea $f: I \rightarrow X$ un camino y $e \in E$ un punto en la fibra de $q$ sobre $f(0)$. Entonces existe un único levantamiento $\widetilde f : I \rightarrow E$ de $f$ tal que $\widetilde f(0) = e$.

*Demostración:*  



**Teorema. (de Monodromía)**. Sea $q: E \rightarrow X$ un mapeo cubriente. Sean $f$ y $g$ caminos en $X$ con el mismo punto inicial y mismo punto final. Sean $\widetilde f_e, \widetilde g_e$ levantamientos de $f$ y $g$ respectivamente con el mismo punto inicial $e \in E$. Entonces

(a) $\widetilde f_e \sim \widetilde g_e$ si y solo si $f \sim g$.

(b) Si $f \sim g$, entonces $\widetilde f_e(1) = \widetilde g_e (1)$.

*Demostración:*

**Teorema. (de inyectividad)**. Sea $q: E \rightarrow X$ un mapeo cubriente. Para cualquier punto $e \in E$, el homomorfismo inducido $q_\ast: \pi_1(E, e) \rightarrow \pi_1(X, q(e))$ es inyectivo.

*Demostración:*

**Teorema (Criterio de levantamiento)**. Sea $q: E \rightarrow X$ un mapeo cubriente. Sea $Y$ un espacio conexo y localmente conexo por caminos y sea $\phi: Y \rightarrow X$ un mapeo continuo. Dados cualesquiera dos puntos $y_0\in Y$ y $e_0 \in E$ tales que $q(e_0) = \phi(y_0)$, el mapeo $\phi$ tiene un levantamiento $\widetilde{\phi}: Y \rightarrow E$ satisfaciendo que $\widetilde{\phi}(y_0) = e_0$ si y solo si el subgrupo $\phi_\ast \pi_1(Y, y_0)$ de $\pi_1(X, \phi(y_0))$ está contenido en $q_\ast \pi_1(E, e_0)$.

*Demostración:* 

