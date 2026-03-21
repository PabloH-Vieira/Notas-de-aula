---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
# Distâncias

### Pontos

A distância entre dois pontos consiste na norma do vetor formado entre esses dois pontos.

- A norma vai tomar quantidade de coordenadas igual a quantidade de planos no espaço.

![[image 21.png|image 21.png]]

### Entre ponto e reta

A distância entre um ponto P e uma reta _r_ é igual a distância entre P e Q, sendo Q definido como a projeção ortogonal de P sobre _r._

Para calcular a distância entre um ponto e uma reta necessitamos de um ponto A pertencente a reta e o vetor diretor $\vec{r}$, chegando na fórmula a seguir.

![[image 1 11.png|image 1 11.png]]

Outra aplicação se dá quando temos, ao invés do vetor diretor, outro ponto na reta, seja ele B.

![[image 2 8.png|image 2 8.png]]

### Ponto e Plano

Para calcular a distância entre um ponto e um plano, utilizamos a mesma lógica da distância anterior, ou seja, a distância entre um ponto e um plano é a mesma que aquela entre P e Q, com Q sendo a projeção do ponto P sobre o plano.

Uma fórmula análoga e que utiliza o vetor normal do plano e um ponto A no plano é a seguinte:

![[image 3 3.png|image 3 3.png]]

Outra forma é utilizando a equação geral do plano juntamente das coordenadas do ponto  
P = (x0, y0, z0)

![[image 4 3.png|image 4 3.png]]

### Retas

A distância entre duas retas é a mesma definida entre os pontos A e B, sendo que esses pontos pertencem a uma reta _r_ perpendicular a ambos os planos.

![[image 5 3.png|image 5 3.png]]

- A distância entre retas concorrentes é igual a 0.

A fórmula para calcular a distância entre duas retas reversas é a seguinte:

- Tomando os pontos P pertencente a _r_ e o ponto Q pertencente a _s._ Além disso tomando $\vec{r}$ como o vetor diretor da reta perpendicular em comum.

![[image 6 3.png|image 6 3.png]]

### Reta e Plano

Tomamos uma reta _r_ com vetor diretor $\vec{r}$ e um plano $\pi$ com vetor normal $\vec{n}$.

1. Se $\vec{n}*\vec{r}$≠$0$ então a reta e o plano são concorrentes e a distância entre eles é igual a 0.

1. Se $\vec{n}*\vec{r}=0$ então a reta e o plano são paralelos ou coincidentes e, nesse caso, a distância será igual a distância entre P e o plano, com P pertencente à reta.

### Planos

Tomando os planos $\pi1$ e $\pi2$ e seus respectivos vetores normais $\vec{n1}$ e $\vec{n2}$.

1. Se os normais forem LI, então os planos são concorrentes e por consequência, a distância entre os planos é 0.
    
    ![[image 7 3.png|image 7 3.png]]
    

1. Se os normais são LD, então os planos são paralelos, e a distância entre os planos será igual a distância entre dois pontos quaisquer pertencentes aos planos (por serem paralelos, a distância é constante).