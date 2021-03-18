---
layout: post
title: "Espacios cubrientes"
date: 2021-03-04 9:00:00
categories: posts
tags: [topologia, topologia-algebraica]
---



**Definición.** Sea $p: E \rightarrow B$ una función continua y sobreyectiva. El abierto $U$ de $B$ se dice que está *evenly covered* por $p$ si la imagen inversa de $p^{-1}(U)$ puede ser escrita como la unión disjunta de abiertos $V_\alpha$ en $E$ tal que para cada $\alpha$, la restricción de $p$ en $V_\alpha$ es un homeomorfismo de $V_\alpha$ en $U$. La colección $\{V_\alpha\}$ se dice que es una partición de $p^{-1}(U)$ es *rebanadas.*



**Definición.** Sea $p: E \rightarrow B$ una función continua y sobreyectiva. Si cada punto $b\in B$ tiene una vecindad $U$ que está *evenly covered* por $p$, entonces se dice que $p$ es un **mapeo cubriente** y se dice que $E$  es un **espacio cubriente** de $B$.

**Teorema.** El mapeo $\epsilon: \mathbb{R} \rightarrow \mathcal{S}^1$ definido como $\epsilon(r) = e^{2\pi \ i \ r}$ es un mapeo cubriente.

*Demostración:* Considere los conjuntos $X_+ := \{z \in \mathcal{S}^1: Re(z) > 0 \}$, $X_{-} := \{z\in S^1: Re(z) < 0 \}$, $Y_+ := \{z\in S^1 : Im(z) > 0\}$ y $Y_{-}:= \{z \in S^1: Im(z) < 0 \}$.

**Teorema.** Sea $p: E \rightarrow B$ un mapeo cubriente. Si $B_0$ es unb subespacio de $B$, y si $E_0 = p^{-1}(B_0)$, entonces el mapeo $p_0: E_0 \rightarrow B_0$ obtenido restringiendo $p$ a $E_0$ es un mapeo cubriente.

**Teorema.**  $p: E \rightarrow B$ y $p^\prime: E^\prime \rightarrow B^\prime$ son mapeos cubrientes, entonces

$$p \times p^\prime: E \times E^\prime \rightarrow B \times B, $$

es un mapeo cubriente.

