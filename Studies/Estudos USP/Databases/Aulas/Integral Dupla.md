---
Course:
  - https://www.notion.so/C-lculo-III-313fa7f60cd880d2a072c0acf7a9fdec?pvs=21
Last Edited: 2026-03-03T16:08
---
Definimos a integral simples como a soma de Riemann quando o maior subintervalo da soma tende a 0 e, por consequência, todos os demais.

![[image 140.png|image 140.png]]

Já a integral dupla consiste em aproximar a área dos subintervalos de 0, o que se dá a partir do limite de $\Delta \rightarrow 0$, sendo esse o mesmo delta de $\Delta{x}$ e $\Delta{y}$. Caso esse limite exista, ele é único e chamado de $K$.

![[image 1 107.png|image 1 107.png]]

Se $K$ existir, dizemos que $f$ é integrável no intervalo $A$

![[image 2 86.png|image 2 86.png]]

## Condição de integrabilidade

### Conjuntos de conteúdo nulo

Sobre conjuntos nulos. É importante notar que a área desse conjunto é zero.

![[image 3 73.png|image 3 73.png]]

Em outras palavras, o A é composto por um número finito de retângulos tão pequenos que tendem a zero.

![[image 4 58.png|image 4 58.png]]

### Limites de fronteira

![[image 5 41.png|image 5 41.png]]

O conjunto de todos os pontos de fronteira compõe a chamada fronteira do conjunto A.

## Teorema de Fubini

O Teorema de Fubini permite calcular uma integral dupla a partir de uma integral simples.

![[image 6 29.png|image 6 29.png]]

Nesse método, fixamos uma das variáveis que compõem a integral dupla (no exemplo, o volume sob a figura) e calculamos uma função que gera a área com relação àquele ponto fixo sob o gráfico.

- Trata-se de uma função com apenas uma variável, mas que ainda depende do ponto fixado.

No fim, o volume será o somatório de todas as áreas geradas quando fixamos um ponto em um dos eixos. Na verdade, geramos um volume a partir dessas áreas, que quando somadas resultarão no volume final.

Esses volumes gerados a partir das áreas são dados por:

![[image 7 25.png|image 7 25.png]]

![[image 8 19.png|image 8 19.png]]

Basicamente, integramos primeiro uma integral simples com uma das variáveis fixada, e a função gerada a partir disso, $g(x)$, é novamente integrada, agora em relação àquela variável fixada anteriormente.

**Exemplo**

![[image 9 13.png|image 9 13.png]]


A escolha por integrar primeiro uma variável ou outra deve ser estratégica. Um macete é observar qual das variáveis descreve uma mesma função ao longo do contradomínio. Se observamos o gráfico e percebermos que teremos que dividir a integral em duas partes, pois o contradomínio descreve duas funções, então é uma má ideia começar por aquela variável.
![[Pasted image 20260316084256.png|524]]
Nesse exemplo, o gráfico com relação a x não permanece a mesma durante o gráfico. Na verdade, ela é um retângulo, e depois um semicírculo. Por outro lado, y permanece um retângulo com um dos lados em curva (a mesma função). A melhor decisão é começar por y.

## Coordenadas polares
