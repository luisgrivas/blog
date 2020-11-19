---
layout: post
title:  "Los tres principios de Littlewood"
date:   2020-11-12 12:00:00 
categories: posts
tags: [analisis-real, medida]
---

> "The extent of knowladge required is nothing like so great as is sometimes supposed. There are three principles, roughly expressible in the following terms: Every (measurable) set is nearly a finite sum of intervals; every function (of class $L^\lambda$) is nearly continuous; every convergent sequence of functions is nearly uniformly convergent. " (Littlewood, 1994).



## Todo conjunto medible es casi un abierto

**Lema 1.** Sea $A$ un conjunto   sea $\epsilon > 0$. Entonces existe un conjunto abierto $O$ tal que $A \subset O$ y $m^\ast O \leq m^\ast A + \epsilon$. Existe un $G \in \mathcal{G}_\delta$ tal que $A \subset G$ y $m^\ast A = m^\ast G$. 

*Demostración:*  Si $m^\ast A = \infty $, la conclusión se satisface inmediatamente. Suponga que $m^* A < \infty$. Entonces, existe una cubierta numerable de intervalos abiertos $(I_n)$ tal que $ \sum_n l(I_n) \leq  m^\ast A + \epsilon $. Luego, $O = \bigcup_n I_n $ satisface lo requerido. 

Para cada $n\in \mathbb{N}$, sea $G_n$ un abierto tal que $m^\ast G_n \leq m^\ast A + \frac{1}{n}$ y $A \subset G_n$. Definamos $G = \bigcap_n G_n$. Claramente $m^\ast A \leq m^\ast G$.  Pero también $m^\ast G \leq  m^\ast A + \frac{1}{n} $, para toda $n\in \mathbb{N}$. Por tanto $m^\ast G = m^\ast A$.



**Lema 2**. Sean $A$ y $B$ subconjuntos de $\mathbb{R}$. Si $B \subset A$ y $m^\ast B < \infty$, entonces $m^\ast(A \setminus B) \leq  m^\ast A - m^\ast B$. 

*Demostración:* Observe que $m^\ast A \leq m^\ast (A \setminus B) + m^\ast(A \cap B) \leq m^\ast (A \setminus B ) + m^\ast B$, y la conclusión se sigue inmediatamente. 



**Teorema.** Sea $E$ un conjunto de números reales. Entonces las siguientes proposiciones son equivalentes:

1. $E$ es medible;
2. dado $\epsilon > 0$, existe un abierto $O \supset E$ tal que $m^*(O \setminus E) < \epsilon$;
3. dado $\epsilon > 0$, existe un conjunto cerrado $F \subset E$ tal que $m^*(E \setminus F) < \epsilon$; 
4. existe un $G$ en $\mathcal{G}_\delta$ con $E \subset G$ y $m^*(G \setminus E) = 0$;
5. existe un $F$ en $\mathcal{F}_\delta$ con $F \subset E$ y $m^*(E \setminus F) = 0$.

Si $m^*E $ es finito, entonces las anteriores proposiciones son equivalentes a:

6. Dado $\epsilon > 0$, existe una unión finita de intervalos abiertos $U$ tal que $m^*(U \Delta E) < \epsilon$.

*Demostración:* Supongamos primero que  $m^\ast E < \infty$. 

(1. $\Rightarrow$ 2.) Por el Lema 1, existe un abierto $O \supset E$ tal que $m^\star O < m^\star E + \epsilon$. Entonces $m^\ast (O \setminus E) = m^\ast O - m^\ast E  < \epsilon$. 

(2. $\Rightarrow$ 4.) Para cada $n\in \mathbb{N}$, sea $G_n$ abierto tal que $G_n \supset E$ y $m^\ast(G_n \setminus E) < \frac{1}{n}$. Definamos  $G = \bigcap_n G_n$. Luego, $G$ es $\mathcal{G_\delta}$ y $m^\ast (G \setminus E) \leq m^\ast G - m^\ast E = \lim_{n \to \infty } m^\ast G_n - m^\ast E < \lim_{n \to \infty} \frac{1}{n} = 0$. 

(4. $\Rightarrow 2.$) Sea $G = \bigcap_n G_n$, con $G_n$ abierto, tal que $E \subset G$ y $m^\ast (G \setminus E) = 0$. Sea $\epsilon > 0$. Entonces existe $k \in \mathbb{N}$ tal que $ G_k \supset E$ y $m^\ast (G_k \setminus E) < \epsilon$. 

Ahora, suponga que $m^\ast E = \infty$.

(1. $\Rightarrow$ 2.) Para cada $k\in \mathbb{N}$, sea  $E_k = E \cap (-k, k)$. Como $E_k$ es medible, existe un abierto $O_k$ tal que $E_k \subset O_k$ y $m^\ast (O_k \setminus E_k) < \frac{\epsilon}{2^k}$. Luego, $E \subset \bigcup_k O_k$ y 


$$
m^\ast(\bigcup_k O_k \setminus E) = m^\ast (\bigcup_k O_k \setminus \bigcup_k E_k) \leq m^*(\bigcup_k O_k \setminus E_k) \leq \sum_k m^\ast (O_k \setminus E_k) < \sum_{k} \frac{\epsilon}{2^k} = \epsilon.
$$


(2. $\Rightarrow$ 4.)



(4. $\Rightarrow$ 1.) 



### Toda función medible es casi continua

**Lema 3**. Sea $f: [a, b] \rightarrow \mathbb{R}$ una función medible que asume los valores $\pm \infty$ en un conjunto de medida cero. Sea $\epsilon > 0$. Entonces existe  $M > 0$ tal que $\lvert f \lvert \leq M$ excepto en un conjunto con medida menor que $\epsilon$.  

*Demostración:* Observe que $\\{x: f(x) = \pm \infty \\} = \bigcap_n \\{x: \lvert f(x) \lvert > n\\}$. Como este conjunto es de medida cero, existe un $M \in \mathbb{N}$ tal que $m^\ast \\{x: \lvert f(x) \lvert > M \\} < \epsilon.$ La conclusión se sigue inmediatamente. $\blacksquare$

**Lema 4.** Sea $f: [a, b] \rightarrow \mathbb{R}^\ast$ una función medible. Sean $\epsilon  > 0$ y $M > 0$. Entonces existe una función simple $\phi$ tal que $\lvert f(x) - \phi(x) \lvert < \epsilon$ excepto donde $\lvert f(x) \lvert \geq M$. Si $m \leq f \leq M$, entonces podemos elegir $\phi$ tal que $m \leq \phi \leq M$. 

*Demostración:* El caso $\epsilon \geq M$ es trivial; supongamos que $\epsilon < M$. Sea $n$ un natural tal que $\frac{2M}{n} < \epsilon$. Considere los números reales $y_k =\frac{2M}{n}k-M$ para $k = 0, 1, \ldots, n$.   Definamos para  $k < n$ el conjunto $A_k = \{x\in [a, b]: y_{k-1} \leq f(x) < y_k \} $ y $A_n = \{x \in [a, b]: y_{n-1} \leq f(x) \leq y_n\}$. Si $A_k \neq \emptyset$, entonces seleccionemos un $t_k \in A_k$.  Definamos la función simple $\phi(x) = \sum_{A_k \neq \emptyset} f(t_k) \chi_{A_k}$. Esta función $\phi$ satisface los requerimientos del Lema. Si $m \leq f \leq M$, procédase de la misma manera considerando $y_k = \frac{M - m}{n} k - m$ con $n \in \mathbb{N}$ tal que $\frac{M-m}{n} < \epsilon$. $\blacksquare$



**Lema 5.** Dado $\epsilon > 0$ y una función escalonada $g$ en $[a, b]$, existe una función continua $h$ tal que $g(x) = h(x)$ excepto en un conjunto de medida menor que $\epsilon$. 

*Demostración:* Si $g$ es constante, el lema se satisface trivialmente. Suponga que $g$ asume $n > 1$ valores distintos. Sean $I_k$ los subintervalos de $[a, b]$ donde $g$ es constante y sea $P = \{x_0, \ldots, x_{n}\}$ la partición de $[a, b]$ inducida por estos subintervalos.  Definamos $\delta = \frac{1}{2}\min \{l(I_1), \ldots, l(I_{n}) \}$ y sea $N \in \mathbb{N}$ tal que $\frac{2\delta(n-1)}{N} < \epsilon$.  Para $ 0 < k <n$, definamos los puntos $y_{2k-1} = x_k - \frac{\delta}{N}$ y $y_{2k} = x_k + \frac{\delta}{N}$ ; $y_0 = x_0$ y $y_{2n+1} = x_{n+1}$. Definamos la función $h$ en $[a, b]$ como 


$$
h(x) = \cases{ g(x), \text{     si } y_{k} \leq  x \leq y_{k+1} \text{ y } k \text{ par }; \\ 
\\
\frac{g(y_{k+1}) - g(y_k))}{y_{k+1} - y_k} (x - y_k) + g(y_k), \text{     si } y_{k} \leq  x \leq y_{k+1} \text{ y } k \text{ impar.} }
$$


Observe que en los intervalos $(y_k, y_{k+1})$ , con $k$ impar, se satisface que $g(x) \neq h(x)$. La longitud de estos es $\frac{2\delta}{N}$ y se tienen $n-1$ de estos. Por tanto el conjunto $\{x \in [a, b]: g(x) \neq h(x) \}$ tiene medida menor que $\epsilon$. $\blacksquare$ *<u>tiene un error..</u>*.



**Lema 6. ** Dada una función simple $\phi$ en $[a, b]$, existe una función escalonada $g$ en $[a, b]$ tal que $g(x) = \phi(x)$ excepto en un conjunto de medida menor que $\epsilon$.

*Demostración:* Sean $a_1, \ldots, a_n$ los valores distintos que asume $\phi$. Definamos $A_k = \phi^{-1}(\{a_k\})$, $k=1, \ldots, n$. 



**Teorema.** Sea $f$ una función medible definida en un intervalo $[a, b]$, y supóngase que $f$ toma los valores $\pm \infty$ únicamente en un conjunto de medida cero. Entonces, dado $\epsilon  >0$, existe una función continua $g$ tal que 
$$
\mid f - g \mid < \epsilon
$$
y  $m \{x: \lvert f(x) - g(x) \lvert \geq \epsilon \} < \epsilon$.

*Demostración:*





**Teorema de Luzin**. Sea $f$ una función medible de valores reales de finida en un intervalo $[a, b]$. Entonces, dado $\delta > 0$, eiste una función continua $\phi$ en $[a, b]$ tal que $m \{ x: f(x) \neq \phi(x) \} < \delta $.  

*Demostración:*



## Toda sucesión convergente de funciones medibles es uniformemente convergente

**Teorema.** Sea $E$ un conjunto medible de medida finita y sea $(f_n)$ una sucesión de funciones medibles que converge a.e. a una función $f$ en $E$. Entonces, dado $\epsilon > 0$ y $\delta > 0$, existe un conjunto $A \subset E$ con $m A < \delta $, y una $N$ tal que para toda $x \notin A$ y para toda $n \geq N$, 
$$
\lvert f_n(x) - f(x)\lvert < \epsilon.
$$
**Demostración:**



**Teorema de Egorov** Sea $(f_n)$ una sucesión de funciones medibles que converge  a una función real $f$ a.e. en un conjunto $E$ de medida finita.  Entonces, dado $\eta > 0$, existe un subconjunto $A \subset E$ tal que $m A < \eta$ y $(f_n)$ converge uniformemente a $f$ en $E \setminus A$. 

**Demostración:**



**DRAFT**