---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-II-24efa7f60cd880bbbbcaf479fda73ab6?pvs=21
Last Edited: 2025-11-16T23:37
---
### O que é Heap?

É uma estrutura de dados usada para ordenação e lista de prioridades. Pode ser visualizada como uma árvore binária com um formato específico. é uma árvore quase cheia, e totalmente balanceada.

- Para encontrar o filho na esquerda de qualquer célula, calculamos $2i$, sendo $i$ o índice da célula mãe.

- Para encontrar o filho na direita, calculamos $2i+1$.

- Isso quando alocamos a célula raiz na posição 1 do vetor. Isso implica em deixar o índice 0 vazio.
    
    - se o índice 0 for a raiz, basta somar +1 no cálculo tanto da esquerda, quanto da direita.
    

Podemos ordenar o heap de duas formas:

- De forma que os maiores valores estejam em níveis primários e os menores em níveis inferiores.

- De forma que os maiores estejam em níveis inferiores e os menores em níveis primários.

Podemos sempre reorganizar a _heap_ para um modo ou outro.

- Como fazer isso? Algoritmo.

### Como criar uma _heap_ a partir de um _array_ desordenado?

Implementamos isso com um algoritmo recursivo, de modo que a cada nível da árvore, comparamos os filhos com a sua mãe. Se uma das filhas for maior que a mãe, trocamos de lugar.

- A cada nível, comparamos a mãe com as filhas. A filha de maior valor (caso as duas sejam maiores) sobe.

Quando removemos a raiz, devemos reordenar a _heap._ Para isso, colocamos na raiz o valor mais a direita da árvore. Isso faz com que comparemos nível a nível mais uma vez e que o maior valor suba até a raiz e o menor desça.

Não necessariamente o menor valor é o elemento mais a direita. A condição é que o nó mãe seja maior que os nós filhas.

![[image 115.png|image 115.png]]

### Ordenação

A etapa de ordenação ocorre depois de criarmos uma _heap_ organizada de forma que o maior valor esteja na raiz.

O próximo passo é trocar de lugar a raiz com o valor mais a direita, do último nível. Pensando em um vetor, estamos trocando a primeira posição com a última.

- Para realizar a comparação entre o elemento mais a direita e o seu nó mãe, acessamos o nó mãe como o índice correspondente a (_i/2)-1_ sendo _i_ o índice de maior número.

- Os passos seguintes, para ir subindo o valor, é ir comparando as células de índice menores que (_i/2)-1_ até que cheguemos ao índice 0.

Agora que o maior valor está no final, tiramos ele da nossa _heap_. O passo agora é reordenar a _heap_ de forma que o menor valor volte para o seu nível e que o segundo maior valor (na _heap_ o maior, já que estamos desconsiderando o maior do vetor) suba até a raiz.

Novamente, invertemos o menor e a raiz de lugar. O segundo maior valor vai parar na última posição do vetor, como é apropriado.

Repete-se todos esses passos até que o menor valor seja o único na árvore.

![[image 1 88.png|image 1 88.png]]

### Inserindo um item na _heap_

Inserir um item na _heap_ segue uma lógica diferente da ordenação. Ao invés de realizarmos comparações de cima para baixo, aqui a comparação é de baixo para cima.

  

### Complexidade

A complexidade é $O(n\log{n})$, pois reordenar a _heap_ de forma que o maior valor suba até a raiz custa $\log{n}$ e realizamos isso no máximo $n$ vezes.