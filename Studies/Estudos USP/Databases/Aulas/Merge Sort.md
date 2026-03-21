---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-II-24efa7f60cd880bbbbcaf479fda73ab6?pvs=21
Last Edited: 2025-11-15T01:42
---
É um algoritmo muito apropriado para listas encadeadas, de forma a transformá-las em listas ordenadas.

Consiste em dividir para conquistar, primeiro dividindo a lista em partes e depois realizar um _merge_ de forma que a lista fique ordenada.

- Separamos de dois em dois recursivamente até que, ao final, cada nó esteja sozinho.

## Separando a lista

A lógica para separar a lista utiliza dois ponteiros, geralmente nomeados como _slow_ e _fast._

- _fast_ sempre avança caso exista um valor no seu nó e também no nó seguinte. Caso essa condição seja satisfeita, ele avança duas posições.

- _slow_ também avança sempre que a condição for atendida, mas ele avança somente uma posição.

Essa lógica de avanço diferente para cada ponteiro faz com que, quando _fast_ chegar ao final da lista, _slow_ esteja exatamente no meio. Desta forma, podemos separar a lista em duas partes.

![[image 114.png|image 114.png]]

Como isso ocorre recursivamente, essa divisão acontece até que os nós fiquem individuais.

## Realizando o _merge_

O _merge_ segue a lógica contrária. A ideia agora é ir montando listas ordenadas que crescem a cada iteração até que cheguemos à lista original, agora ordenada.

- Definimos dois ponteiros, um para cada lista. No caso mais baixo, quando os nós estão sozinhos, os ponteiros apontam um para cada nó.

- Comparamos os ponteiros, colocando o menor à direita e o maior à esquerda, para o caso de nós inferiores. Essa comparação é sempre na ordem de $2^n$ (no primeiro caso são 2 nós apenas).

- No próximo passo, vamos comparar listas com dois nós cada. Definimos ponteiros para cada lista, iniciando no primeiro nó. A seguir comparamos os nós, o de menor valor será o primeiro elemento da lista formada, e o ponteiro corresponde avança um nó.

- Realiza-se essa comparação entre os ponteiros até que eles cheguem em _null_ (a lista acabou).

- Isso é feito recursivamente até que cheguemos na lista com todos os nós.