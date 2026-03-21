---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-11-15T20:00
---
Uma relação de recorrência ocorre quando o próximo número de uma sequência depende dos números anteriores.

- Exemplos: sequência de Fibonacci, onde $a\footnotesize{n}= a\footnotesize{n-1}+\footnotesize{n-2}$

Tomando como exemplo da sequência de Fibonacci, em relações de recorrência sempre devemos definir o caso base, no caso, é igual a 1.

Em casos mais complexos, onde precisamos, por exemplo, descobrir um valor que ocupa uma posição centenas a frente da origem, devemos usar métodos específicos.

- Definimos expressões específicas para o problema.

- Por exemplo, a solução para descobrir o valor em uma posição da sequência geométrica é igual a $a{\footnotesize{n}}=a{\footnotesize{0}}(2^n)$, para o caso que o número dobra de tamanho. A razão poderia ser outra.

Generalizando, sempre vamos usar os termos $a\footnotesize{n}$, $a\footnotesize{n-1}$ e $a\footnotesize{0}$

Dica: em casos onde somamos os valores anteriores a $a\footnotesize{n}$, isto é $\displaystyle\sum_{i=1}^{n}{i}$, podemos também calcular $\frac{n(n+1)}{2}$ que obteremos o mesmo resultado.

![[image 83.png|image 83.png]]

- $(n+1)$ é somado _n_ vezes, e o _2_ passa para o outro lado.

Outra fórmula útil é a seguinte $a{\footnotesize{n}}-a{\footnotesize{n-1}}=k$ e $a{\footnotesize{0}}=c$. Daí, $a{\footnotesize{n}}=c{\displaystyle{\sum_{i=1}^{n}{k}}}$ .