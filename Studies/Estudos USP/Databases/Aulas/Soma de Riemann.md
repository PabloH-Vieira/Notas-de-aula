---
Course:
  - https://www.notion.so/C-lculo-III-313fa7f60cd880d2a072c0acf7a9fdec?pvs=21
Last Edited: 2026-03-02T17:41
---
A definição de soma de Riemann do cálculo I pode ser reimaginada no Cálculo III, com a diferença de que agora há mais de uma dimensão.

Em sua primeira versão, podia-se dividir um conjunto limitado em intervalos que, somados, compunham o conjunto inteiro. Aqui, os eixos também são divididos, mas ao observá-los no gráfico percebemos a formação de partições, retângulos (ou qualquer que seja a figura formada no gráfico) com duas ou mais dimensões.

- Considerando que o eixo _x_ tenha _m_ intervalos e o eixo _y_ tenha _n_ intervalos, temos a formação de $m * n$ partições

![[image 139.png|image 139.png]]

A área de cada retângulo (ou partição) é dada por $\Delta xi * \Delta yj$

### Soma de Riemann

![[image 1 106.png|image 1 106.png]]

Por definição, a Soma de Riemann é a soma de todos os pontos escolhidos arbitrariamente dentro de um intervalo, multiplicados pelo sub-intervalo ao qual pertencem.

  

Para planos, a Soma de Riemann torna-se uma integral dupla.

![[image 2 85.png|image 2 85.png]]

Nele, temos uma integral dupla de uma função _f_ cujo comportamento é $\mathbb{R}² \rightarrow \mathbb{R}$ em um ponto arbitrário $Xij$ pertencente a uma subconjunto A. Essa função é multiplicada pela partição dada por $\Delta xi\Delta yj$

- Os elementos pertencentes ao subconjunto A são calculados pela Soma de Riemann, enquanto os que não pertencem tem valor 0.

![[image 3 72.png|image 3 72.png]]

No exemplo, tomamos um ponto $Xij$ pertencente à partição $\Delta xi\Delta yj$ em uma função que descreve um paralelepípedo.

  

O valor da parcela de um ponto $Xij$ estará sempre entre os valores resultantes do pontos que descrevem o maior e o menor valor para a função.

![[image 4 57.png|image 4 57.png]]

Quanto mais as partições diminuírem de tamanho, maior fica a soma de Riemann e nos aproximamos do volume descrito pela superfície de f(x,y) em A.