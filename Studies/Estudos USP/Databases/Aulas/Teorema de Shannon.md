---
Course:
  - https://www.notion.so/L-gica-Digital-1c1fa7f60cd88012b3fee27ba8aaeae7?pvs=21
Last Edited: 2025-08-09T11:52
---
O Teorema de Shannon é a definição algébrica que prova que podemos implementar qualquer função lógica utilizando multiplexadores.

O princípio de funcionamento consiste na escolha de um dos elementos da função como seletor. Basicamente, vamos reescrever a função fazendo minterms em função desse seletor.

![[image 62.png|image 62.png]]

- No primeiro minterm, temos _w1_ com valor 0 e depois com valor 1.

- O próximo passo é para cada trecho, aplicar o valor do seletor na função e preservar o resultado.

![[image 1 46.png|image 1 46.png]]

**Multiplexador dessa função**

![[image 2 37.png|image 2 37.png]]

Podemos agrupar os elementos como seletores para funções mais complexas, fazendo uma expansão de Shannon em cascata.

![[image 3 30.png|image 3 30.png]]

![[image 4 27.png|image 4 27.png]]