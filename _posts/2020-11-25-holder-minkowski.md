---
layout: post
title: "Las desigualdades de Hölder y de Minkowski"
date: 2020-11-25 3:00:00
categories: posts
tags: analisis-real
---



**Desigualdad de Young**. Sean $a$ y $b$ reales no negativos y sea $0 < \lambda < 1$. Entonces $a^\lambda b^{1 - \lambda} \leq \lambda a + (1 - \lambda ) b$.

*Demostración.* Consideremos la función $\phi(t) = (1 - \lambda) + \lambda t - t^{\lambda}$. Observe que $\phi^\prime(t) = \lambda - \lambda t^{\lambda - 1}$. Como $\lambda - 1 < 0$, si $0 < t < 1$, entonces $\phi^\prime(t) < 0$ y si $t > 1$, entonces $\phi^\prime(t) > 0$. Entonces $\phi(t) > \phi(1) = 0$ para toda $t \geq 0$. De manera que $(1 - \lambda) + \lambda t \geq t^\lambda$ para toda $t \geq 0$. Si hacemos $t = a/b$, se obtiene la desigualdad deseada. $\blacksquare$



**Desigualdad de Hölder.** Si $p$ y $q$ son dos números reales extendidos tales que $\frac{1}{p} + \frac{1}{q} = 1$, y si $ f \in L^p$ y $g \in L^q$, entonces $f\cdot g \in L^1$ y 
$$
\int \lvert fg \lvert \leq \parallel f\parallel_p \cdot \parallel g \parallel_q.
$$
La desigualdad solo es obtenida si y solo si, existen constantes $\alpha$, $\beta$  tales que $\alpha \lvert f \lvert^p = \beta \lvert g \lvert^q$ c.s.

*Demostración.* Considere el caso $p = 1$ y $q = \infty$. Observe que $\lvert f g \lvert = \lvert f \lvert \cdot \lvert g \lvert \leq \lvert f \lvert \cdot \parallel g \parallel_\infty$. Entonces 


$$
\int \lvert f g\lvert \leq \parallel g \parallel_\infty \int \lvert f \lvert = \parallel f\parallel_p \cdot \parallel g \parallel_\infty,
$$
 

obteniendo lo deseado.

 Ahora supong que $\parallel f \parallel_p = \parallel g \parallel_q = 1$, entonces $\lvert fg \lvert \leq  \frac{\lvert f \lvert^p}{p} + \frac{ \lvert g \lvert^q}{q} $ por la desigualdad de Young. Luego, 


$$
\int \lvert fg \lvert \leq \int\left( \frac{\lvert f \lvert^p}{p} + \frac{ \lvert g \lvert^q}{q}\right) = \frac{1}{p}\int \lvert f \lvert^q + \frac{1}{q} \int  \lvert g \lvert^q = 1 = \parallel f\parallel_p \cdot \parallel g \parallel_q, 
$$
y por tanto  $f\cdot g \in L^1$. 

Suponga ahora que $ \parallel f \parallel_p \neq 0 $ y $ \parallel g \parallel_q \neq 0$. Entonces 


$$
\frac{1}{\parallel f \parallel_p \parallel g \parallel_q} \int \lvert fg \lvert = \int \frac{\lvert f \lvert}{\parallel f \parallel_p} \frac{\lvert g \lvert }{\parallel g \parallel_q} \leq 1.
$$


 Despejando se obtiene $\int \lvert fg \lvert \leq \parallel f \parallel_p \parallel g \parallel_q$, y por tanto $f \cdot g \in L^1$. 

Finalmente, la desigualdad se satisface trivialmente si $\parallel f \parallel_p = 0$ o $\parallel g \parallel_q = 0$. $\blacksquare$

**Desigualdad de Minkowski.** Si $f$ y $g$ son elementos de $L^p$, entonces $f + g \in L^p $ y
$$
\parallel f + g \parallel_p \leq \parallel f \parallel_p + \parallel g \parallel_q.
$$
*Demostración.* Es claro que $f + g \in L^p$, ya que $\lvert f + g \lvert \leq \lvert f \lvert + \lvert g \lvert $.



**DRAFT**

