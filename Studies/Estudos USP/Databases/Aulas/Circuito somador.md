---
Course:
  - https://www.notion.so/L-gica-Digital-1c1fa7f60cd88012b3fee27ba8aaeae7?pvs=21
Last Edited: 2025-08-09T11:53
---
# Half adder

Há duas entradas e duas saídas, estas últimas sendo representadas por S(sum) e C(carry).

Para dois números de apenas um bit é necessário de dois bits para o resultado.

- Podemos encontrar o resultado da saída S como um XOR entre as entradas.

- A saída Carry é definida por um AND entre as saídas.

# Full adder

Para soma de bits maiores é necessário usar um full adder.

Construído usando half-adders.

- Existem três entradas e duas saídas.

- Além das duas entradas das casas dos números, soma-se o Carry in.

- As duas saídas são o S e Carry out.

A característica do full adder é que para somar cada par de bit o carry out do par anterior liga-se ao carry in do próximo.

A saída S pode ser simplificada através de um XOR, no seguinte aspecto:

![[image 57.png|image 57.png]]

![[image 1 41.png|image 1 41.png]]

A saída Carry out é definida pelas três combinações AND possíveis entre as entradas.

![[image 2 32.png|image 2 32.png]]

É possível construir um full adder utilizando dois half adders.

![[image 3 25.png|image 3 25.png]]

  

# Ripple-carry adder

O ripple-carry adder é construído usando sequências de full adders. Um para cada par de bits.

- A mesma lógica do full adder permanece, a de conectar o carry-out no carry-in do próximo.

Para realizar operações é importante conhecer um macete muito prático:

- Para multiplicar ou dividir números por 2 e seus múltiplos, basta mover o número para a esquerda (multiplica) ou direita (divide), colocando 0 onde a nova casa aparecer.
    
    - A quantidade de bits vai determinar quantas vezes a operações acontece.
    

  

Em números com sinal, o bit mais à esquerda define o sinal, portanto o bit mais significativo é o segundo mais à esquerda.

É possível implementar a subtração no ripple-carry. Para tanto, primeiramente definimos um input para especificar se a operação será soma ou subtração.

- O valor 0 desse input significa que a operação será soma.

- O valor 1 desse input significa que a operação será subtração.

  

Para substrações, devemos obter o valor em complemento de 2. Para tal, o carry-in será 1 (pois como visto em [![](https://www.notion.so/icons/clipping_gray.svg)Complemento de 1 e de 2](https://www.notion.so/Complemento-de-1-e-de-2-1e3fa7f60cd880e2998fe44c214ad45f?pvs=21), o complemento de 2 é obtido somando 1 ao complemento de 1).

- Para tanto, o seletor de operações também é conectado ao primeiro carry in.

  

No ripple carry, para chegar ao valor negativo de um valor, calculamos seus bits negados, isto é x’, e somamos 1. Isto é: -x=x’+1. Na prática estamos realizando uma soma com o valor do subtrator negativado (y+(-x)).

- A versão negada consiste na forma de complemento de 1, o qual é obtido invertendo todos os bits.

- Somando 1 ao complemento de 1 chegamos ao complemento de 2 daquele algarismo.

- Para obter a versão negada, realizamos a operação XOR entre o subtrator e o seletor de operação.

- Esse +1 é obtido a partir do seletor de operação, ele entra no primeiro carry in.

![[image 4 22.png|image 4 22.png]]

- O primeiro algarismo pode ser inserido no formato padrão, em sinal de magnitude.

- O segundo algarismo é convertido em complemento de 2.

- O resultado é dado em complemento de 2.