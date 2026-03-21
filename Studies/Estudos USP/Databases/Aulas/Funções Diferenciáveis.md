---
Course:
  - https://www.notion.so/C-lculo-II-24efa7f60cd880b0b8e2ea5108f9eeb0?pvs=21
Last Edited: 2025-11-11T09:34
---
Vimos que, por definição, uma função f(x) é diferenciável ou derivável em x0 se e somente se o limite, quando h tende a zero, da razão incremental existir e for finito.

![[image 104.png|image 104.png]]

Esta forma não é adequada para generalização, pois se f for uma função de duas variáveis reais h será um par ordenado e, então, a razão incremental não terá sentido. Nossa tarefa a seguir é a de tentar obter uma forma equivalente à definição de diferenciabilidade e que seja passível de generalização.

Para estender esse conceito à funções de duas variáveis, precisamos inserir uma segunda incógnita em nossa expressão, _a._

![[image 1 79.png|image 1 79.png]]

Então, podemos definir a diferenciabilidade de modo estendido:

![[image 2 63.png|image 2 63.png]]

  

> Teorema 1. Se f for diferenciável em (x0, y0), então f será contínua em (x0, y0).

  

Relacionamos esse assunto às derivadas parciais na afirmação de que, se uma função é diferenciável nas variáveis (x0, y0), então existem derivadas parciais nesse ponto.

![[image 3 54.png|image 3 54.png]]

A demonstração desse fato discorre da simples igualdade de uma das variáveis a zero. Por sabermos que existe a diferenciabilidade, e que o resultado da expressão é 0, podemos igualar tudo a uma derivada parcial:

![[image 4 45.png|image 4 45.png]]

Observação: sendo _a_ e _b_ iguais à derivada parcial da função _f_ diferenciável no ponto (x0, y0), então esses são os únicos valores reais para os quais o limite da expressão completa, incluindo _ah e bk_ é igual a 0.

**Corolário que resume essa propriedade:**

- Para verificar se uma função é diferenciável em um ponto, podemos usar o **Teorema da Condição Suficiente para Diferenciabilidade**.

- Este teorema diz que, se as derivadas parciais (\$\frac{\partial f}{\partial x} \frac{\partial f}{\partial y}$) existem e são **contínuas** em uma região aberta ao redor de um ponto, então a função é diferenciável nesse ponto.

- Para uma função ser diferenciável em um ponto, primeiro ela deve ser contínua neste mesmo ponto.

![[image 5 31.png|image 5 31.png]]

**Observações**

![[image 6 22.png|image 6 22.png]]

Por fim, diremos que f é uma função diferenciável se f for diferenciável em todo ponto de seu domínio.

## Teste de Diferenciabilidade

O teste