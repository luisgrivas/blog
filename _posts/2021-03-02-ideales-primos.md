---
layout: post
title: "Ideales de anillos"
date: 2021-03-02 14:30:00
categories: posts
tags: [algebra, ideales]
---

## Ideales

En lo siguiente, se asume que un anillo $A$ es conmutativo y que tiene un elemento unitario.

**Definición**. Un ideal de un anillo $A$ es un subconjunto $I \subset A $ que es un grupo aditivo tal que $AI \subset a$.

**Ejemplo.** Es claro que los conjuntos $\{0\}$ y $A$ son ideales de cualquier anillo $A$.

**Ejemplo.** Si $A$ es un anillo y $a \in A$, el conjunto $(a) := \{ra : r \in A \}$ es un ideal. A estos ideales se les conoce como **ideales principales**. En el anillo $\mathbb{Z}$ sucede que todo ideal es principal. Para ver esto sea $I$ un ideal de $\mathbb{Z}$ distinto $(0)$. Como $I$ es un subgrupo aditivo, entonces $I \cap \mathbb{N} \neq \varnothing $. Por el Principio del Buen Orden, existe un natural mínimo en $I$, digamos $d$. Afirmamos que $I = (d)$. Claramente, $(d) \subset I$. Sea $p \in I$ y dividámoslo por $d$ mediante el algoritmo de Euclides: $p = qd + r$, con $0 \leq r < d$. Entonces $r = p - dq \in I$, ya que este es un ideal. Pero $r < d$ y $d$ es el natural mínimo que pertenece a $I$; luego $r = 0$. Por tanto $ I \subset (d).$

**Ejemplo.** Sea $\phi: A \rightarrow B$ un homomorfismo de anillos. Una computación directa demuestre que el kernel de $\phi$ definido como $\ker \phi := \{x \in R: \phi(x) = 0\}$ es un ideal de $A$.

Los ideales juegan el papel de subgrupos normales en el sentido de que el cociente $A / I$ forma un anillo bajo las operaciones inducidas *naturalmente* por $A$: $[a] + [b] = [a + b]$ y $[a] \cdot [b] = [a \cdot b]$. Evidementemente es necesario demostrar previamente que estas operaciones están bien definidas. El anillo $A/I$ se le conoce como **anillo cociente.**

Sea $\phi: A \rightarrow A/I$ es un homomorfismo de anillos y sea $J$ un ideal de $A/I$. Sea $K:= \phi^{-1}(J)$. Observe que si $x, y \in K$, entonces $\phi(x + y) = \phi(x) + \phi(y) \in J$, que implica que $x + y \in K$. Por otro lado, $\phi(-x) = - \phi(x) \in J$, entonces $-x \in K$. Esto muestra que $K$ es un subgrupo aditivo de $A$. Más aún, si $r \in A$, entonces $\phi(r a) = \phi(r) \phi(a) \in J$, de manera que $ra \in K$. Lo anterior demuestra que $K$ es un ideal. Más aún, $I \subset K$, ya que $\phi(I) = [0] \in J$. Concluimos con el siguiente teorema.

**Teorema.** Existe una correspondencia uno a uno entre los ideales de $A$ que contienen a $I$ y los ideales de $A/I$.

Existe una caracterización muy útil de un campo $A$ mediante ideales. 

**Teorema.** Sea $A$ un anillo distinto del $\{0\}$. Los siguientes son equivalentes:

1. $A$ es un campo.
2. Los únicos ideales de $A$ son $0$ y $(1)$. 
3. Todo homomorfismo de $A$ en anillo no cero $B$ es inyectivo. 

*Demostración:* $(1. \Rightarrow 2.)$ Si $I$ es un ideal de $A$ distinto de cero, entonces existe un $r \in I$ distinto de cero. Como $r$ tiene inverso, $(r) = (1)\subset I$. Luego, $I = (1)$.

$(2. \Rightarrow 3.)$ Si $\phi: A \rightarrow B$ es un homomorfismo, el $\ker \phi$ es un ideal. Este es distinto de $(1)$ ya que $B$ no es cero, entonces $\ker \phi = \{0\}$. Por tanto $\phi$ es inyectivo.

$(3. \Rightarrow 1.)$ ...

## Ideales primos e ideales maximales

Consideremos el anillo de los enteros $\mathbb{Z}$ bajo las operaciones de suma y multiplicación usuales. Existe una forma de caracterizar a los ideales de $\mathbb{Z}$: Si $I$ es un ideal de $\mathbb{Z}$, entonces $I = \{a n: n\in \mathbb{Z} \} = (a).$ Para ver esto, observe que ...

**Definición.** Un ideal $P$ es **primo** si $P \neq (1)$ y si $xy \in P$, entonces $x \in P$ o $y \in P$. Un ideal $M$ es **maximal** si $M \neq (1)$ y si no existe un ideal $I$ tal que $M \subset I \subset (1)$.

Existe una forma equivalente (e interesante) de caracterizar a los ideales primos y maximales de un anillo:

**Proposición.** Sea $A$ un anillo y $I$ un ideal de $A$. Entonces:

1.  $I$ es primo si y solo si $A/I$ es un dominio.
2. $I$ es maximal si y solo si $A/I$ es un campo.

*Demostración:* ($1. \Rightarrow$) Sea $I$ primo y sean $[a], [b] \in A/I$ tales que $[a][b] = [0]$. Esto implica que $[ab] = [0]$, es decir, $ab \in I$. Entonces $a \in I$ o $b \in I$, lo que muestra que $[a] = [0] $ o $[b] = [0]$. 

$(1. \Leftarrow)$ Si $A/I$ es dominio, entonces   ...

Observe que la proposición anterior implica que todo Como veremos más adelante, el estudio de ideales primos es central en álgebra. Una pregunta natural es, ¿para cualquier anillo $A$ siempre puedo encontrar un ideal $I$ de $A$ maximal?

**Teorema.** Todo anillo $A \neq \{0\}$ tiene al menos un ideal maximal.

*Demostración:*

Sea $\mathcal{R} $ el conjunto de todos los elementos nilpotentes de $A$. A este conjunto se le conoce como **nilradical** de $A$. Este conjunto satisface lo siguiente.

**Proposición.** El nilradical $\mathcal{R}$ de un anillo $A$ es un ideal de $A$. Además, el anillo $A/\mathcal{R}$ no tiene elementos nilpotentes.

*Demostración:*

El nilradical posee una interesante caracterización descrita por la siguiente proposición.

**Proposición.** El nilradical de $A$ es la intersección de todos los ideales primos de $A$. 

*Demostración:*

Una aplicación inmediata de esta proposición es la resolución del siguiente problema.

**Aplicación.** $f = \sum_{r=0}^n a_r x^r \in A[x]$ es una unidad si y solo si $a_0$ es una unidad y $a_1, \ldots, a_n$ son nilpotentes.

*Demostración:* $(\Leftarrow)$ Vease [esta publicación](https://www.luisgrivas.com/blog/posts/2021/03/01/ej-algebra-1.html).

$(\Rightarrow)$ Sea $\mathcal{R}$ el nilradical de $A$ y sea $f = \sum_{r=0}^n a_r x^r \in A[x]$ es una unidad. Entonces existe $g = \sum_{} \in A[x]$ tal que $fg = 1$.

**DRAFT**

**Referencias**

Introduction to Commutative Algebra ... Atiyah