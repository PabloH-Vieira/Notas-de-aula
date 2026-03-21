---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-II-24efa7f60cd880bbbbcaf479fda73ab6?pvs=21
Last Edited: 2025-11-16T15:04
---
Notação

A notação assintótuica presume uam outra função multiplicada por uma constante para estabelecer uma ordem entre duas funções:

f(n) = cg(n)

As notações existentes são:

- $O$: limitada superiormente.

- $\Omega$: limitada inferiormente

- $\theta:$ mesma ordem

Para determinar a ordem, então, comparamos com uma outra função multiplicada por uma constante, e verificamos a desigualdade. Se existir uma constante que permita a desigualdade ser verdadeira, então podemos estabelecer aquela relação.

## Método da Árvore

No método da árvore, devemos fazer uma tabela que reúne as regras para calcular:

- quantidade de níveis;

- tamanho do problema no último nível;

- quantidade de nós;

- tempo por nó;

Na equação da recorrência $T(n)=aT(n/c)+f(n)$ podemos extrair algumas informações:

- $a$ é a quantidade de vezes em que o problema é dividido a cada nível. Começa com a raiz, e o próximo nível terá $a$ nós. O outro, $a²$ e por aí vai.

- $T(n/c)$ indica o tamanho dos nós a cada nível. Na raiz, é $n$. No próximo, será $n/c$, e depois $n/c²$, e por aí vai.

- $f(n)$ indica o tempo gasto por cada nó.

- O tamanho no último nível sempre será igual a 1.

![[image 111.png|image 111.png]]

A partir da tabela, podemos encontrar a quantidade de níveis em função do tamanho. Calculamos a função generalizada do tamanho e igualamos a 1 (último nível), resultando na quantidade de vezes que o tamanho foi reduzido.

A quantidade de nós é encontrada em razão da quantidade de níveis. Calculamos a função generalizada de nós por nível e aplicamos a quantidade de níveis final.

![[image 1 86.png|image 1 86.png]]

Na função da quantidade de nós, podemos trocar o $2$ e o $n$ de posições, chegando a $n^{\log_{2}{3}}$.

Para calcular o tempo fazemos o somatório do tempo gasto por cada nó, para cada nível.

No exemplo, encontramos o tempo $\sum_{i=0}^{\log_{3}{n}}2^i$

- O somatório de uma constante maior do que 1 pode ser reescrito como a constante elevada ao máximo da somatório +1, menos um sobre a constante menos um, isto é:

$$\frac{2^{\log_{3}{n}+1}-1}{2-1}$$

## Método Mestre

O método mestre pode ser aplicado quando existe uma divisão na função, e a expressão com o seguinte formato:

![[image 2 69.png|image 2 69.png]]

Além disso, é necessário memorizar três diferentes casos:

![[image 3 60.png|image 3 60.png]]

### Versão Simplificada

![[image 4 49.png|image 4 49.png]]

Nesse caso, consideramos a expressão como $T(n)=aT(\frac{n}{b})+\Theta(n^k)$