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

Este problema es interesante ya que establece una clasificación completa de mapeos continuos del toro en el toro, salvo homotopía. En primer lugar, recordemos que $\pi_1(T^2, z_0) = \pi_1(\mathbb S^1 \times \mathbb S^1, z_0) = \langle [\omega_1][\omega_2]\rangle$, donde $\omega_i: I \to \mathbb S^1  \times \mathbb S^1$ ($i = 1, 2$) son mapeos definidos como 


$$
\omega_1(t) = (e^{2 \pi i t}, 1), \\
\omega_2(t) = (1, e^{2 \pi i t}).
$$


