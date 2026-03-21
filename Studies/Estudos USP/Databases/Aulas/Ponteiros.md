---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-1b9fa7f60cd880c9a478ea23cbd908a4?pvs=21
Last Edited: 2025-08-09T11:51
---
### Definição

Ponteiros são variáveis que armazenam endereços de memória.

- Esse endereço costuma ser a posição de outra variável (é dito que o ponteiro aponta para a variável).

Para declarar um ponteiro indica-se o tipo da variável a qual o ponteiro vai apontar e antes de inserir o identificador utiliza-se um asterisco `int *ponteiro;`

Na atribuição, a variável que será apontada é acompanhada de um & `int *ponteiro = &var`;

### Derreferência

Pelo fato do ponteiro já retornar um endereço, o & não é necessário em funções que solicitam um endereço como parâmetro, como o scanf. Ao invés disso, utiliza-se um asterisco para retornar o valor do endereço o qual o ponteiro aponta `printf("%d", *ponteiro);`

É possível realizar operações ao utilizar o ponteiro acompanhado pelo asterisco, e inclusive alterar o valor que ele aponta.

### Operações no Endereço

Uma operação com o endereço do ponteiro obrigatoriamente muda o endereço para o qual ele aponta. A distância para o endereço novo é igual a n*tamanho da variável.

- Exemplo: uma variável do tipo int(ocupa 4bytes), no endereço 0x01 é multiplicada por 1. O novo endereço será o endereço atual somado de 4*1, portanto o novo endereço será 0x05.

### Casting no ponteiro

Quando atribuímos o endereço de uma variável de tipo diferente daquele do ponteiro, o ponteiro vai armazenar uma quantidade de bytes igual ao tipo declarado, independente do tamanho da variável.

```C
int var = 5;
char *ponteiro = (char*)&var;
```

A variável do tipo int ocupa 4bytes mas o tipo char somente 1byte. Sendo assim, o ponteiro vai armazenar somente uma parte do endereço e, portanto, da variável.

  

### Ponteiro de Ponteiro

Para declarar um ponteiro que aponta para outro ponteiro, declaramos ele com dois asteriscos. A referência de um ponteiro para o outro pode ocorrer de forma ilimitada.