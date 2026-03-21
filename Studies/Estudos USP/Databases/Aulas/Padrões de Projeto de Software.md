---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-10-29T15:18
---
A ideia de padrão é uma ideia central para a resolução de problemas recorrentes, sendo que essa solução nunca é implementada da mesma maneira, apenas obedece à ideia central.

Existe um catálogo de padrões que transmitem uma base de soluções eficientes e bem conhecidas.

- O primeiro livro a reunir um conjunto de padrões é o GoF (Gang of Four), apelido para _Design Patterns: Elements of reusable object-oriented software,_ pois foi desenvolvido por 4 profissionais da área.

Dessa forma, passamos a falar de implementações em alto nível como fábricas, fachadas, observadores etc.

O livro descreve 23 padrões com um formato bem definido

![[image 136.png|image 136.png]]

Existem três categorias de padrões:

- Criação (formas de criar novos objetos)

- Estruturais (organização de estruturas de dados complexas, com diversos objetos)

- Comportamentais (dinâmica de um sistema para torná-lo mais flexível e robusto).

  

## Padrão Estratégia (315) - Comportamento

![[image 1 103.png|image 1 103.png]]

![[image 2 82.png|image 2 82.png]]

  

A classe estratégia é abstrata, e na execução do programa determina-se qual subclasse concreta de fato implementa o método, introduzindo variações específicas.

Exemplo (salvador de figura)

![[image 3 70.png|image 3 70.png]]

No exemplo, a classe editor de figuras possui um apontador chamado _salvador_ que é de uma classe de estratégia. Essa classe possui as suas subclasses que determinam o formato do salvamento.

- Substitui-se herança (três classes editor de figura, uma por formato) por delegação.

Nesse outro exemplo, criamos uma superclasse pato com dois objetos da interface FlyBehavior e QuackBehavior. Isso porque o pato pode ter comportamentos diferentes a depender do seu tipo. Na construção do objeto, definimos esse objeto como uma das classes que implementam a interface.

![[image 4 55.png|image 4 55.png]]

  

## Padrão Adaptador - Estrutural

![[image 5 39.png|image 5 39.png]]

O adaptador é uma classe que funciona entre duas interfaces que inicialmente não eram capazes de trabalhar entre si, seja pela diferença no nome dos atributos, ou dos parâmetros, etc.

![[image 6 27.png|image 6 27.png]]

No exemplo, o cliente chama o método A, que por sua vez chama o método B, agora adaptado.

Outra implementação é criando a classe adaptadora como uma subclasse da interface não compatível.

![[image 7 23.png|image 7 23.png]]