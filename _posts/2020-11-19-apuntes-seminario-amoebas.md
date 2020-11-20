---
layout: post
title: "Apuntes seminario amoebas 1119"
date: 2020-11-19 16:00:00
categories: posts
tags: teoria-de-graficas
---



**Objetivo:** A cada gráfica $G$ asignar un grupo $S_G \leq S_n$.

**Observacion:** $\frac{\lvert S_n \lvert }{ \lvert Aut(G) \lvert }$ = número de subgraficas de $K_n$ isomorfas a $G$ (encajes).

Hacer para $C_4$.



## Reemplazos admisibles de aristas. 

**Definición**. Sean $G$ una gráfica , $e \in E(G)$ y $e^\prime \in E(\bar{G}) \cup \{e\}$- Decimos que $G - e + e^\prime$ es un *reemplazo admisible* de aristas si $G - e + e^\prime  \cong G$.


$$
R_G = \{rs \mapsto kl : G - v_r v_s + v_k v_l \cong G\}.
$$
**Observación:** $R_{G_\sigma} = R_G$ para toda $\sigma \in S_n$. 
$$
S_G(rs \mapsto kl) = \{\sigma \in S_n: G_\delta = G- v_r v_s + v_k v_l\}
$$
**Ejemplo: ** Para $P_4$ , $L_G = \{12, 23, 34\}$. 
$$
R_{P_4}  = \{12 \mapsto 12,12 \mapsto 14, 23 \mapsto 23, 23 \mapsto 14, 23 \mapsto 24, 23 \mapsto 13, ...  \}
$$

$$
S_{P_4}(23 \mapsto 13) = \{(12), (1324)\}.
$$

**Observación**: $(1324) (12) = (14) (23)$.

**Definción**. Dada una gráfica simple $G$ definimos $S_G$ grupo
$$
S_G = \langle  \bigcup_{e\mapsto e^\prime \in R_G} S_G(e \mapsto e^\prime) \rangle
$$
El generado por todas las permutaciónes.

**Ejemplo:** $C_4$.

**PENDIENTE.**



**Ejemplo:** $P_5$.

### Amoeba local

**Definción.** Una gráfica simple $G$ es amoeba local si $S_G \cong S_{n}$ donde $n = \lvert G \lvert$. 



Preguntas

* *¿Cadenas de reemplazos admisibles?*