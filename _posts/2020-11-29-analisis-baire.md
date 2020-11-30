---
layout: post
title: "Teorema de Baire en espacios métricos"
date: 2020-11-29 22:53:00
categories: posts
tags: analisis-real
---



**Definición.** Decimos que un conjunto $E$ en un espacio métrico $X$ es **denso en ninguna parte**, si $\bar{E}^c$ es denso en $X$.

Un ejemplo sencillo de este tipo de conjuntos son los enteros $\mathbb{Z}$. También [el conjunto de Cantor es denso en ninguna parte](https://luisgrivas.github.io/blog/post/2020/11/06/conjunto-cantor.html). 



**Teorema.** Sea $X$ un espacio métrico completo y $\\{O_n\\}$ una colección numerable de subconjuntos abiertos densos en $X$. Entonces $\bigcap_n O_n$ es no vacía. 

*Demostración.*



**Corolario (Teorema de Categoría de Baire).** Un espacio métrico completo no es la unión numerable de conjuntos densos en ninguna parte. 

*Demostración:* Sea $X$ un espacio métrico completo. Suponga que $X = \bigcup_n O_n$ donde $O_n$ son densos en ninguna parte. Entonces $\bar{O}_n^c$ es un conjunto abierto  y denso para toda $n\in \mathbb{N}$. Pero $\emptyset = \bigcap \bar{O}_n^c$, lo cual contradice al Teorema anterior. $\blacksquare$

Un conjunto $E$ se dice que es de **primera categoría** si es la unión numerable de conjuntos densos en ninguna parte. El corolario anterior puede reescribirse  como: *ningún espacio métrico completo es de primera categoría.* 

Por ejemplo, $\mathbb{Q}$ es de primera categoría en $\mathbb{R}$. Sea $(x_n)$ una enumeración de $\mathbb{Q}$. Entonces $\mathbb{Q} = \bigcup_n\\{x_n\\}$ y también $\overline{\\{x_n\\}}^c = (-\infty, x_n]\cup[x_n, \infty)$ es denso para toda $n$ en $\mathbb{N}$. Esto tiene como consecuencia algo todavía más interesante: no existe una función real continua $\mathbb{Q}$ y discontinua en $\mathbb{R}\setminus \mathbb{Q}$. Si existiera, entonces $\mathbb{Q}$ sería un conjunto $\mathcal{G}_\delta$, es decir,  $\mathbb{Q} = \bigcap_n O_n$ con $O_n$ abierto en $\mathbb{R}$. Como $\mathbb{Q} \subset O_n$ y $\mathbb{Q}$ es denso en $\mathbb{R}$, entonces $O_n$ es denso en $\mathbb{R}$. Luego, $\mathbb{R}\setminus \mathbb{Q} = \bigcup_n O_n^c$. Observe que $\overline{O_n^c} = O_n^c$ ya que este es cerrado y por tanto $\overline{O_n^c}^c = O_n$ es denso para toda $n\in \mathbb{N}$. Se sigue que $\\{O_n^c\\}$ es una colección numerable de conjuntos densos en ninguna parte. Esto implica que $\mathbb{R}\setminus \mathbb{Q}$ es de primera categoría. Como $\mathbb{Q}$ es de primera categoría, se sigue que $\mathbb{R}$ también lo es. Pero esto es imposible, ya que que $\mathbb{R}$ es un espacio métrico completo. Para una demostración más elemental véase el siguiente artículo sobre el [teorema de Volterra](https://luisgrivas.github.io/blog/posts/2020/11/17/volterra.html).

