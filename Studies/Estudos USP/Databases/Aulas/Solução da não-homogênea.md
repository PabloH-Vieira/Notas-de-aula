---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-11-17T23:58
---
Uma recorrência não homogênea é aquela na qual o resultado da relação de recorrência entre os termos é diferente de 0. Na verdade, o resultado é um $f(n)$ ou uma constante.

![[image 81.png|image 81.png]]

## Estratégia geral

![[image 1 61.png|image 1 61.png]]

Resolvemos primeiro o problema pensando na forma homogênea e depois o caso particular, como em uma soma de vetores.

### Casos comuns

![[image 2 51.png|image 2 51.png]]

Do lado esquerdo, temos o resultado da equação de recorrência, e do outro, o valor do termo $a{\footnotesize{n}}$

- Esses casos são aplicáveis para a parte particular, e não a homogênea, a qual é calculada do modo convencional.

### Exemplo

**Parte homogênea (procedimento padrão):**

- Perceba que desconsideramos o valor de $f(n)$ e consideramos que a relação de recorrência é igual a 0.

![[image 3 43.png|image 3 43.png]]

**Parte particular:**

Caso a raiz for igual, isto é, o $\Delta$ da raiz for igual a 0, devemos multiplicar por _n_ o nosso termo na parte particular.

- Além disso, caso a raiz seja igual ao resultado da recorrência, também devemos multiplicar o termo por _n_.

No momento da parte particular, trocamos cada termo pelo correspondente na tabela. No caso do exemplo, substituímos todos os termos para a fórmula $Ar^n$ e considerando $r=2^n$ (o valor de $f(n)$), os termos terão a forma: $A2^n$.

- Um detalhe importante é que _n_ corresponde ao índice do termo.

- Outro detalhe é que mantemos os coeficientes dos termos após a substituição.

![[image 4 37.png|image 4 37.png]]

Finalmente, somando as partes homogênea e particular podemos encontrar a expressão para o termo.

![[image 5 26.png|image 5 26.png]]

- Encontramos $\alpha$ ao aplicar um resultado conhecido do termo, geralmente $a\footnotesize{0}$, já que este cancela a parte particular.

### Exemplo 2

**Parte homogênea:**

![[image 6 18.png|image 6 18.png]]

**Parte particular:**

- Nesse caso, como encontramos dois valores para _r,_ não foi necessário multiplicar o termo por _n_

![[image 7 15.png|image 7 15.png]]

### Dica

Sempre que a equação de recorrência tiver a forma $a{\footnotesize{n}}-a{\footnotesize{n-1}}=f(n)$, sendo f(n) uma função em razão de _n_ ou uma constante, podemos resolver essa recorrência simplesmente por $a{\footnotesize{n}}=\sum_{i=1}^{n}f(n)$.

---

## Coeficientes Indeterminados

Um equação de recorrência homogênea pode ser transformada em uma recorrência não homogênea se adicionarmos um termo não homogêneo.

Nesse caso, devemos chutar uma solução, considerando que a nossa equação homogênea agora é igual a $g(n)$. A partir daí, basta apenas resolver a parte particular do modo convencional.