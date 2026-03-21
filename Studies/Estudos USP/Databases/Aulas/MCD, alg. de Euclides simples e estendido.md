---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-09-25T19:05
---
## MCD: máximo comum divisor

![[image 77.png|image 77.png]]

![[image 1 58.png|image 1 58.png]]

- Fatores em comum aparecem dos dois lados da igualdade.

![[image 2 48.png|image 2 48.png]]

**Exemplo**

![[image 3 41.png|image 3 41.png]]

O algoritmo de Euclides pode ser muito útil para calcular o MCD de dois números, a cada passo aplicando o resto do módulo entre os dois números anteriores.

- A complexidade acaba sendo $2log{\tiny{2}}n$, o que é extremamente eficiente.

O ponto central é que: **"a cada dois passos, o 2º termo do MCD divide por dois (pelo menos)"**.

Vamos provar isso considerando dois passos do algoritmo com `MCD(a, b)`, onde `a &gt; b`:

1. **Passo 1:** `MCD(b, r₁)`, onde `r₁ = a mod b` e `r₁ &lt; b`.

1. **Passo 2:** `MCD(r₁, r₂)`, onde `r₂ = b mod r₁` e `r₂ &lt; r₁`.

Precisamos mostrar que `r₂ &lt; b/2` em dois casos:

- **Caso 1:** Se `r₁ ≤ b/2`, como `r₂ &lt; r₁`, então `r₂ &lt; b/2`.

- **Caso 2:** Se `r₁ &gt; b/2`, o quociente de `b mod r₁` é 1, logo `r₂ = b - r₁ &lt; b - (b/2) = b/2`.

Em ambos os casos, o segundo termo reduz a menos da metade em no máximo dois passos.

### Conectando a Redução ao Logaritmo

Esta propriedade fundamenta a complexidade logarítmica do algoritmo:

1. Se temos `P = 2k` passos (k pares),

1. E a cada par o termo `b` é dividido por 2, após k pares temos `b / 2^k`.

1. O algoritmo termina quando chegamos próximo a 1, então `b / 2^k ≈ 1`, ou `b ≈ 2^k`.

1. Para encontrar `k`, aplicamos o logaritmo na base 2 em ambos os lados: `log₂(b) ≈ k`.

1. Como `P = 2k`, temos `P ≈ 2 log₂(b)`.

Isso explica por que a complexidade cresce logaritmicamente, não linearmente, com o tamanho do número.

### MCD como combinação linear

![[image 4 36.png|image 4 36.png]]

![[image 5 25.png|image 5 25.png]]

Outra forma de calcular o MCD é através da combinação linear. Uma **combinação linear** de dois inteiros a e b é qualquer número na forma ia+jb, onde i e j são inteiros.

**Exemplo simples:** Com os números 10 e 4:

- 2⋅10+3⋅4=32 (combinação linear);

- 1⋅10−2⋅4=2 (outra combinação);

- (−3)⋅10+8⋅4=2 (mesma solução, coeficientes diferentes);

### Como a Combinação Linear se Aplica ao MCD?

Segundo a **Identidade de Bézout** (Lema 6.2), o MCD de dois números é sempre uma combinação linear deles.

Isto significa que para quaisquer números n e d, **seu MCD é uma combinação linear** destes números. Existem inteiros i e j tais que: $MCD(n,d)=in+jd$

Estes coeficientes i e j são obtidos pelo **Algoritmo de Euclides Estendido**.

### Algoritmo de Euclides Estendido

Através do Algoritmo de Euclides, podemos encontrar os termos _i_ e _j_ do passo anterior usando os coeficientes do passo atual, e assim encontrar o MCD até chegar no passo zero, do final até o começo.

- Lembrando de que _i_ e _j_ são os coeficientes dos termos no MCD, e pode ser igualado ao valor de _r: $r=ia+jb$._

Vamos encontrar o MCD de 56 e 15 e escrevê-lo como uma combinação linear.

**1. Algoritmo de Euclides (para encontrar o MCD):**

- 56=3⋅15+11

- 15=1⋅11+4

- 11=2⋅4+3

- 4=1⋅3+1⟹ O MCD é 1.

**2. Algoritmo de Euclides Estendido (trabalhando de trás para a frente para encontrar a combinação):**  
O objetivo é escrever o MCD (que é 1) em termos dos números originais (56 e 15).

- Da penúltima linha, isolamos o MCD:  
    1=4−1⋅3

- Da linha acima, sabemos que 3=11−2⋅4. Substituímos esse 3 na equação:  
    1=4−1⋅(11−2⋅4)1=4−1⋅11+2⋅41=3⋅4−1⋅11

- Da linha de cima, sabemos que 4=15−1⋅11. Substituímos esse 4 na equação:  
    1=3⋅(15−1⋅11)−1⋅111=3⋅15−3⋅11−1⋅111=3⋅15−4⋅11

- Da primeira linha, sabemos que 11=56−3⋅15. Substituímos esse 11 na equação:  
    1=3⋅15−4⋅(56−3⋅15)1=3⋅15−4⋅56+12⋅151=15⋅15−4⋅56

**Conclusão:**  
Conseguimos escrever o MCD como uma combinação linear: MCD(56,15)=1=(−4)⋅56+(15)⋅15.

Neste caso, i=−4 e j=15.

Essa propriedade é extremamente útil. Por exemplo, como o seu material aponta, ela é a base para provar quando um número tem um inverso em Zd e para calcular esse inverso.

  

**Exemplo**

![[image 6 17.png|image 6 17.png]]

- Observe que começamos do final: escrevemos o _r_ do último passo sendo igual a 3-2.

- O passo a seguir é substituir 2, o _r_ anterior, pelo seu valor isolando na conta anterior: $2=11-3*3$.

- A seguir, substituímos o valor de 3, o _r_ anterior, pelo seu valor após isolá-lo.

- Observe que sempre deixamos o termo do _r_ anterior em evidência, para que possamos substituir pelo seu valor após isolá-lo.

- Repetimos esse processo até chegar ao _r_ do módulo inicial.