---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-12-03T17:33
---
As árvores binárias de busca são estruturas de dados que maximizam o acesso aos nós em razão de uma chave, que funciona como um índice.

- Os nós pertencentes à sub-árvore esquerda possuem valores de chave menores que o valor associado à chave do nó raiz $r$.

- Os nós pertencentes à sub-árvore direita possuem valores de chave maiores que o valor associado à chave do nó raiz $r$.

![[image 120.png|image 120.png]]

- Um percurso em-ordem em uma ABB resulta na sequência de valores em ordem crescente

Uma árvore binária de busca é dinâmica e pode sofrer alterações (inserções e remoções de nós) após ter sido criada.

A árvore binária de busca é ordenada e permite a utilização da busca binária, de forma que verificações para buscar resultados são minimizadas.

## Inserção

![[image 1 92.png|image 1 92.png]]

## Remoção

![[image 2 73.png|image 2 73.png]]

A remoção acontece de forma binária e deve tratar dois casos especiais::

- Se o nó a ser removido tem uma filha apenas;

- Se o nó a ser removido tem duas filhas.

  

No primeiro caso, verificamos se a única filha existente está na esquerda ou na direita, e guardamos seu valor com uma variável temporária. Então removemos o nó mãe a substituímos com a filha.

![[image 3 62.png|image 3 62.png]]

No segundo o tratamento é um pouco mais complexo. Devemos acessar a árvore a partir da filha da direita, e então ir até o nó mais à esquerda. Isso vai garantir o comportamento da árvore de busca (mãe maior que a árvore filha da esquerda e menor que a árvore filha da direita).

![[image 4 51.png|image 4 51.png]]

![[image 5 35.png|image 5 35.png]]

Após buscar o nó de forma recursiva, o algoritmo vai reciclar o nó removido com um novo valor apropriado. Esse novo valor apropriado é o descrito acima. O primeiro passo é ir para a direita e então tentar acessar o nó mais a esquerda, parando quando chegar em `nullptr` .

Então, tendo o valor do nó excluído sido trocado, vamos excluir o nó original do novo valor. Agora chamamos a função recursivamente para o lado direito do nó raiz (o cujo valor foi substituído) e para o valor repetido.

![[image 6 25.png|image 6 25.png]]

### Funções utilitárias

![[image 7 21.png|image 7 21.png]]

A função de contagem funciona recursivamente. Quando chegamos no nó folha, a chamada retorna -1, que ao voltar para a chamada anterior, vai comparar com o outro lado e somar 1. Isso vai acontecer a cada nível, acrescentando 1 a cada chamada.