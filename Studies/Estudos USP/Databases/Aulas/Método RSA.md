---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-11-14T11:37
---
O método RSA é um método de criptografia que consiste em criptografar uma mensagem na ordem de 10$^{300}$ dígitos a partir de uma chave pública e descodificá-la a partir de uma chave privada.

![[image 79.png|image 79.png]]

Determinamos algumas variáveis:

- $p, q$ dois valores quaisquer, que juntos formam a chave privada.

- $n = pq$ a chave pública, obtida pelo produto entre dois números. É extremamente encontrar a chave privada, $p$ e $q$ unicamente a partir de $n$.

- $e$, um valor que seja coprimo (apenas 1 como maior divisor comum) com $(p-1)(q-1)$

- $m$, a mensagem criptografada.

- $c$, a mensagem criptografada, obtida a partir de $c=m^e (mod\space n)$

  

Percebe-se que a mensagem criptografada _c_ pode ser construída a partir de valores públicos, mas a descriptografar segue um outro processo.

- encontramos um valor $d$ tal que $de=1(mod\space(p-1)(q-1))$

- podemos encontrar a mensagem criptografada a partir da relação $m = c^d(mod\space n)$

  

Outra notação que pode aparecer para o termo $(p-1)(q-1)$ é $\phi(n)$.

---

## Encontrando as chaves secretas a partir das públicas

Para encontrar _p_ e _q:_

- Definimos um limite para o menor termo como $\sqrt{n}$

- Testamos dividir _n_ pelos primos até o limite de forma que encontremos um outro inteiro primo como resultado.

- Esses dois números primos são os termos _p_ e _q._