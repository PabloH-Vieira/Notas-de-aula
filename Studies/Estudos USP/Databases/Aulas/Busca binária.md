---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-II-24efa7f60cd880bbbbcaf479fda73ab6?pvs=21
Last Edited: 2025-11-16T01:39
---
A busca binária consiste em um algoritmo de busca em um vetor devidamente ordenado.

Consiste em um algoritmo que sempre busca no índice intermediário da lista. Caso ele não encontre, realiza-se uma comparação e fazemos uma busca em um subintervalo.

- O subintervalo em que ocorrerá a nova busca é definido comparando o valor buscado com o valor intermediário.

- Se maior, o subintervalo será a metade superior.

- Se menor, o subintervalo será a metade inferior.

- A cada passo da busca, o intervalo é dividido por 2, até que se encontre o valor buscado ou que reste apenas um valor (este sendo diferente do buscado).

Esse algoritmo pode ser implementado a partir de uma abordagem recursiva e não recursiva.

### Não recursivo

![[image 117.png|image 117.png]]

A cada iteração verificamos se o valor buscado _x_ é o valor do meio. Se não, redefinimos o intervalo para a parte maior ou menor do que o valor intermediário.

### Recursivo

![[image 1 90.png|image 1 90.png]]

A nossa condição de parada é quando houver apenas um item no intervalo e este seja diferente do buscado. Nesse caso, ocorre o caso base, quando o indicador inferior tem uma posição maior do que o superior (ou vice-versa).

### Complexidade

No pior caso, a complexidade da busca binária é $O(\log n)$, pois dividimos o vetor até haver apenas um elemento (a quantidade de divisões do vetor é o logaritmo).