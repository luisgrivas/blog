---
layout: post
title: "Clasificación homotópica de mapeos en el toro"
date: 2021-06-18 15:57:00
categories: posts
tags: homotopia, topología-algebraica
---

En el libro *Introduction to Topological Manifolds* de John M. Lee aparece el siguiente problema.

Demuestre que para todo mapeo continuo $\phi: T^2 \to T^2$, existe una matriz $D(\phi)$ de $2 \times 2$ con entradas en $\mathbb Z$ con las siguientes propiedades:

1. Dos mapeos continuos $\phi$ y $\psi$ son homotópicos si y solo si $D(\phi) = D(\psi)$.
2. $D(\psi \circ \phi)$ es igual al producto $D(\psi) D(\phi)$.
3. Para toda matriz $E$ de $2 \times 2$ con entradas en $\mathbb Z$ existe un mapeo continuo $\psi: T^2 \to T^2$ tal que $D(\phi) = E$.
4. $\phi$ es homotópico a un homeomorfismo si y solo si $D(\phi)$ es invertible sobre los enteros.

Este problema es interesante ya que establece una clasificación completa de mapeos continuos del toro en el toro, salvo homotopía. 

En primer lugar, recordemos que $\pi_1(T^2, z_0) = \pi_1(\mathbb S^1 \times \mathbb S^1, z_0) = \langle [\omega_1], [\omega_2]\rangle$, donde $\omega_1, \omega_2: I \to \mathbb S^1  \times \mathbb S^1$ son los mapeos definidos como 


$$
\omega_1(t) = (e^{2 \pi i t}, 1), \\
\omega_2(t) = (1, e^{2 \pi i t}).
$$


Si $\phi: T^2 \to T^2$ es un mapeo continuo, entonces podemos escribir $\phi(s, t) = (\phi_1(s, t), \phi_2(s, t))$ con $\phi_1, \phi_2: T^2 \to \mathbb S^1$ mapeos continuos. La composición $\phi_i \circ \omega_j$ puede ser vista como un lazo en $\mathbb S^1$. De esta manera, podemos definir el [número de enrollamiento](https://www.luisgrivas.com/blog/posts/2021/05/21/prop-levantamientos.html), $E(\phi_i \circ \omega_j)$, del mapeo $\phi_i \circ \omega_j$ para toda $i$ y $j$. Con esto, definimos la matriz asociada $D(\phi) = (a_{ij})$ al mapeo $\phi$ como 
$$
a_{ij} = E(\phi_i \circ \omega_j).
$$
Es claro que esta matriz es  $2 \times 2$ con entradas en $\mathbb Z$. Procedamos a resolver cada uno de los puntos mencionados. En lo siguiente, los mapeos $\phi, \psi: T^2 \to T^2$ son continuos.



#### Propiedad 1

Sean $\phi $ y $\psi$ con homotópicos. Entonces $\phi_i $ es homotópico a $\psi_i$ para $i = 1, 2$. Esto implica que $\phi_i \circ \omega_j$ es homotópico a $\psi_i \circ \omega_j$. Luego, los lazos satisfacen que $E(\phi_i \circ \omega_j) = E(\psi_i \circ \omega_j)$. Por tanto $D(\phi) = D(\psi)$. El converso es cierto ya que las implicaciones anteriores son bicondicionales.



#### Propiedad 2



#### Propiedad 3

Sea $A = (a_{ij})$ una matriz $2 \times 2$ con entradas en $\mathbb Z$. Observe que el mapeo $\phi: T^2 \to T^2$ definido como $\phi(s, t) = (s^{a_{11}}t^{a_{12}}, s^{a_{21}}t^{a_{22}})$ satisface lo requerido. Por ejemplo, como $\phi_1(s, t) = s^{a_{12}}t^{a_{11}}$, entonces


$$
\phi_1(\omega_1(r)) = \phi_1(e^{2\pi i r}, 1) = e^{2\pi i (a_{11} r)}, \\
\phi_1(\omega_2(r)) = \phi_1(1, e^{2\pi i r}) = e^{2\pi i (a_{12} r)}. \\
$$
De aquí, los números de enrollamiento son $E(\phi_1(\omega_1(r))) = a_{11}$ y $E(\phi_1(\omega_2(r))) = a_{12}$.



#### Propiedad 4

Suponga que $\phi$ es homotópico a un homeomorfismo $\psi$. Sea $\psi^{-1}: T^2 \to T^2 $ el inverso de $\psi$. Entonces $ D(\psi) D(\psi^{-1}) = D(\psi \circ \psi^{-1}) = D(id) = I$ y $D(\psi^{-1}) D(\psi) = D(\psi^{-1} \circ \psi) = D(id) = I$. Como $D(\phi) = D(\psi)$, lo anterior muestra que $D(\phi)$ es invertible sobre los enteros. 

Conversamente, suponga que $D(\phi)$ es invertible en $\mathbb Z$.

---

**DRAFT**