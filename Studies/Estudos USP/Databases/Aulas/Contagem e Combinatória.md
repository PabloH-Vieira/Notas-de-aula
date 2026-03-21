---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-09-02T22:16
---
Princípios de adição;

Princípios do produto;

Listas;

Fatorial;

Arranjo;

Permutações;

Combinações, com e sem repetição de elementos;

Subconjuntos e triângulo de Pascal.

---

## Introdução

Um conjunto é uma coleção de objetos, sejam eles números ou objetos propriamente.

Um conjunto complementar diz respeito a todos os elementos não pertencentes ao conjunto original. Por exemplo, o complementar de A = {1,2,34} nos naturais é um conjunto infinito, que não inclui {1,2,3,4}.

### Definições

- A cardinalidade de um conjunto é o número de elementos no conjunto.

- Conjuntos disjuntos não possuem elementos em comum.

- Uma família de conjuntos são mutuamente disjuntos quando tomados dois a dois. Sua representação é {$A\footnotesize{i}$}${\footnotesize{i=1,2,3}}$ quando a família contém $A{\footnotesize{1}}$, $A{\footnotesize{2}}$, $A{\footnotesize{3}}$.

![[image 69.png|image 69.png]]

## Princípio de Adição

Consideramos uma família de conjunto finita, cujo seus conjuntos são finitos e mutuamente disjuntos.

A cardinalidade da reunião desses conjuntos é a soma da cardinalidade de cada um dos conjuntos.

![[image 1 52.png|image 1 52.png]]

Sendo cardinalidade representado pelo módulo. Para dizer que estamos operando conjuntos disjuntos usamos $\prod$ para união e $\coprod$ para intersecção.

Chamamos de partição de A uma família de subconjuntos de A que sejam disjuntos e ao serem reunidos formam todo o conjunto A.

- Cada conjunto nessa família é chamado de bloco da partição.

- Dada uma partição de um conjunto A, a cardinalidade de A é a soma da cardinalidade dos blocos de partição.

## Princípio do Produto

Tomamos uma família formada _**N**_ por conjuntos finitos, e cada um dos conjuntos são mutuamente disjuntos e possuem uma mesma cardinalidade _**M.**_

Então a cardinalidade da família será igual ao produto _**MN.**_

![[image 2 43.png|image 2 43.png]]

Podemos denotar essa propriedade em termos de produto cartesiano de conjuntos finitos.

- O produto cartesiano forma um novo conjunto cujos elementos possuem como par ordenado: primeiro os valores do primeiro conjunto e segundo os valores do segundo conjunto.

- As duplas não estão fixadas, podemos variar o valor da segunda coordenada (_b_) para cada valor da primeira (_a_).

- Então a cardinalidade da família formada pelo produto $A \times B$ será o produto entre os conjuntos $|A \times B| = |A|*|B|$

![[image 3 36.png|image 3 36.png]]

Também podemos concluir que a cardinalidade de uma família composta por _**N**_ conjuntos é o produtório da cardinalidade de cada conjunto, que também pode ser entendido como o produto cartesiano de cada conjunto.

- O resultado desse produto escalar é um conjunto de vetores com _n_ coordenadas, variando as coordenadas pertencentes a cada conjunto.

![[image 4 32.png|image 4 32.png]]

![[image 5 22.png|image 5 22.png]]

## Princípio da Bijeção

Tomando dois conjuntos _**A**_ e _**B**_ eles só tem a mesma cardinalidade se e somente se existir uma bijeção entre os conjuntos.

- Uma propriedade leva à outra: se eles são bijetores, eles têm a mesma cardinalidade, e vice-versa.

---

![[image 6 15.png|image 6 15.png]]

Nesse exercício, é perguntado quantos seguimentos orientados podem ser formados pelos vértices pertencentes a um conjunto V.

- Um seguimento orientado precisa de dois vértices, um de início _a_ e um de fim _b._

A quantidade possível de seguimentos consiste no conjunto de duplas possíveis entre os vértices.

- Denotamos isso como a união entre os pontos _a_ e os pontos _b,_ tal que _b_ não pode ser _a._

- Então, a resposta que procuramos é justamente a cardinalidade dessa união. A cardinalidade de cada vértice é _n-1_, sendo _n_ a quantidade de vértices. Portanto, a resposta é, usando o princípio do produto, _n(n-1)/2_, pois não iremos contar o mesmo seguimento duas vezes, apenas mudando o ponto de início e final.

---

## Lista

É uma lista ordenada de _k_ objetos, escolhidos num conjunto de _N_ elementos.

- Alterar a ordem dos elementos altera a lista.

![[image 7 13.png|image 7 13.png]]

## Permutações

São listas, mas sem repetições de elementos, escolhidos _k_ objetos em um conjunto de _N_ elementos.

- Correspondem às funções injetoras.

![[image 8 10.png|image 8 10.png]]

---

## Combinações

Correspondem aos subconjuntos de _k_ elementos, de um conjunto de _N_ elementos.

- Aqui a ordem não importa (_ab = ba_), estamos pensando unicamente nos elementos.

![[image 9 6.png|image 9 6.png]]

---

### Complemento do Princípio do Produto

![[image 10 4.png|image 10 4.png]]

Podemos utilizar essa propriedade nas permutações.

- Utilizamos o produtório do primeiro elemento (_n_ maneiras) até o _k-ésimo_ elemento (_n-k+1_).

![[image 11 3.png|image 11 3.png]]

---