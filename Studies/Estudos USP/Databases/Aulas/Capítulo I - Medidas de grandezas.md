---
Course:
  - "[[Lab. de Física]]"
Last Edited:
---
O resultado de uma medida de uma grandeza física consiste no valor numérico associado a sua incerteza, utilizando o sistema de medidas apropriado. Deve refletir o processo de medida completo, incluindo os instrumentos, montagem experimental e método experimental.

Existem medidas diretas, que são associadas diretamente à escala medida no instrumento (é o caso do relógio, do tamanho em uma régua); e medidas indiretas, que utilizam de uma fórmula que calcula o resultado a partir de medidas diretas (por exemplo, o volume de um sólido, a velocidade de um objeto).

Instrumentos de medida tem um valor de precisão D agregado. É importante saber identificá-lo, sendo D o mínimo valor da escala do instrumento (por exemplo 1mm ou 0,5 mm). Para instrumentos digitais, trata-se da última casa decimal.

O valor medido deve aproximar-se do valor verdadeiro, que é desconhecido a princípio. A diferença entre esses valores é conhecido como erro -- de forma que nunca sabemos se o valor medido é de fato o valor verdadeiro.

Ao medir a grandeza física X múltiplas vezes, obteremos uma medida $x i$ que flutua para cima ou para baixo do valor verdadeiro, uma vez que a existência do erro se dá de maneira aleatória. Assim, na média aritmética, quando maior o valor de aferições, mais nos aproximamos do valor verdadeiro.
![[Pasted image 20260325212030.png]]


É possível calcular a incerteza associada à dispersão dos resultados a partir do desvio médio e do desvio padrão.
- O desvio médio é a média aritmética dos desvios de cada aferição em relação ao valor médio (o que consideramos o mais próximo do valor verdadeiro).
	- ![[Pasted image 20260325123953.png|264]]
- O desvio padrão utiliza uma fórmula específica, a função quadrado, ao invés dos desvios de cada aferição.
	- ![[Pasted image 20260325124119.png]]
O resultado do processo de medida pode ser informado dando o intervalo \[$\overline x - \sigma, \overline x + \sigma$], ou pois sabe-se que existe a possibilidade em 68% do valor verdadeiro estar nesse intervalo.
Outras formas de representar esse intervalo são:
![[Pasted image 20260325211718.png|77]]


Apesar do desvio ser indiretamente proporcional ao número de aferições N, isso não significa que podemos aumentar a precisão da medida de forma ilimitada, pois existe o limite da precisão de medida do instrumento.
- Assim, se os valores de desvio forem menores que o D, a precisão do instrumento, o valor calculado será justamente D.
![[Pasted image 20260325211800.png]]


Caso o valor medido não variar dadas diferentes aferições, podemos concluir que o erro é suficientemente pequeno de forma que o resultado será D.
![[Pasted image 20260325212116.png]]

Em grandezas dadas por uma função de múltiplas grandezas medidas, erros existentes nas grandezas da função se propagam para a medida da grandeza calculada na função.
- Por exemplo, o volume 𝑉 de um cubo de aresta 𝑎, cuja medida direta forneceu 𝑎 = (10 +-1) cm, terá como valor mais provável 𝑣 = (10 cm)³ = 1000 cm³. Entretanto, como 𝑎 tem dispersão, teremos variações prováveis no valor de 𝑉 entre 𝑉e 𝑉- = (9cm)³ e V+ = (11cm)³ = 1331 𝑐𝑚. Arredondando para uma faixa simétrica, resulta em V = (1000 +- 300)cm³.

Para calcular a propagação de incertezas para qualquer operação matemática ou função utilizamos ferramentas do cálculo diferencial.
![[Pasted image 20260325213224.png]]

Algumas das principais operações podem ter suas incertezas calculadas sa seguinte forma:
![[Pasted image 20260325213348.png]]
Sendo $\Delta x$ e $\Delta y$ os desvios de x e de y.
No cálculo de funções, constantes bem conhecidas como g e $\pi$ são considerados sem erro.

Na representação do resultado calculado final, já considerando a incerteza, devemos definir a quantidade de casas decimais. Para isso, devemos parar na casa em que o erro começa, isso porque sabemos que a partir dali o erro já terá afetado o resultado. 
- Por exemplo, tendo calculado $\overline x = 5,34481349 m$ e desvio padrão $\sigma = 0,03256874m$ devemos representar $\overline x = (5,34)m$, pois a partir desta casa o erro já terá comprometido o resultado. Assim, temos o resultado $\overline x = (5,34 +- 0,03)m$
	- o tamanho das casas do erro é até onde vai o primeiro algarismo significativo
- Caso a próxima casa com relação ao primeiro algarismo diferente de zero da incerteza for maior que 5 devemos arredondar o algarismo significativo para cima.
	- Seja $\overline x = 5,34481349 m$ e $\sigma = 0,0368491m$ devemos expressar $\overline x = (5,345 +- 0,004)m$


Como avaliar se dois valores de medidas de mesma grandeza são iguais, considerando que cada medida tem sua própria incerteza, isto é $x1 ± \sigma1$ e $x2 ± \sigma2$.
A forma correta de avaliar se x1 e x2 são iguais é se:
![[Pasted image 20260325220639.png]]
Eles não serão equivalentes caso:
![[Pasted image 20260325220703.png]]

Se a diferença |x1 - x2| não atender às condições, o resultado não é suficientemente conclusivo para afirmar se eles são equivalentes ou não.
