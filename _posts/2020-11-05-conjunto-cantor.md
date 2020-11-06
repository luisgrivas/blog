---
layout: post
title: "Temas relacionados con el conjunto de Cantor"
date:   2020-11-06 13:38:00 -600
categories: analisis topologia
---

## Conjunto de Cantor



<img src="https://upload.wikimedia.org/wikipedia/commons/5/56/Cantor_set_in_seven_iterations.svg" alt="conjunto de cantor" style="zoom:150%;" />



Hagamos $P_0 = [0, 1]$. Sea $P_1$ el conjunto resultante al remover el tercio central $(\frac{1}{3}, \frac{2}{3})$ de $P_0$, es decir, $P_1  = [0, \frac{1}{3}] \cup [\frac{2}{3}, 1]$. Sea $P_2$ el conjunto resultante al remover los tercios centrales de los intervalos de $P_1$. Obtenemos $P_2 = [0, \frac{1}{9}]\cup [\frac{2}{9}, \frac{3}{9}]\cup [\frac{6}{9}, \frac{7}{9}]\cup [\frac{8}{9}, 1]$. Continuando de está manera, sea $P_n$ el conjunto resultante al remover los tercios centrales de cada intervalo de $P_{n-1}$.  El conjunto de Cantor se define como 

$$C = \bigcap_{k=1}^\infty P_n.$$

Es importante recalcar que esta intersección es no vacía ya que $P_n \supset P_{n+1}$ y cada uno de estos es compacto[^1].

Existe otra definición no obvia para este conjunto. El conjunto de Cantor se define como el conjunto de todos los números reales en $[0, 1]$ cuya expansión ternaria $(a_n)_3$ satisface que $a_n = 0$ o $a_n = 2$ para toda $n \in \mathbb{N}$.

Sea $x = (a_n)_3$ con la descripción anterior. Sea $k \in \mathbb{N}$ el primer natural tal que $a_k = 2$. 

## Propiedades topológicas

De la primera definición podemos constatar que $C$ es **cerrado**, pues es la interseccion de conjuntos cerrados. Otra propiedad interesante es que $C$ es **perfecto**, es decir, además se tiene que todos sus puntos son puntos límites. Si $x \in C$, entonces $x \in P_n$ para toda $n \in \mathbb{N}$. Denotemos por $I_{n, x}$ el intervalo de $P_n$ que contiene a $x$.  Observe que la longitud de $I_{n, x}$ es $l(I_{n, x}) = \frac{1}{3^n}$. Entonces, si $V$ es una vecindad de $x$, para $n$ suficientemente grande $I_{n, x} \subset V$. Luego, alguno de los puntos extremos de $I_{n, x}$ pertenece a $V \cap C\setminus \{ x\}$. Luego $x$ es un punto límite de $C$.  Resumamos lo anterior con el siguiente teorema. 

**Teorema**. El conjunto de Cantor $C$ es perfecto. 

Cabe preguntarse, ¿cómo es el interior de este conjunto? Observe que al definir cada $P_n$, removemos un intervalo de la forma $(\frac{3m + 1}{3^n}, \frac{3m +2}{3^n})$ donde $m$ es un entero no negativo. Si $V$ es una vecindad de $x \in C$, siempre podemos encontrar un intervalo  de la anterior forma que esté contenido en $V$. Esto muestra que ninguna vecindad de $x$ está contenida en $C$. Se duduce que el interior de $C$ es vacío. Esto muestra que el conjunto de cantor es **denso en ninguna parte** de $[0, 1]$. 



## No numerabilidad 

Supongamos $C$ fuera numerable. Sea $\{x_n\}$ una enumeración de $C$. 



**Teorema**. Todo conjunto perfecto es no numerable.

Una segunda forma de demostrar que este conjunto es no numerable es establecer una correspondencia biyectiva entre $C$ y un conjunto no numerable. Por ejemplo, definamos el mapeo  $(a_n)_3 \mapsto (\frac{a_n}{2})_2$. Es claro que esta función es $1-1$ y sobre en el conjunto de todas las sucesiones con rango $\\{0, 1\\}$. 

**Corolario**. El conjunto de cantor es no numerable.



## Medida

En teoría de la medida se conoce el siguiente teorema.

**Teorema**. Si $A$ es numerable, entonces $m A = 0$.

El conjunto de Cantor muestra que el converso no es cierto. Este conjunto es no numerable y sin embargo


$$
m C = \lim_{n \to \infty} m P_n = \lim_{n \to \infty} \left(\frac{2}{3}\right)^n = 0.
$$


## Función Ternaria de Cantor

<img src="https://upload.wikimedia.org/wikipedia/commons/7/7f/Cantor_function.gif" alt="Función ternaria de Cantor" style="zoom:50%;" />





**DRAFT**

[^1]: Vea el siguiente [teorema](https://en.wikipedia.org/wiki/Cantor%27s_intersection_theorem).

