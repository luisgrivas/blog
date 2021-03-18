---
layout: post
title: "Problemas Royden Capítulo 6: Espacios de Banach"
date: 2021-01-19
categories: posts
tags: analisis-real
---

**Problema 1.** Demuester que $\parallel f + g \parallel_\infty \leq \parallel f \parallel_\infty + \parallel g \parallel_\infty$.

*Demostración.* Observe que $\lvert f \lvert \leq \parallel f \parallel_\infty $ y  $\lvert g \lvert \leq \parallel g \parallel_\infty $, entonces  $\lvert f + g \lvert \leq \lvert f \lvert + \lvert g \lvert \leq \parallel f \parallel_\infty + \parallel g \parallel_\infty$. Luego $\parallel f + g \parallel_\infty \leq \parallel f \parallel_\infty + \parallel g \parallel_\infty$. $\blacksquare$ 

**Problema 2.** Sea $f$ una función medible acotada definida en $[0, 1]$. Entonces $\lim_{p \to \infty } \parallel f \parallel_p  = \parallel f \parallel_\infty$.

*Demostración.* Sea $\epsilon > 0$. 

**Problema 3**. Demuestre que $\parallel f + g \parallel_1 \leq \parallel f \parallel_1 + \parallel g \parallel_1$.

*Demostración.* Se tiene que $\lvert f + g \lvert \leq \lvert f \lvert + \lvert g \lvert $. Integrando en ambos lados de la desigualdad y aplicando linealidad se obtiene el resultado.

**Problema 4.** Si $f \in L^1$ y $g \in L^\infty$, entonces $\int \lvert fg \lvert \leq \parallel f \parallel_1 \cdot \parallel g \parallel_\infty$.

*Demostración.* El resultado se sigue integrando en la desigualdad $\lvert fg \lvert = \lvert f \lvert\cdot \lvert g \lvert \leq \lvert f \lvert \cdot \parallel g \parallel_\infty$ y aplicando linealidad. 

**Problema 5.** Para $1 \leq p \leq \infty$, denotemos por $l^p$ el espacio de todas las sucesiones $\langle \xi_\nu \rangle_{\nu=1}^\infty$ tales que $\sum_{\nu=1}^\infty \lvert \xi_\nu \lvert^p < \infty.$ Demuestre que si $\langle \xi_\nu \rangle \in l^p$ y $\langle \eta_\nu\rangle \in l^q$ con $\frac{1}{p} + \frac{1}{q} = 1$, entonces


$$
\sum_{\nu = 1}^\infty \lvert \xi_\nu \eta_\nu \lvert \leq \parallel \langle \xi_\nu \rangle \parallel_p \cdot \parallel \langle \eta_\nu \rangle \parallel_q,
$$


**DRAFT**