---
Course:
  - https://www.notion.so/Modelagem-Comp-em-Grafos-313fa7f60cd8809cbb66ff6f47321f6e?pvs=21
Last Edited: 2026-03-09T12:20
---
Um grafo é dito multigrafo quando existe mais de uma aresta ligando dois vértices.

Por efeito de comparação, um grafo normal tem apenas uma aresta ligando os vértices.

![[image 138.png|image 138.png]]

Um grafo cuja arestas ligam-se no mesmo vértice é dito como laço.

![[image 1 105.png|image 1 105.png]]

Vértices são ditos vizinhos quando são os extremos de uma mesma aresta.

![[image 2 84.png|image 2 84.png]]

Por sua vez, duas arestas são ditas vizinhas/adjacentes quando possuírem um mesmo vértice.

  

Um grafo é dito completo se todos os seus vértices forem adjacentes, ou seja, possuem arestas em comuns com todos os vértices.

- Um grafo completo $Kn$ possui $n(n-1)/2$ arestas.

  

![[image 3 71.png|image 3 71.png]]

Um dígrafo (ou grafo orientado) consiste em um conjunto $V$ de vértices e de um conjunto $E$ de arestas com pares ordenados de vértices distintos. Em outras palavras, cada vértice liga-se a um outro vértice exclusivamente.

![[image 4 56.png|image 4 56.png]]

Em um grafo orientado (o sentido da aresta importa), podemos classificar a aresta com relação ao vértice.

- Uma aresta é divergente em relação a um vértice se sua direção for oposta a ele.

- Uma aresta é convergente em relação a um vértice se sua direção for em relação a ele.

![[imagem_2026-03-09_115135522.png]]

  

O grau de um vértice diz respeito à quantidade de vértices adjacentes a ele (ou o número de arestas incidentes sobre ele)

  

Um grafo é cíclico se no caminho entre os vértices eles forem todos distintos, exceto pelo último e pelo primeiro.

[](https://www.notion.soundefined)

### Grafo Hamiltoniano

Caminho Hamiltoniano é aquele que contém cada vértice do grafo exatamente uma vez.

Um ciclo é hamiltoniano se o caminho entre os vértices forem um caminho hamiltoniano.

[](https://www.notion.soundefined)

Um grafo hamiltoniano é aquele que possui um ciclo hamiltoniano.

### Grafo Euleriano

  

  

---

### Bipartido

Há dois conjuntos de vértices $A$ e $B$ com arestas unicamente entre vértices de tipos diferentes.

No tipo bipartido completo, os vértices se conectam a todos os vértices do outro tipo.

![[image 5 40.png|image 5 40.png]]

  

O complemento de um gráfico é o conjunto de arestas que não existe no grafo principal, e que une os vértices que inicialmente não estavam ligados entre si.

Grafos isomorfos possuem o mesmo conjunto de vértices e arestas, preservando a relação de incidência. No sentido gráfico, eles representam uma mesma figura — ainda que em perspectivas diferentes.

  

A definição de árvore é de um grafo conexo (nenhum vértice sem arestas) e acíclico (nenhum vértice com mais de uma aresta).

Outra definição é a de árvore enraizada, a qual consiste em uma árvore com arestas orientadas e que possui um vértice a partir do qual todas as conexões começam.

![[image 6 28.png|image 6 28.png]]

  

O subgrafo consiste em uma parte do grafo principal, preservando as conexões entre _n_ vértices dentre os _k_ vértices do grafo principal.

### Subgrafo gerador

![[image 7 24.png|image 7 24.png]]

Existe um caso específico que é o de árvore geradora. É um subgrafo do grafo principal com o formato de árvore.

---

## Estruturas de Dados

Os grafos podem ser transcritos para código via duas estruturas de dados principais:

- matriz de adjacências

- lista linear de adjacência

### Matriz de Adjacência

![[image 8 18.png|image 8 18.png]]

É uma tabela que marca 1 quando houver aresta entre os vértices de índice da linha e da coluna. POr exemplo, o vértice 1 liga-se ao vértice 2, por isso o valor do quadrinho é 1. Por outro lado, como 1 não liga-se à 3, o valor do quadrinho é 0.

É a forma mais simples de representação, no entanto o seu armazenamento é sempre da ordem $O(n²)$, o que pode ser ruim para grafos com poucas arestas.

### Lista de adjacências

É criada uma lista com todos os vértices, e cada vértice aponta para uma sublista com os vértices aos quais ele liga-se.

![[image 9 12.png|image 9 12.png]]

É uma representação mais elaborada, de complexidade $O(m+n)$

Caminho Euleriano é aquele que contém cada aresta do grafo exatamente uma vez.

Um grafo é Euleriano se há um circuito em G que contenha todas as suas arestas

[](https://www.notion.soundefined)

  

  

Um grafo $G = (V, E)$ é conexo quando existe um caminho entre cada par de vértices de G, caso contrário, $G$ é desconexo. Para um grafo orientado, a decisão é feita SEM considerar a orientação da arestas.

Todo grafo euleriano é conexo e todos os seus vértices possuem grau par

  

### Fortemente conexo

Um grafo orientado $D = (V, E)$ é dito ser fortemente conexo quando existe um caminho entre cada par de vértices $(x,y)$ e também entre $(y,x)$.