---
Course:
  - https://www.notion.so/C-lculo-II-24efa7f60cd880b0b8e2ea5108f9eeb0?pvs=21
Last Edited: 2026-02-14T00:34
---
O plano tangente consiste no plano formado pelas retas tangentes formadas pelas derivadas parciais em cada um dos eixos de uma função.

- Todas as retas que passam por aquele ponto específico da curva pertencem ao mesmo plano.

![[image 105.png|image 105.png]]

O vetor gradiente consiste em um vetor pertencente a esse plano e que permite a melhor trajetória para chegar ao vértice no topo do gráfico.

- Em outras palavras, ele indica a reta com a maior taxa de variação no plano tangente.

![[image 1 80.png|image 1 80.png]]

## Calculando o vetor gradiente

![[image 2 64.png|image 2 64.png]]

Essa definição também pode aparecer simplesmente como f(x, y), e significa que primeiro encontramos a derivada parcial em relação à x e depois em relação à y.

O vetor gradiente então terá como componentes as duas derivadas parciais.

---

## Plano Tangente e Reta Normal

![[image 3 55.png|image 3 55.png]]

Para chegar nisso, consideramos $x+h = x$ e $y+k=y$.

==**Observe que só definimos plano tangente em (x0, y0, f(x0, y0)) se f for diferenciável em (x0, y0). Se f não for diferenciável em (x0, y0), mas admitir derivadas parciais neste ponto, então o plano existirá, mas não será plano tangente.**==

Ao escrevermos essa equação em termos de produto escalar, concluímos que o plano é perpendicular ao vetor…

![[image 4 46.png|image 4 46.png]]

A reta que passa pelo ponto $(x0, y0, f(x0, y0))$ e é paralela ao vetor denomina-se reta normal ao gráfico de f no ponto $(x0, y0, f(x0, y0))$. A equação de tal reta é:

![[image 5 32.png|image 5 32.png]]

---