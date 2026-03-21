---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-11-18T13:10
---
Existe um algoritmo que nos facilita encontrar primos recebendo como parâmetro um real _n_ qualquer. Esse algoritmo nos diz que no espaço $\log_{e}{n}$ ao redor de _n_ haverá ao menos um número primo.

No entanto, precisamos de uma forma que nos permita comprovar que um número é primo de maneira efetiva. Testar todos os possíveis divisores até _n_ levaria muito tempo, mas existem algoritmos mais eficazes para esta tarefa.

É o caso de uma variação do Pequeno Teorema de Fermat. Alguns métodos foram desenvolvidos, mas o mais atual trabalha com uma análise com uma taxa de erro igual a qualquer inteiro diferente de 0. Essa área de estudos é chamada de Teste de Miller Rabin.

O Pequeno Teorema de Fermat nos diz que:

- v. 1: seja _p_ um primo e _a_ um _a_ pertencente a $\mathbb{Z}{p}$, então $a^{p-1}(\mod{p})=1$.

- v. 2: para qualquer inteiro positivo _a_ não múltiplo de _p_ (um número primo), então $a^{p-1}(\mod{p})=1$.

Daí, se $x^{m-1}(\mod{m}) \neq 1$, seja $x$ um número sem multiplicativo inverso em $\mathbb{Z}m$, então $m$ não é um número primo. Caso o teste resultar em igual a 1, então dizemos que $m$ é um _pseudoprimo_ e esse tipo já pode ser utilizado no RSA.

## Teste de Miller Rabin

O teste de Miller Rabin é uma variação do Pequeno Teorema de Fermat e nos diz se um número é primo ou um composto.

Assumimos que o número é primo, e caso cheguemos a uma afirmativa falsa, concluímos que o número é na verdade um composto.

Realizamos diversas modificações na fórmula do Pequeno Teorema de Fermat e utilizamos e o Lema de Euclides.

- O lema de Euclides nos diz que se dois números $a*b=0(\mod{p})$, então $p$ é múltiplo de $a$ ou $b$. Caso isso não seja atendido, então $p$ não é primo.

Escrevemos o P.T de Fermat na forma:

$$a^{n-1}=1(\mod m)$$

Seja:

- $a$ um número pertencente a $\mathbb{Z}m$

e daí:

$$a^{n-1}-1=0(\mod{m})$$

e então fatoramos os termos da esquerda diversas vezes (caso o expoente for par). Paramos somente quando encontrarmos um termo na esquerda cujo expoente é ímpar.

Agora verificamos o Lema de Euclides: se $m$ for de fato primo, ele deve dividir ao menos um dos termos.

![[image 84.png|image 84.png]]

![[image 1 63.png|image 1 63.png]]

Para um teste qualquer, a probabilidade de que $m$, passando no teste, seja de fato primo é de 3/4. No entanto, para diversos testes com $m$ diferentes, essa probabilidade aumenta consideravelmente com relação a taxa de erro.

### Algoritmo

A definição no bloco acima mostra o caminho para provar o teste de Miller Rabin, mas não é aplicável para valores muito grandes.

Para de fato verificar se _n_ é primo seguimos um passo-a-passo:

- Encontramos $s$ e $d$ tal que $n-1 = 2^s \cdot d$ (com $d$ ímpar).
    
    - Basicamente, dividimos $n-1$ por $2$ repetidamente até sobrar um número ímpar: $d$ será o valor do inteiro da última divisão e $s$ a quantidade de divisões até chegar lá.
    

- Escolhemos a base $a$ entre $2$ e $n-1$.

- **Teste Inicial:** Calculamos $x = a^d \pmod n$, e se $x=1$ ou $x=n-1$, podemos concluir que $n$ é um pseudoprimo.

- **Loop de quadrados:** Repetimos $s-1$ vezes o seguinte cálculo: $x = x^2 \pmod n$ e se chegarmos a $x=n-1$, concluímos que $n$ é um pseudoprimo.

- Se não encontrarmos $x=n-1$ então $x$ é um composto.