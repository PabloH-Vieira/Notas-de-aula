---
Course:
  - "[[Organização de Arquivos]]"
Last Edited: 2026-03-03T15:34
---
Um arquivo é salvo na forma de registros na RAM. Um registro tem a mesma estrutura de uma `struct` na programação usual. Isto é, ele tem campos.

Existem campos de tamanho fixo e de tamanho variável.

- Tamanho variável possui um tamanho inicial que pode variar. Pode ser enxergado como um vetor em memória dinâmica.

- Tamanho fixo são campos com tamanhos pré-definidos, como se fosse uma variável tipada.

Tamanhos fixos têm desvantagens por ter espaço desperdiçado e truncamento de dados (quando a informação não cabe nos bytes definidos).

Por outro lado, eles são extremamente rápidos para serem acessados, pois o byte de cada palavra é encontrado por uma fórmula matemática

![[image 137.png|image 137.png]]

Nessa outra aplicação com tamanho variável, existe um indicador de tamanho antes do dado propriamente dito. A desvantagem é que para acessar diferentes dados, deve-se considerar o tamanho dos indicadores e então pular de byte em byte.

![[image 1 104.png|image 1 104.png]]

Tendo em vista acelerar o acesso, essa outra aplicação com memória variável utiliza um delimitador ao final de cada dado. No entanto, a leitura é byte a byte e vai identificar a palavra desejada ao encontrar um pipe.

![[image 2 83.png|image 2 83.png]]

## Registros

Existem registros de tamanho fixo e de tamanho variável, de forma semelhante aos campos.

Se todos os campos de um registro tiverem tamanho fixo, pode-se concluir que o registro é de tamanho fixo.

No entanto, se o registro tem tamanho fixo não pode-se afirmar que todos os campos também o tenham.

A forma de acessar os registros fixos é a partir da fórmula do *byte offset*.
- Usamos o RRN, o indicador relativo do registro (basicamente o índice)
- E o tamanho em bytes de cada registro
- Daí, temos a fórmula $RRN * tam$


### Organização Híbrida

Na maioria dos casos, os campos de um registro são tanto variáveis quanto fixos. Existem alguns cuidados a serem tomados quando esse é o caso de um registro.
1. campos de tamanho fixo, como uma variável do tipo int, não precisam de um delimitador (como o caso de uma string que é de tamanho variável)
2. devido ao fato de variáveis de tamanho fixo não possuírem delimitadores, é necessário acessá-las a partir da fórmula *byte offset*. Para tal, é necessário alocá-las no início ou no final (o primeiro caso é o mais comum);

![[Pasted image 20260310144130.png]]

