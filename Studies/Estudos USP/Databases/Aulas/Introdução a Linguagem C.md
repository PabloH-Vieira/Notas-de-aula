---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-1b9fa7f60cd880c9a478ea23cbd908a4?pvs=21
Last Edited: 2025-08-12T21:30
---
Configurar o lint no VSCode

A ferramenta CygDrive permite simular o ambiente do Linux, onde há o compilador GCC.

![[image 50.png|image 50.png]]

### Forma generalizada de um código

![[image 1 35.png|image 1 35.png]]

**Diretivos**

Os diretivos são comandos direcionados ao pré-processador, que executa sua função antes do compilador.

Um exemplo de diretivo é o `#include`, que faz com que uma biblioteca seja incluída no código do programa.

- Não utilizam ;

- Iniciam por #

  

**Funções**

Existem dois tipos de funções em C: aquelas escritas pelo programador e aquelas inerentes às bibliotecas da linguagem, suportadas pelo compilador.

Em termos gerais, uma função consiste em um conjunto de instruções agrupadas e nomeadas.

As funções podem computar ou não um valor. Quando elas computam, utiliza-se o comando `return` para especificar o que ela retorna, como: `return y*y - z*z` .

Somente a função main é obrigatória, sendo executada automaticamente quando o programa é executado.

`int main (void) return 0`

- Sendo uma função, `main` retorna um valor, do tipo específico `int` como sinalizado no início da instrução. Esse valor, que pode ser 0 ou 1, é, basicamente, um status para o compilador encerrar ou não o programa.

- O termo `void` determina que a função não tem argumentos

  

### Comandos

Comandos são linhas de códigos a serem executadas quando o programa iniciar. Os comandos terminam em ; para indicar que aquele é o fim do comando.

### Comentários

Comentários são escritos ao serem antecedidos pelo sinal /* e encerrados por */. Esses delimitadores podem estar na mesma linha ou não.

Além disso, não existe a possibilidade de escrever comentários aninhados, pois isso resulta em um erro.

### Variáveis

Variáveis consistem em espaços na memória para armazenar informações. É importante definir o tipo adequado às necessidades, como casas decimais ou espaço de memória.

- É possível definir um valor do tipo float para uma variável int, mas isso não é aconselhável.

  

==Para imprimir uma variável é necessário sinalizar o lugar do texto onde ela será mostrada por um indicador, que depende do tipo de variável.==

- %d para int.

- %f para float.

- %c para caractere.

  

Ao imprimir valores float, pode ser necessário limitar as casas decimais (o tipo int possui 6 casas depois do 0.), e isso é feito ao colocar .n após o sinalizar, ex:  
`printf("printing the value %.3f",var)`, colocando três casas decimais para a variável `var`.

Para quaisquer valores com decimais, é importante adicionar o caractere `f` ao final do valor, para que essa variável seja identificada pelo compilador como o tipo `float`, caso contrário, ela poderá compilá-la como `double` , que acaba ocupando um espaço de memória maior.

![[image 2 27.png|image 2 27.png]]

  

==Declarar uma variável sem valor e depois chamá-la pode ser problemático: é possível que seja retornado um valor aleatório armazenado anteriormente naquele espaço de memória ou até um crash no programa.==

Pode-se realizar operações entre variáveis dentro de comandos, o que ajuda na redução de variáveis (não será necessário criar uma variável apenas para armazenar o resultado daquela operação).

![[image 3 20.png|image 3 20.png]]

É importante que ao definir um nome para uma variável, não pode-se iniciar por caracteres especiais, nem números. Além disso, não pode-se utilizar as palavras-chave, importantes para o funcionamento do pré-processador.

![[image 4 17.png|image 4 17.png]]

### Constantes

Constantes são espaços de memória com valores imutáveis durante o programa.

É possível nomeá-las usando a função de definição de macro, utilizando o diretivo \#define seguido pelo nome da constante e o valor, sem ; ao final. Exemplo:

`#define CONST_A 999`

- Por convenção, os nomes de constantes são escritos com letras maiúsculas.

A partir desse ponto, podemos inserir a constante `CONST_A` em qualquer operação e o pré-processador irá utilizar o valor definido.

O valor de uma constante também pode ser uma operação, e se há operadores, toda a expressão deve estar entre parênteses.

  

  

Para a organização do código, a linguagem C permite escrever uma linha de comando em diferentes linhas do programa, facilitando a visualização do código.

![[image 5 14.png|image 5 14.png]]

  

  

**Software CLion**

  

Operador ternário usado quando uma variável receba um valor caso atenda a uma condição ou outro valor caso não atenda.