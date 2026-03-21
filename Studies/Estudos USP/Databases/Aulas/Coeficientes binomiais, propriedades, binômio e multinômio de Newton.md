---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-09-10T11:38
---
![[image 71.png|image 71.png]]

Podemos relacionar os coeficientes binomiais ao triângulo de Pascal, e dele extrair algumas propriedades.

![[image 1 54.png|image 1 54.png]]

- A primeira propriedade nos diz que ao somarmos um elemento com o seu posterior, chegamos ao elemento da linha de baixo.

- A segunda propriedade nos diz que as linhas são simétricas. Os elementos exatamente opostos seguem a mesma sequência.

- A soma dos elementos de cada linha é exatamente o dobro da linha anterior.

![[image 2 44.png|image 2 44.png]]

Essas propriedades também podem ser interpretadas do ponto de vista da análise combinatória.

1. O total de combinações de subconjuntos de _k_ elementos de um conjunto de _n_ elementos é igual à quantidade de subconjuntos com _n-k_ elementos.

1. O total de combinações de subconjuntos de _k_ elementos dentro do conjunto de _n_ elementos é igual ao total de combinações entre os subconjuntos de _k-1_ elementos entre _n-1_ elementos somado ao total de combinações de _k_ elementos escolhidos num conjunto de _n-1_ elementos.

1. A terceira propriedade pode ser entendida a partir do princípio da bijeção. Consiste no total de combinações possíveis de subconjuntos com _k=0_ até _k=n_ elementos. Imaginemos que os elementos escolhidos tem valor 1, e os demais 0. Para cada subconjunto de _k_ elementos, há duas possibilidades: 0 ou 1. Assim, incrementando _k_ até chegar em _n_, teremos $2^n$ possibilidades.

## Binômio de Newton

![[image 3 37.png|image 3 37.png]]

Usamos o binômio para calcular a soma na e_nésima_ potência.

**Exemplo: n=2**

![[image 4 33.png|image 4 33.png]]

- Observe que calculamos os arranjos possíveis com _n_ fixado em 2.

O binômio de Newton pode ser provado por indução e por lógica combinatória.

## Trinômio de Newton

![[image 5 23.png|image 5 23.png]]