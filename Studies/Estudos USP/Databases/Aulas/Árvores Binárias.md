---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-12-04T07:22
---
Árvores binárias são estruturas de dados compostas por nós organizados de forma hierárquica. O principal nó chama-se raiz e assim como suas filhas, possui outras árvores à direita e à esquerda. Os nós que se encontram no último nível são chamados de nós folhas.

### Árvore estritamente binária

A árvore estritamente binária tem como característica o fato de que os nós tem dois nós filhos ou nenhum.

![[image 122.png|image 122.png]]

### Árvore binária cheia

A árvore binária cheia tem como característica o fato de que todos os nós filhos estão no mesmo nível.

- Nesse tipo de árvore podemos saber a quantidade total de nós em razão da profundidade $d$, calculando $2^{d+1}-1$.
    
    - seja $d=3$, então para $d=1, n = 1$, para $d=2, n=3$…
    
    - manipulando a expressão, chegamos que $d={\log_{2}(n+1)}-1$
    

![[image 1 93.png|image 1 93.png]]

### Árvore perfeitamente balanceada

- Para cada nó, o número de nós de suas subárvores esquerda e direita difere em, no máximo, 1.

![[image 2 74.png|image 2 74.png]]

### Árvore balanceada

- Para cada nó, as alturas de suas duas subárvores diferem de, no máximo, 1.

![[image 3 63.png|image 3 63.png]]