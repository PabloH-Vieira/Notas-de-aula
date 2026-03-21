---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-09-04T22:37
Related to Semestres:
  - "[[Estudos Complementares]]"
---
### Objeto

Um objeto é uma forma de encapsulamento de:

- Dados: variáveis e atributos.

- Código/Métodos: funções para manipular os dados.

### Classe

Define os elementos de um conjunto de objetos, especificando os métodos e atributos de cada um dos objetos.

- Também pode ser usada para criar novos objetos, o que é chamado de instanciação de objetos.

```Java
Carro c = new Carro();
```

```C++
Carro *c = new Carro();
```

Sistemas orientados a objetos são compostos por vários objetos que trocam mensagens entre si. Esse sistema usa objetos para representar coisas do seu domínio, seja ele real ou virtual.

- Essa troca de mensagens pode ser pela utilização de um método pertencente à outra classe, permitindo manipular as variáveis entre dois objetos de classes distintas.

---

## Variáveis de Classe X Variáveis de Objetos

Em Java, definimos uma nova classe usando o termo Class.

Para definirmos especificamente uma variável definida dessa classe utilizamos a palavra-chave `static` , para sinalizar que ela terá aquele valor em todos os seus objetos.

- As variáveis de classe, aquelas declaradas com `static` ao serem alteradas na execução de um objeto, automaticamente altera o valor da variáveis para todas os demais objetos dessa mesma classe.

- No entanto, as variáveis de objeto, as instanciadas, podem ser alteradas de forma isolada em cada um dos objetos.

---

## Herança

Trata de classes e subclasses, funcionando como um mecanismo para evitar duplicação de código e de promover o reuso de código.

- Relação “**é um**”, ex: pato é uma ave.

- A classe mãe já tem seus atributos e métodos, as quais cada subclasse herda, somando-se aos atributos e métodos das subclasses.

Exemplo (pessoas em uma universidade):

![[image 127.png|image 127.png]]

Outro exemplo:

![[image 1 98.png|image 1 98.png]]

Ir da classe maior para as classes filhas, estamos realizando uma especialização. O processo contrário chama-se generalização.

### Por que usar?

- Para organizar as abstrações

- Para acrescentar novos atributos e métodos à subclasse, aproveitando os já existentes da classe-mãe.

- Para alterar comportamento: podemos criar a subclasse para reimplementar parte da classe mãe, reescrevendo de acordo com o funcionamento da subclasse.

  

Em Python, declaramos uma subclasse colocando dentro do parênteses da linha de declaração o nome da superclasse.

![[image 2 78.png|image 2 78.png]]

---

## Unified Modelling Language (UML)

É uma linguagem gráfica utilizada em programação orientada a objetos, utilizada para visualizar uma arquitetura de software baseada em POO. Também pode ser utilizada para fornecer especificações a serem seguidas no desenvolvimento do projeto e, por fim, pode ser usada como documentação.

**Diagrama de classes**

![[image 3 66.png|image 3 66.png]]

Os sinais dizem se o atributo/método é público (+, acessada por qualquer classe) ou privado (-, acessada somente pela própria classe), ou ainda protegido (#, quando só pode acessado pela própria classe e subclasses).

  

![[image 4 53.png|image 4 53.png]]

Podemos representar associações entre as classes.

![[image 5 37.png|image 5 37.png]]

Outras classes podem existir para representar a associação entre as classes.

A herança é representada por uma flecha com um triângulo no topo.

Podemos representar uma agregação, quando uma classe possui mais de um objeto de uma classe associada.

![[image 6 26.png|image 6 26.png]]

- O instituto pode ter mais de um departamento, mas os departamentos têm apenas um instituto.

Também há a composição, um tipo de agregação a qual a classe de baixo só existe se a classe superior existir.

![[image 7 22.png|image 7 22.png]]

![[image 8 17.png|image 8 17.png]]

Representação de um sistema codificado em UML.

Existem duas formas de trabalhar com UML:

- Estrutural (detalha classes, objetos, implantação)

- Comportamental (sequências, atividades)

---

## Linguagens Processadas X Interpretadas

Em 1948 surgiu a linguagem de montagem, o Assembly.

Ao final da década de 50, surgiram as linguagens de alto nível, o FORTRAN e o LISP.

As linguagens interpretadas começam por um arquivo de texto, que passa por um interpretador e traduz, linha a linha, os comandos para linguagem de máquina.

As linguagens compiladas começam pelo arquivo de texto, e em seguida para o compilador que, por sua vez, gera um arquivo com os comandos em linguagem de máquina. Por fim, o programa é inicializado ao executar esse arquivo.

As linguagens híbridas são compiladas e também interpretadas. Escrevemos o programa que passa por um compilador, traduzindo o código para uma linguagem de baixo nível (_byte code_), que fica armazenado em um arquivo. Por fim, ao executar esse novo arquivo, um interpretador lê as linhas, as traduz para código de máquina e, finalmente, executa o programa.