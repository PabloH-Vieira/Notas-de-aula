---
Course:
  - https://www.notion.so/L-gica-Digital-1c1fa7f60cd88012b3fee27ba8aaeae7?pvs=21
Last Edited: 2025-08-12T21:44
---
### **Minterms (Produtos Canônicos)**

- Um **minterm** é um produto (AND) de todas as variáveis da função, onde cada variável aparece **na forma normal ou complementada**, dependendo da linha da tabela verdade.

- Notação: , onde iii é o número decimal correspondente à combinação binária das variáveis.

- A variável com valor 1 é mantida intacta e a variável 0 é substituída pela sua versão negada.

**Exemplos**

Linha 0: A=0, B=0, C=0

$m0=\overline{A} \cdot \overline{B} \cdot \overline{C}$

  

Linha 5: A=1, B=0, C=1

m5 = $A \cdot \overline{B} \cdot C$

  

==Ao final da tabela verdade, observamos os casos em que a expressão resultou 1 e realizamos a soma entre essas expressões.==

![[image 55.png|image 55.png]]

![[image 1 39.png|image 1 39.png]]

---

# **Maxtermos (Somas Canônicas)**

- Um **maxtermo** é uma soma (∨) de todas as variáveis da função, onde cada variável aparece **na forma normal ou complementada**, dependendo da linha da tabela verdade.

- Notação: Mi, onde iii é o número decimal correspondente à combinação binária das variáveis.

- A variável com valor 0 é mantida intacta e a variável 1 é substituída pela sua versão negada.

**Exemplo para três variáveis A,B,CA, B, CA,B,C:**

![[image 2 30.png|image 2 30.png]]

O **produto (∧) entre dois maxtermos** gera uma **nova expressão que ainda segue o formato de um Produto de Somas**.

==Ao final da tabela verdade, observamos os casos em que a expressão resultou 0x e realizamos a multiplicação entre essas expressões.==

![[image 3 23.png|image 3 23.png]]

![[image 4 20.png|image 4 20.png]]

---

Os operadores NAND e NOR negam o resultado da operação, isto é, não alteram o valor das variáveis.

A representação no circuito é com toda a operação sendo negada.

![[image 5 17.png|image 5 17.png]]

![[image 6 12.png|image 6 12.png]]

É interessante relembrar a propriedade De Morgan, a qual gera portas lógicas do tipo NOR e NAND a partir de OR e AND de variáveis negadas, e vice-versa.

![[image 7 11.png|image 7 11.png]]

---

## Multiplexer

O multiplexer exerce uma função de controle. Dependendo do seu valor, ele escolhe uma saída ou outra para seguir no circuito.

  

  

---

Peso das portas lógicas!

Propriedades booleanas na simplificação de operações

- Fazer exercícios de simplificação!

  

Para a tabela verdade fazer uma função que resulte 0, e assim eliminar na tabela as linhas que, nesta função, resultem em 0.