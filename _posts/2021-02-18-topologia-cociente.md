---
layout: posts
title: "Topología Cociente"
date: 2021-01-18 12:00:00
categories: posts
tags: topologia
---

# Topología Cociente

_Definición_. Sean $X$ y $Y$ espacios topológicos; sea $p: X \rightarrow Y$ un mapeo sobreyectivo. El mapeo $p$ es un **mapeo cociente** si  $U \subset Y$ es abierto ssi $p^{-1}(U)$ es abierto en $X$. 

Obsérvese que la definición anterior es más fuerte que continuidad. Otra forma de llamar a los mapeos cociente es **continuidad fuerte.**

Otra forma de describir un mapeo cociente es la siguiente: decimos que un subconjunto $C \subset X$ es **saturado** si $C$ contiene cada conjunto $p^{-1}(\{y\})$ que intersecta. Con esto, decimos que $p$ es un mapeo cociente si $p$ es continua y mapea conjuntos abiertos y saturados de $X$ en abiertos de $Y$.

**Definición.** Si $X$ es un espacio topológico y $A$ es un conjunto y si $p: X \rightarrow A$ es un mapeo sobreyectivo, entonces existe exactamente una topología $\tau$ en $A$ tal que $p$ es un mapeo cociente. A esta topología se le conoce como **topología cociente** inducida por $p$.

**Definición.** Sea $X$ un espacio topológico, y sea $X^*$ una partición disjunta de $X$. Sea $p: X \rightarrow X^\ast$ el mapeo sobreyectivo que mapea cada punto de $X$ al elemento de $X^\ast$ que contiene a ese punto. En la topología cociente inducida por $p$, el espacio $X^\ast$ se le conoce como **espacio cociente** de $X$.

Al espacio cociente también se le llama **espacio de identificación** de $X$.

