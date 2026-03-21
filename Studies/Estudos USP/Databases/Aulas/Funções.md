---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-1b9fa7f60cd880c9a478ea23cbd908a4?pvs=21
Last Edited: 2025-08-12T21:30
---
Existem duas formas de passar parâmetros para uma função:

- Por valor, o qual simplesmente copia o valor do argumento, sem modificar o original ao final da função.

- Por referência, o qual utiliza a variável durante a função, de fato alterando-o se isso ocorrer.

  

Na passagem por referência, utilizamos um ponteiro na declaração dos argumentos da função e o endereço da variável como parâmetro. Se estivermos tratando com um ponteiro não será necessário o &.

![[image 52.png|image 52.png]]

## Argumentos da função _main_

Os argumentos da função main que podem ser utilizados são:

- `argc` : determina a quantidade de argumentos que devem ser inseridos ao rodar o programa

- `argv` : trata-se de uma array de strings que armazena cada um dos argumentos digitados ao rodar o programa. Podemos acessar cada argumento separadamente no programa especificando o índice.
    
    - é importante ter em mente que o primeiro argumento, ou seja, `argv[0]` é sempre o nome do programa
    

```C
// C program named mainreturn.c to demonstrate the working
// of command line arguement
\#include <stdio.h>

// defining main with arguments
int main(int argc, char* argv[])
{
    printf("You have entered %d arguments:\n", argc);

    for (int i = 0; i < argc; i++) {
        printf("%s\n", argv[i]);
    }
    return 0;
}
```

![[image 1 36.png|image 1 36.png]]