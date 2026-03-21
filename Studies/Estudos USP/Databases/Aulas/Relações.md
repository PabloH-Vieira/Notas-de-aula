---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-09-02T22:16
---
Conceito;

Funções como relações, propriedades, equivalências, ordens parcial e total: e o problema da Arrumação da Estante;

## Relações

Dados dois conjuntos X,Y, chamamos de **relação de X em Y o conjunto R** contido no produto cartesiano $X \times Y$.

Para citar um par (x,y) pertencente à R dizemos $xRy$.

![[image 68.png|image 68.png]]

Uma função representada através de um gráfico é um exemplo de relação, pois corresponde a um conjunto de pontos determinado pelo produto cartesiano entre os conjuntos do domínio e do contradomínio.

### Tipos de Relações

- ==**Reflexiva**==, se $\forall x \in X$ vale $xRx$.
    
    - gráfico com comportamento diagonal.
    
    ![[image 1 51.png|image 1 51.png]]
    

- ==**Simétrica**==, se $xRy$ vale também $yRx$.
    
    - o gráfico tem um formato simétrico.
    
    - se existe uma relação de x para y e também o inverso.
    

- ==**Antissimétrica**==, se $xRy \wedge yRx \Longrightarrow$ $x=y$.
    
    - existe uma relação de x que também vale para y, de forma que ambos sejam iguais.
    
    - vale também essa relação quando a hipótese é falsa, o que faz com que qualquer tese seja verdadeira (tabela verdade do AND).
        
        - $xRy \Longleftrightarrow$ $x<y$ é um exemplo de antissimetria, pois essa relação não pode ser aplicada aos dois casos.
        
    
    - Poder haver uma relação tanto de simetria quanto de antissimetria para dois mesmos conjuntos.
    

- ==**Transitiva**==, se ($xRy \wedge yRz$) $\Longrightarrow xRz$

## Relações de Equivalência

Uma relação de equivalência é aquela que vale as três relações: ==**reflexiva, simétrica e transitiva**==.

![[image 2 42.png|image 2 42.png]]

- Vale apenas uma relação entre classes de equivalência: ou elas têm os mesmos elementos entre si, ou não há nenhum elemento em comum.

- Uma partição é uma reunião de conjuntos disjuntos cuja reunião dá o conjunto inteiro.

![[image 3 35.png|image 3 35.png]]

- Se existe uma partição de um conjunto, é possível definir uma classe de equivalência, isto é, uma relação de equivalência entre os elementos daquela partição.

- A classe de equivalência contém todas as formas de relações entre os elementos relacionados.

![[image 4 31.png|image 4 31.png]]

### Relações de Ordem

Dizemos que existe uma relação de ordem parcial se houver relação ==**reflexiva, antissimétrica e transitiva.**==

Existe uma relação de ordem total se ela é uma relação de ordem parcial e também valer que $\forall x, y \in X$ vale ($xRy \vee yRx$).

Dizemos, em cada um desses casos, que o conjunto é parcialmente ou totalmente ordenado.