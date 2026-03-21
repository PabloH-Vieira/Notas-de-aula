---
Course:
  - https://www.notion.so/C-lculo-II-24efa7f60cd880b0b8e2ea5108f9eeb0?pvs=21
Last Edited: 2025-11-28T22:30
---
## Matriz Hessiana

A matriz hessiana consiste em uma matriz que guarda as derivadas parciais de ordens superiores, de forma semelhante ao vetor gradiente (guarda as derivadas parciais de primeira ordem).

O tamanho da matriz será igual ao grau da derivada parcial. Uma matriz hessiana de derivadas de ordem 3 terá tamanho 3x3.

Caso as derivadas mistas coincidam, a matriz será dita simétrica.

## Método dos Multiplicadores de Lagrange

### Uma restrição

Nesse método, buscamos encontrar os valores máximos de uma função quando seu domínio está restrito a uma curva no eixos $x$ e $y$.

![[image 110.png|image 110.png]]

O passo seguinte é realizar cortes horizontais, definindo assim curvas de níveis, da função $f$, e compará-las com a curva em vermelho, a $g(x,y)$.

- Daí, buscamos a curva de nível mais externa a tocar a curva de $g(x,y)$, definindo o ponto máximo.

- Daí, buscamos a curva de nível mais interna a tocar a curva de $g(x,y)$, definindo o ponto mínimo.

Essas curvas que se tocam são, por definição, tangentes entre si, permitindo aplicar algumas propriedades.

- A primeira delas é que, no ponto de tangência, os vetores gradientes de cada função são paralelos entre si.

![[image 1 85.png|image 1 85.png]]

Então cabe o teorema:

![[image 2 68.png|image 2 68.png]]

No entanto, devemos encontrar o ponto de máxima e mínima tangência, o que se faz possível através do método dos multiplicadores de Lagrange.

![[image 3 59.png|image 3 59.png]]

O mesmo método se aplica às funções com três variáveis.

No passo a passo, montamos um sistema com a primeira coordenada do gradiente de $f$ sendo igual a um múltiplo da primeira coordenada do gradiente de $g$; a segunda equação sendo semelhante à primeira, mas com relação às coordenadas dos gradientes no eixo $y$; e a terceira coordenada a função $g(x,y)=k$.

- Daí, calculamos possíveis soluções em uma das equações, e aplicamos o valor nas demais equações, encontrando os valores das variáveis restantes.

- Então, para todas as possíveis soluções encontradas, substítuimos os valores de $x$ e $y$ em $f$ e calculamos os resultados.

- Definimos os resultados de maior valor como os pontos máximos e os de menor valor como pontos mínimos.

### Ponto Crítico

Os pontos onde encontramos os máximos ou mínimos locais em um intervalo $(a,b)$ tem derivadas parciais iguais a zero, se elas existirem.

- Nem todos os pontos críticos (pontos onde as derivadas são iguais a zero) são o máximo ou mínimo.

![[image 4 48.png|image 4 48.png]]

No entanto, existe uma forma de verificar se de fato esse ponto é um ponto mínimo ou máximo, através da matriz hessiana e das derivadas de ordem dois.

![[image 5 33.png|image 5 33.png]]

**Ponto de sela**

É um ponto onde, em uma direção a curvatura da função, e em outra direção, temos uma outra curvatura, de forma que é impossível determinar se o ponto é mínimo ou máximo (é máximo em uma direção e mínimo em outra).

![[image 6 23.png|image 6 23.png]]

## Funções com Domínios Restritos

Em funções com domínio restrito não basta aplicar o método da matriz hessiana.

Para uma função f de uma variável, o Teorema do Valor Extremo diz que, se f é contí-nua em um intervalo fechado [a, b], então f tem um valor mínimo absoluto e um valor máximo absoluto. De acordo com o Método dos Intervalos Fechados da Seção 4.1, no Volume 1, achamos esses valores calculando f não somente nos pontos críticos, mas também nas extremidades a e b.

Para as funções de duas variáveis, a situação é semelhante. Do mesmo modo que os intervalos fechados contêm suas extremidades, um conjunto fechado de $\mathbb{R}^2$ contém todos os seus pontos da fronteira.

![[image 7 19.png|image 7 19.png]]

Em funções cujo gráfico consiste em figuras planas, devemos seguir um passo a passo:

- Calcular os pontos críticos.

- Definir retas que formem a figura, ou curvas etc.

- Nessas curvas, alguns pontos estarão fixos, e outros, variando (isso vai depender da direção da reta).

- Então, aplicamos em $f(x,y)$ a constante e a variável, e estudamos qual é o ponto máximo e mínimo daquela reta.

- Ao final, comparamos todos os pontos encontrados aplicados na função e definimos o máximo e mínimo global.

**Exemplo (note os pontos fixos nas equações das retas)**

![[image 8 15.png|image 8 15.png]]

No exemplo, o máximo global é $f(3,0)=9$ e o mínimo é $f(2,2)=0$.