---
Course:
  - "[[Cálculo III]]"
Last Edited:
---
Integrais são utilizadas para calcular a massa ou a área em gráficos descritos por funções. No entanto, o que acontece se o gráfico não for gerado por uma função, isto é, com início e fim definidos e um comportamento previsível?
Para isso utilizamos integrais de linha. Basicamente estaremos calculando a massa/área de uma curva no espaço.
A integral, ao invés de estar definida entre dois pontos, estará definida ao longo de uma curva C. A função dentro da integral deve descrever a massa ou a área e derivamos com relação a ds (o comprimento do arco).
- f(x,y) aplicado em uma curva fornece uma altura (como se a curva fosse um plano, e com f(x,y) fosse uma superfície);
- ds representa partes de comprimentos mínimas da curva;
- altura * comprimento = área. A soma das áreas de cada parte é a integral.
Basicamente, a função vai descrever a região entre o gráfico gerado por ela e a curva, dentro da qual calcularemos a área.

Calcular a curva a partir de uma função de duas variáveis torna o processo muito mais complicado. Uma solução para isso é usar uma função de uma variável apenas. Para isso, transformamos a função em uma função vetorial.
- $f(x,y) \rightarrow f(x(t), y(t))$
No entanto, precisaremos ajustar ds também. Na prática, o comprimento pode ser calculado na forma de $\sqrt{[x'(t)]²+[y'(t)]²}$
Essa fórmula nada mais é do que a de magnitude do vetor. Então, obtemos:
A nossa integral agora é parametrizada em razão de pontos *t* do vetor. Essa variável será também o limite de integração da nossa variável.
![[Pasted image 20260331124943.png]]

A curva pode ter a forma de uma circunferência, de forma que podemos utilizar coordenadas polares para a resolução dos problemas.
- Nesse caso, os da função vetorial $\vec{r}(t) = xi + yj$ são substituídos pelos valores dessas variáveis na forma de coordenadas polares, chegando a $\vec{r}(t) = rcos(t)i + rsin(t)j$.
- Também substituímos os valores na função f(x, y).
![[Pasted image 20260331144402.png|476]]

Outro caso é quando temos uma curva na forma de segmento.
- Um detalhe importante desse caso é que os limites de integração de t serão sempre 0 e 1.
- Os valores de x e y devem ter a forma de retas quando parametrizadas em t, ou seja, uma função afim.
- Definimos o valor da constante e do coeficiente na função afim a partir dos pontos estabelecidos do segmento.
	- Cada um desses pontos deve estar relacionado com um dos limites de integração, ou seja, 0 ou 1.

Em alguns casos, é dada uma integral que não está em função do comprimento da curva, isto é, em ds. Ao invés disso, ela é dada em função de $dx$, $dy$ e $dz$.
- Esse caso requer um tratamento especial.
- Devemos determinar o coeficiente de dt a partir da derivada da função a fim de x/ y.

Uma exigência para as integrais de linha é que a curva seja suave, isto é, não possua bicos.
- Se não for o caso, devemos quebrar em segmentos que, por sua vez, sejam suaves.
- Nesses casos, a ordem que estabelecemos a relação com o valor de t importa. 