---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-09-18T19:54
---
Coleções são uma forma de organizar um programa que conta com um grande número de objetos.

### Array List

Essa é uma das formas de utilizar coleções.

Podemos adicionar ou remover elementos (objetos), receber o tamanho ou ainda acessar um elemento da lista.

![[image 132.png|image 132.png]]

Um detalhe importante é que o array list interpreta os elementos ali dentro como pertencentes à classe Object. Portanto, somente métodos e atributos oriundos dessa classe podem ser acessados. **Ou seja, não podemos acessar um atributo da classe específica dentro do array.**

- Existe uma forma de conseguir acessar os atributos específicos: é através do **casting**. Consiste em explicitar o nome da classe.

![[image 1 100.png|image 1 100.png]]

---

Outra forma de utilizar coleções, sem o mesmo problema da array list é através dos tipos parametrizáveis.

Passamos um tipo como parâmetro para o array list.

![[image 2 79.png|image 2 79.png]]

Criamos uma variável chamada `contas` cujo tipo é um array list parametrizado para a classe `ContaCorrente` . Desta forma, é possível acessar os atributos dos objetos sem a necessidade do casting.

- Não necessariamente precisa ser uma classe, pode-se utilizar uma superclasse ou uma interclasse.

![[image 3 67.png|image 3 67.png]]

_Forma mais simplificada de escrever._

![[image 4 54.png|image 4 54.png]]

A interface `iterable` no topo da estrutura de coleções, é basicamente uma coleção que agrupa diversas coleções e trata todas como iteráveis. Isso permite utilizar o `for` melhorado, permitindo acessar, adicionar, excluir ou editar os dados presentes em cada um dos objetos.

![[image 5 38.png|image 5 38.png]]

  

O Java já inclui bibliotecas com diversos tipos de coleções já implementadas.

O uso de interfaces comuns é muito recomendado, pois pode-se acessar diferentes tipos de coleções de forma padronizada e uniforme.