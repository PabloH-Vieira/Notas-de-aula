---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-12-03T00:54
---
## Infixa

**Expressões infixas são o tipo de expressão mais comum.**  Essa notação é tipicamente empregada ao escrever expressões aritméticas manualmente. Além disso, na expressão infixa, colocamos o operador entre os dois operandos sobre os quais ele opera.

$$A+B-C+D$$

Nas expressões infixas também aparecem parênteses para indicar a prioridade.

## Pré-fixa

Nas expressões pré-fixas, os operadores aparecem antes dos operandos. A ordem é da direita para a esquerda, então todos os operandos a direita de um operador (até que apareça outro operador), vão são calculados.

- Perceba que aparecem primeiro os operadores das últimas posições.

- Perceba que após o sinal aparece primeiro o operando da direita e depois da esquerda.

$$-++ABCD$$

### Convertendo da infixa

  

## Pós-fixa

As expressões pós-fixas são o inverso das pós-fixas. Nelas, os operandos aparecem à esquerda do operador. Assim, todos os operandos à esquerda de um operador (até que apareça outro operador) vão ser calculados.

$AB+CD-$

![[image 121.png|image 121.png]]

- A ordem dos operadores na expressão diz a ordem em que eles vão ser executados (da esquerda para a direita)

### Convertendo da infixa

- A ordem das variáveis são copiadas na mesma ordem.

Durante o processo de conversão, os caracteres da expressão infixa são processados da esquerda para a direita. Quando operadores com maior prioridade são vistos, esses são empilhados de modo a ocupar o topo da pilha. Eles devem permanecer na pilha até aparecer na entrada um operador de prioridade menor ou igual.