---
Course:
  - https://www.notion.so/C-lculo-II-24efa7f60cd880b0b8e2ea5108f9eeb0?pvs=21
Last Edited: 2025-11-23T22:14
---
No estudo de curvas, retas tangentes e retas normais, podemos descrever esses elementos de duas formas: equação paramétrica e equação cartesiana.

A equação paramétrica tem a forma: $r(t)=(a,b)+t(p,q)$, sendo $a$ e $b$ um ponto pertencente à curva e $p,q$ os pontos do vetor diretor.

A equação cartesiana tem a forma: $A(x-x{\footnotesize{0}})+B(y-y{\footnotesize{0}})=0$, sendo $A$ e $B$ as coordenadas de um vetor ortogonal à curva e $x{\footnotesize{0}}$, $y{\footnotesize{0}}$ um ponto pertencente à curva.

Para agilizar, o vetor gradiente sempre vai ser paralelo à reta normal, de forma que podemos utilizá-lo para definir a função da normal.

## Derivadas Direcionais

A derivada direcional diz respeito à variação de uma função em uma direção dada por um vetor $\vec{u}$.

- Esse vetor é unitário, isto é, tem norma 1.

A fórmula para calcular essa derivada utiliza os eixos $x$ e $y$.

![[image 107.png|image 107.png]]

![[image 1 82.png|image 1 82.png]]

Na imagem, é possível ver que traçamos um plano que corta a função em relação ao vetor $\vec{u}$ e então encontramos a inclinação da reta formada no ponto em que a curva toca o plano. No exemplo, essa reta passa pelo ponto $P$.

### Derivada direcional em razão do vetor gradiente

![[image 2 66.png|image 2 66.png]]

Fazemos o produto escalar entre o vetor gradiente de $f$ nos pontos $x\footnotesize{0}$ e $y\footnotesize{0}$ e o vetor $\vec{u}$

![[image 3 57.png|image 3 57.png]]

Quando andamos sobre o vetor gradiente, estamos pegando os pontos com a maior taxa de variação da função.