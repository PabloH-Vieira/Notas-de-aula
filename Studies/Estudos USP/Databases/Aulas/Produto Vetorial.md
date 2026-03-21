---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
O produto vetorial consiste em uma operação entre dois vetores que resulta em um terceiro vetor ortogonal aos dois primeiros.

- Esse vetor é único em sentido e módulo.

# Definição

A representação do produto vetorial é ${\vec{u}}\wedge{\vec{v}}$

1. Se ${\vec{u}}$ e ${\vec{v}}$ são LD, então o produto vetorial entre eles é 0.

1. Se os vetores ${\vec{u}}$ e ${\vec{v}}$ são LI e houver um ângulo entre eles:
    
    1. ${\vec{u}}\wedge{\vec{v}}$ é ortogonal a ${\vec{u}}$ e ${\vec{v}}$.
    
    1. A base composta por (${\vec{u}}, {\vec{v}}, {\vec{u}}\wedge{\vec{v}}$) é positiva.
    
    $$||{\vec{u}}\wedge{\vec{v}}|| = ||{\vec{u}}|| * ||{\vec{v}}|| * sen{\Theta}$$
    

O produto vetorial será igual a 0 unicamente quando os vetores da operação forem LD.

O módulo do produto vetorial pode ser obtido também em função da área do paralelogramo determinado por ${\vec{u}}$ e ${\vec{v}}$.

![[image 15.png|image 15.png]]

O produto vetorial é calculado a partir de uma matriz que contém os vetores de uma base ortonormal, bem como as coordenadas dos vetores (em relação a essa base) que compõem a operação, dispostos em linhas:

![[image 1 5.png|image 1 5.png]]

# Propriedades

1. ${\vec{u}}\wedge{\vec{v}}$ = $-{\vec{v}}\wedge{\vec{u}}$

1. ${\vec{u}}\wedge({\delta}*{\vec{v}})$=${\vec{v}}\wedge({\delta}*{\vec{u}})$=${\delta}*$(${\vec{u}}\wedge{\vec{v}}$)

1. ${\vec{u}}\wedge({\vec{v}}+{\vec{w}})$= ${\vec{u}}\wedge{\vec{v}}+{\vec{u}}\wedge{\vec{w}}$

## Proposição

1. $({\vec{u}}\wedge{\vec{v}})\wedge{\vec{w}}$ = $-({\vec{v}}*{\vec{w}}){\vec{u}}+({\vec{u}}*{\vec{w}}){\vec{v}}$

1. ${\vec{u}}\wedge({\vec{v}}\wedge{\vec{w}})$ = $({\vec{w}}*{\vec{u}}){\vec{v}}-({\vec{v}}*{\vec{u}}){\vec{w}}$

## Corolário - Identidade de Jacobi

$({\vec{u}}\wedge{\vec{v}})\wedge{\vec{w}}+({\vec{v}}\wedge{\vec{w}})\wedge{\vec{u}}+({\vec{u}}\wedge{\vec{w}})\wedge{\vec{v}}=0$

### Observação

$({\vec{u}}\wedge{\vec{v}})\wedge{\vec{w}} ≠ {\vec{u}}\wedge({\vec{v}}\wedge{\vec{w}})$

Por isso é importante atentar-se à posição dos parênteses.

## Proposição

Sejam ${\vec{u}}$ e ${\vec{v}}$ dois vetores LI. Então:

1. $({\vec{u}}\wedge{\vec{v}})\wedge{\vec{w}}$ é uma combinação linear de ${\vec{u}}$ e ${\vec{v}}$, independente do valor de ${\vec{w}}$.

## Corolário

Sejam ${\vec{u}}$ e ${\vec{v}}$ dois vetores LI. Então B=(${\vec{i}}, {\vec{j}}, {\vec{k}}$) com:

$${\vec{i}}={\frac{{\vec{u}}}{||{\vec{u}}||}}$$

$${\vec{j}}={\frac{({\vec{u}}\wedge{\vec{v}})\wedge{\vec{u}}}{||({\vec{u}}\wedge{\vec{v}})\wedge{\vec{u}}||}}$$

$${\vec{k}}={\frac{{\vec{u}}\wedge{\vec{v}}}{||{\vec{u}}\wedge{\vec{v}}||}}$$

É uma base ortormal.