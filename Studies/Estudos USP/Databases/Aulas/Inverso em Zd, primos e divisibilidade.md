---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-09-25T19:56
---
## Inverso em $\mathbb{Z}$d

![[image 78.png|image 78.png]]

Juntamos esse lema ao conteúdo visto em MCD, que diz que MCD de um número é sempre a combinação linear de dois outros.

Dizemos que dois números são primos entre eles quando o MCD é igual a 1. Essa definição se conecta com o Teorema de Euclides.

![[image 1 59.png|image 1 59.png]]

![[image 2 49.png|image 2 49.png]]

Podemos calcular o inverso da classe de _a_ através do algoritmo de Euclides, a partir do qual vamos encontrar o valor do coeficiente de j do último passo.

  

Corolário 6.4: um elemento $[a]\small{d}$ é invertível em Zd se, e somente se, o Máximo Comum Divisor (MCD) entre a e d for 1.

- Por exemplo, $[3]\small{5}$ é invertível porque MCD(3,5)=1.

- Em Z6, o elemento $[4]\small{6}$ não seria invertível, pois MCD(4,6)=2. Não existe nenhum número que multiplicado por 4 resulte em 1 no módulo 6.

### Mais propriedades dos primos

![[image 3 42.png|image 3 42.png]]