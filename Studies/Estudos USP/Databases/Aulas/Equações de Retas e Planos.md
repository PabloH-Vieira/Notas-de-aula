---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
Tomamos uma reta r e um vetor ${\vec{u}}$ paralelo a ela.

- O vetor é chamado de vetor diretor.

Tomando um ponto x qualquer no espaço, só podemos concluir que ele pertence a reta se o vetor definido por x e um ponto da reta for paralelo ao vetor $\vec{u}$. Por isso, os vetores devem ser LD.

## Equação Vetorial da Reta

$$x=A+{\lambda}{\vec{u}}$$

- A: ponto fixo pertencente a reta.

Não havendo um vetor, podemos definir um vetor diretor a partir de dois pontos pertencentes a reta.

- Para formar um vetor entre dois pontos, subtraímos as coordenadas, ${\vec{AB}}=B-A$

## Equações Paramétricas da Reta

Tomando a equação inicial $x=A+{\lambda}{\vec{u}}$, podemos montar um sistema tomando as coordenadas de cada desses valores.

- x=(x, y, z)

- A= (x0, y0, z0)

- ${\vec{u}}$=(a, b, c)

Podemos realizar a soma coordenada a coordenada, isto é $(x, y, z)=(x0, y0, z0)+{\lambda}(a, b, c)$.

![[image 18.png|image 18.png]]

## Equações Simétricas da Reta

![[image 1 8.png|image 1 8.png]]

As equações simétricas são obtidas isolando ${\lambda}$ em cada uma das equações paramétricas.

# Planos

Para definir um plano, tomamos dois vetores ${\vec{u}}$ e ${\vec{v}}$ L.I entre si e dois pontos A e X pertencentes ao plano.

Para que um vetor ${\pi}$ exista é necessário que os vetores ${\vec{u}}$, ${\vec{v}}$ e ${\vec{AX}}$ sejam LD entre si.

Para definir ${\vec{AX}}$ usamos os outros vetores de forma que:

$${\vec{AX}}={\lambda}{\vec{u}}+{\delta}{\vec{v}}$$

- Sendo ${\lambda}$ e ${\delta}$ dois números reais.

Isolando X chegamos a equação vetorial do plano:

$$X=A+{\lambda}{\vec{u}}+{\delta}{\vec{v}}$$

- Ao contrário da equação da reta, a equação do plano tem dois vetores diretores.

Semelhante a reta, podemos obter as equações paramétricas do plano.

![[image 2 6.png|image 2 6.png]]

## Equação Geral do Plano

$$ax+by+cz+d=0$$

- a, b, c, d são números reais

- x, y, z são coordenadas.

## Vetor normal ao plano

Vetores normais são ortogonais a qualquer vetor que seja paralelo ao plano ${\pi}$.

O conceito de vetor normal é importante para o conteúdo a seguir.

  

Para saber se um determinado ponto pertence ao plano o vetor formado por ele e um ponto fixo do plano deve ser ortogonal a um vetor normal ao plano.

${\vec{h}}*{\vec{AX}}=0$

Ao desenvolver esse produto chegamos à equação geral do plano.

  

Observamos, por fim, que as coordenadas do vetor normal ao plano pode ser encontrado nos coeficientes a, b e c da equação geral do plano.

${\vec{h}}=(a, b, c)$

### Exemplo

$2x+3y+6z-6=0$

${\vec{h}}=(2, 3, 6)$

  

Além disso, o vetor diretor é resultado do produto vetorial dos vetores diretores do plano.

$\vec{n}={\vec{u}}{\times}{\vec{v}}$