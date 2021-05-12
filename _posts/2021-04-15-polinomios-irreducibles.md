---
layout: post
title: "Polinomios irreducibles en Fp"
date: 2021-04-15 14:30:00
categories: posts
tags: algebra, galois, polinomios 
---

En este post demostraremos el siguiente teorema:

**Proposición.** El número de polinomios mónicos irreducibles de grado $n$ sobre $\mathbb{F}_p$ es

$$ N_n = \frac{1}{n}\sum_{d \mid n} \mu(d) p^{n/d}, $$


donde la sumatoria recorre todos los divisores $d$ de $n$.

## Campos finitos



**Teorema 2.** Sea $p$ un número primo y $n$ un entero positivo. El polinomio $x^{p^n}-x$ es el producto de todos los polinomios mónicos irreducibles sobre $\mathbb{F}_p$ cuyo grado $d$ divide a $n$.

*Demostración:* Sea $q(x) \in \mathbb{F}_{p}[x]$ un polinomio mónico e irreducible de grado $d$. Sea $K = \mathbb{F}_p[x] / (q)$ el campo cuya dimensión como espacio vectorial sobre $\mathbb{F}_p$ es $d$. Si $q(x) \mid x^{p^n} - x$, entonces $K$ es (isomorfo a) un subcampo del *splitting field*  $\mathbb{F}_{p^n}$ de $x^{p^n}-x$. Luego, $n = [\mathbb{F}_{p^n}: \mathbb{F}_{p}] = [\mathbb{F}_{p^n}:K] [K:\mathbb{F}_{p}] = [\mathbb{F}_{p^n}:K] \cdot d$, es decir, $d \mid n$.

Conversamente, suponga que $m = n/d$. Consideremos el automorfismo (verificar) $\phi: \mathbb{F}_{p^n} \rightarrow \mathbb{F}_{p^n}$ definido como $\phi(x) = x^{p^m}$. El campo fijo $K^\prime = \{x \in \mathbb{F}_{p^n}: \phi(x) = x\}$ es isomorfo a $K$.

## Producto de Dirichlet y fórmula de inversión de Möbius 

**Definición.** Definimos a la función de Möbius $\mu$ como sigue:
$$
\mu(1) = 1;
$$
Si $n > 1$, descomonemos a $n$ en potencias de primos $n = p_1^{\alpha_1} \cdots p_k^{\alpha_k}$. Entonces


$$
\mu(n) = \cases{(-1)^k \ \ \text{si } \alpha_1 = \cdots = \alpha_k = 1, \\ 0 \ \ \ \ \ \ \ \ \ \ \text{en otro caso.}}
$$

 

**Definición.** Si $f$  $g$ son dos funciones aritméticas definimos su producto de Dirichlet como la función aritmética $h$ definida por
$$
h(n) = \sum_{d \mid n} f(d) g\left(\frac{n}{d}\right).
$$
Escribiremos $f \ast g$ en lugar de $h$. 

El plan de esta sección es mostrar que las funciones aritméticas $f$ tales que $f(1) \neq 0$ forman un grupo abeliano bajo el producto de Dirichlet. De esta manera, la fórmula de inversión de Möbius se deduce directamente bajo operaciones básicas de grupos. 

**Lema.** La multiplicación de Dirichlet es asociativa y conmutativa. 

*Demostración:* Sean $f, g$ y $k$ funciones aritméticas. 



**Teorema (Fórmula de inversión de Möbius)**  La ecuación 
$$
f(n) = \sum_{d \mid n} g(d),
$$
implica
$$
g(n) = \sum_{d \mid n} f(d) \mu\left(\frac{n}{d} \right).
$$
*Demostración:* Si $f(n) = \sum_{d \mid n} g(d)$, entonces $f = g \ast u$. Multiplicando por $\mu$ obtenemos $f \ast \mu = (g \ast u) \ast \mu = g \ast (u \ast \mu) = g \ast I = g.$

---

**Referencias**

* Simmons, G. J., The Number of Irreducible Polynomials of Degree n over GF(p), Amer. Math. Monthly 77 (1970), pp. 743-745.
* Apostol, T.M., Introducción a la Teoría Analítica de Números, Editorial Reverté