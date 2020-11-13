---
layout: post
title:  "Apuntes Seminario Amoebas 12-20"
date:   2020-11-12 17:00:00
categories: posts
tags: [teoria-de-graficas]
---



### Objetivo

A cada gráfica $G$ le vamos a asociar un grupo $S_G$. 

**Notación: **

* $[n] = \\{1, 2, \ldots, n\\}$ y $[n, m] = \\{n. n+1, \ldots, m\\}$.
* $S_n$ es el grupo simétrico sobre $n$ elementos. $\mid S_n \mid = n! $.
* $Aut(G) = $ grupo de automorfismos de $G$. Ejemplo:  $Aut(K_n) \cong S_n$.
* $V = \\{v_1, v_2, \ldots, v_n\\}$ *vértices*; $K_n = (V, {n \choose 2})$ *gráfica completa*; $G = (V, E(G) \subset {V \choose 2})$.
* $L_G = \\{ij : v_i v_j \in E(G)\\}$ (no importa el orden).



### Etiquetación

$\lambda_\sigma: V \rightarrow [n]$, definida como  $\lambda_\sigma(v_i) = \sigma(i)$.

Para cada $\sigma \in S_n$ (permutación de $[n]$), definamos $G_\sigma = (V, E(G_\sigma))$, donde $E(G_\sigma) = \\{ v_{\sigma^{-1}(i)} v_{\sigma^{-1}(j)}: ij \in L_G \\} = \\{v_i v_j: \sigma(i)\sigma(j) \in L_G\\}$.

**Observación**: $\\{\sigma \in S_n: G_\sigma = G \\} \cong Aut(G)$


### Problema

$G = (V, E)$, $V = \\{v_1, v_2, v_3, v_4\\}$, $E = \\{v_1 v_2, v_2 v_3, v_1 v_3, v_3 v_4 \\}$, $L_G = \\{12, 23, 13, 34\\}$.

Determinar $S = \\{\sigma \in S_n: G_\sigma = G \\}$.

**PENDIENTE**

### Conceptos a investigar

* Gráficas generadoras
* Encajes
* Etiquetas
* Grupo de automorfismos de $G$.

