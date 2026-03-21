---
Course:
  - https://www.notion.so/C-lculo-II-24efa7f60cd880b0b8e2ea5108f9eeb0?pvs=21
Last Edited: 2025-11-28T22:30
---
## Fórmula de Taylor com Resto de Lagrange

![[image 109.png|image 109.png]]

![[image 1 84.png|image 1 84.png]]

Podemos reescrever essa função determinando $h=x-x\footnotesize{}0$ e $k=y-y\footnotesize{0}$, de forma que observamos essa função se aproximar muito da equação do plano tangente. Essa função, dada por $L(x,y)$ é chamada de aproximação linear.

$$L(x,y)=f(x0,y0)+\frac{\partial f}{\partial x}(x0,y0)*(x-x0)+\frac{\partial f}{\partial y}(x0,y0)*(y-y0)$$

Chegamos então na forma de um polinômio de Taylor somado com um erro, o resto de Lagrange, sendo esse erro uma estimativa dada por

$$E(x,y)=\frac{[(x-x0)\frac{\partial}{\partial x}+(y-y0)\frac{\partial}{\partial y}]^{n+1}}{(n+1)!} * f(\overline{x},\overline{y})$$

Onde x e y barrados pertencem ao segmento da reta que une ($x0,y0$) a $(x,y)$.

Outra notação possível é:

$$E(x,y)=\frac{f^{n+1}(k)}{(n+1)!} * (x-c)^{n+1}$$

Onde $c$ é o ponto onde a função está centrada e $k$ é um valor aproximado do nosso $x0$.

Podemos expandir esse termo, considerando $n+1=2$, e então caímos em um produto notável, sendo que cada termo da expansão multiplicará por $f.$ Nessa multiplicação, os valores de $x$ e $y$ não devem ser alterados de maneira alguma, tanto é que podemos reescrevemos como $h$ e $k$

### Resumo

![[image 2 67.png|image 2 67.png]]

![[image 3 58.png|image 3 58.png]]