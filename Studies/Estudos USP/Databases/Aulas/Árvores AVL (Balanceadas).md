---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-12-03T21:22
---
Altura de uma árvore binária (AB): igual à profundidade, ou nível máximo, de suas folhas

- A eficiência da busca em árvore depende do seu balanceamento

- Algoritmos de inserção e remoção em ABB não garantem que a árvore gerada a cada passo seja balanceada

Na árvore AVL o fator de balanceamento é sempre 1, -1 ou 0. Isso significa que a altura da subárvore de um lado tem no máximo 1 de diferença com relação ao outro lado.

![[image 119.png|image 119.png]]

- Perceba que nós filhos de uma mesma raiz tem no máximo uma linha de diferença.

Um problema das árvores balanceadas é garantir que elas mantenham o seu comportamento após inserções ou remoções.

  

Para manter uma árvore balanceada é necessário aplicar uma transformação na árvore tal que

1. O percurso em-ordem na árvore transformada seja igual ao da árvore original (isto é, a árvore transformada continua sendo uma ABB)

1. A árvore transformada fique balanceada

A transformação que mantém a árvore balanceada é chamada de rotação

- A rotação pode ser feita à esquerda ou à direita, dependendo do desbalanceamento a ser tratado

- Em alguns casos, é necessário fazer mais de uma rotação

### Rotação à esquerda

![[image 1 91.png|image 1 91.png]]

Na rotação à esquerda, o filho da direita da raiz sobe para se tornar a raiz. Caso esse nó possua uma subárvore, esta vai se tornar o filho da direita da antiga raiz, que agora encontra-se do lado esquerdo.

A rotação à direita é análoga, de forma que a antiga raiz é deslocada para a direita, e caso o antigo nó filho tivesse um filho, esse vai ser o filho da esquerda da antiga raiz.

![[image 2 72.png|image 2 72.png]]

É possível diagnosticar quando uma rotação dupla é necessária. Vamos olhar para o fator de balanceamento: caso o nó raiz tenha um FB positivo e seu nó filho um FB negativo, então é necessário uma rotação dupla.

![[image 3 61.png|image 3 61.png]]

### Dupla à esquerda

![[image 4 50.png|image 4 50.png]]

### Dupla à direita

![[image 5 34.png|image 5 34.png]]

### Determinando as rotações

![[image 6 24.png|image 6 24.png]]

### Implementação da rotação

![[image 7 20.png|image 7 20.png]]

### Inserção

![[image 8 16.png|image 8 16.png]]

Basicamente inserimos na árvore de forma que mantemos o formato ABB e depois balanceamos chamando a função.

![[image 9 11.png|image 9 11.png]]

A lógica de remoção permanece a mesma da ABB.