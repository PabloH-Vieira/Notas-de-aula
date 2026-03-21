---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-11-13T20:39
---
![[image 80.png|image 80.png]]

O teorema nos diz que equações congruentes a uma mesma variável, mas com módulos diferentes, e que sejam relativamente primas (”primos entre si”) possuem uma solução única para os módulos que são relativamente primos.

## Equação para encontrar o valor da variável

![[image 1 60.png|image 1 60.png]]

- é necessário verificar a condição antes de tudo!

Para calcular as demais incógnitas dadas por M maiúsculos, realizamos as seguintes operações:

- $M =m{\footnotesize{1}}*m{\footnotesize{2}}*m{\footnotesize{3}}$

- $M{\footnotesize{1}} = \frac{M}{m{\footnotesize{1}}}$

- $M{\footnotesize{2}} = \frac{M}{m{\footnotesize{2}}}$

- $M{\footnotesize{3}} = \frac{M}{m{\footnotesize{3}}}$

- $M{\footnotesize{1}} * M{\footnotesize{1}}^{-1} = 1mod(m{\footnotesize{1}})$

- $M{\footnotesize{2}} * M{\footnotesize{2}}^{-1} = 1mod(m{\footnotesize{2}})$

- $M{\footnotesize{3}} * M{\footnotesize{3}}^{-1} = 1mod(m{\footnotesize{3}})$

Se os números são grandes, uma solução para encontrar o inverso de $M{\footnotesize{n}}$ é utilizando o algoritmo de Euclides estendido.

**Dica para encontrar** $M\footnotesize{n}^{-1}$**:**

![[image 2 50.png|image 2 50.png]]