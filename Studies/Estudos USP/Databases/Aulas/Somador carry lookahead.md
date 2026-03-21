---
Course:
  - https://www.notion.so/L-gica-Digital-1c1fa7f60cd88012b3fee27ba8aaeae7?pvs=21
Last Edited: 2025-08-09T11:52
---
O somador lookahead visa diminuir o tempo para a execução de uma soma, um problema que é perceptível no caso do somador ripplecarry.

- O problema no somador ripplecarry consiste no fato de que, para o próximo bit ser operado, é necessário esperar o carry out do bit anterior.

  

A expressão que determina o carry lookahead é semelhante pelo menos em relação a saída S. A diferença de fato ocorre na saída carry.

- Ela é calculada ao agrupar as possibilidades (na tabela verdade), em que a saída carry out é 1. Basicamente, dois casos: quando o carry é gerado ou propagado.

![[image 59.png|image 59.png]]

### Carry Gerado

O carry out é sempre igual a 1 se tanto A quanto B forem 1.

![[image 1 43.png|image 1 43.png]]

### Carry Propagado

Ocorre quando o carry out copia o carry in.

Para tal, A ou B deve ser igual a 1, e em seguida fazemos um AND com o carry in.

![[image 2 34.png|image 2 34.png]]

### Expressão Final

![[image 3 27.png|image 3 27.png]]

E para cada novo bit, reutilizamos o carry out anterior (a expressão inteira).

![[image 4 24.png|image 4 24.png]]