---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
Se ${\vec{u}}$, ${\vec{v}}$ e ${\vec{w}}$ não são coplanares, eles são LI.

Uma base é um triplo ordenado B=(${\vec{u}}$, ${\vec{v}},$ ${\vec{w}}$) onde ${\vec{u}}$, ${\vec{v}},$ ${\vec{w}}$ são LI.

![[image 2.png|image 2.png]]

  

Pode ser conveniente trocar os elementos de uma base para outra. O conceito central é que um mesmo vetor pode ser expresso de diferentes maneiras, dependendo da base escolhida.

  

Sejam,

${\vec{v}} = (x1,x2,x3){\tiny{E}}$

${\vec{v}} = (y1,y2,y3){\tiny{F}}$

![[image 1.png]]

As coordenadas do vetor ${\vec{v}}$ podem ser escritas em relação a cada uma das bases:

![[image 2 2.png|image 2 2.png]]

  

  

A seguir, podemos escrever as coordenadas da base F em relação à base E.

![[image 3.png]]

- Onde os coeficientes _a_ são valores reais.

  

Desta forma, é possível escrever as coordenadas de F em relação às coordenadas de E.

![[image 4.png]]

- note: y1, y2 e y3 referem-se às coordenadas de ${\vec{v}}$ na base F.

- No caso, por exemplo, estamos substituindo a multiplicação de $y1f1$ (a qual seria uma coordenada de ${\vec{v}}$ na base F) pelo valor de f1 (relação das coordenadas de F pelas coordenadas de E).

  

Por fim, encontramos as coordenadas de ${\vec{v}}$ na base E a partir das coordenadas de ${\vec{v}}$ na base F, com os valores ecnontrados anteriormente.

![[image 5.png]]

  

  

De forma geral, é possível aplicar uma matriz de mudança de base, a qual possui as coordenadas de ${\vec{v}}$ na base E e as coordenadas de ${\vec{v}}$ na base F, passando por uma matriz P, com os coeficientes que igualam as coordenadas.

- Com ela, multiplicamos a matriz da base original por P, assim chegando à nova base.

![[image 6.png]]

  

## Definição

![[image 7.png]]

A matriz de mudança de E para F como:

![[image 8.png]]

É necessário notar algumas regras importantes:

- Os coeficientes de cada coordenada da base deve ocupar uma coluna, isto é, os coeficientes de f1 são a 1a coluna, os coeficientes de f2 são a segunda coluna e os coeficientes de f3 a terceira.
    
    - Exemplo:
    

![[image 9.png]]

  

A matriz de mudança pode ser representada como:

![[image 10.png]]

## Teorema

Sejam E = (e1, e2, e3), F=(f1, f2, f3) e G=(g1, g2, g3) ${\in}$ V³

  

1. A mudança de base E → E é uma matriz identidade de ordem 3.
    
    ![[image 11.png]]
    

1. A mudança de base E →$^M$ → F é igual a inversa de F →$^M$→E, isto é $M{\tiny{FE}}=(M{\tiny{EF}})^-1$

1. A mudança de base E → $^M$→F * E →$^M$→G é igual a E→$^M$→G, isto é: $M{\tiny{FE}}*M{\tiny{FG}}=M{\tiny{EG}}$

## Teorema

A matriz A e M${\tiny{3}}$(A) tem matriz inversa se e somente se |A|≠0.

- Corolário: |M${\tiny{EF}}$|≠0.

### Proposição

Sejam A, B ${\in}$ M${\tiny{3}}$ são inversíveis:

- $(AB)$$^{-1}$=$A^{-1}*B{^-1}$

- $(A^{-1})^{-1}=A$

- $I{\tiny{3}}^{-1}=I{\tiny{3}}$