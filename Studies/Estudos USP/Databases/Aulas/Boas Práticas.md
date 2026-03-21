---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-09-04T22:37
Related to Semestres:
  - "[[Estudos Complementares]]"
---
- Bons nomes para variáveis, atributos e argumentos de métodos de classes.
    
    - _intetion revealing names_
    
    - uma boa prática é nomear classes como substantivos, métodos como verbos.
    

- Boa bateria de testes automatizados (um código que testa outro código).

- Uso de arcabouços/frameworks para implementar os testes esquematizados (SUnit, Junit, CPPUnit, Pytest)

- Existe uma metodologia chamada TDD (Test Driven Development), onde guia-se a escrita do código para o programa a partir da escrita de testes
    
    - escrevemos o teste e depois o código a ser testado. Isso para cada funcionalidade.
    

- Revisão por pares: outros programadores podem identificar erros e implementar melhorias.

---

Herança é um instrumento muito poderoso, mas que pode tornar o código muito inflexível se aplicada a uma hierarquia muito profunda.

- Saber utilizar! Evitar hierarquias profundas demais.

- O uso de delegação leva a sistemas mais simples e flexíveis, isto é, a partir de classes independentes.

---

Encapsulamento consiste em agrupar códigos e dados, levando em conta o que a classe deve expor ao cliente.

- Encapsular significa esconder parte do código, decidindo o que mostrar ou não da classe.

- Uma classe não deve mexer nos atributos de outra.

Modularização é organizar o sistema em módulos:

- um sistema orientado a objetos devem possuir classes que possuem uma única responsabilidade no funcionamento do sistema (uma classe não deve tratar de assuntos diferentes).
    
    - não há problema em quebrar uma classe em outras se ela tiver desempenhando mais de uma função no sistema.
    

---

Minimizar o acoplamento entre as classes, ou seja, o quanto uma classe conhece do seu entorno. Isso significa reutilizar nomes de outras classes, o que pode gerar confusão ao utilizar essas diversas classes no sistema.

- Muitas referências a outras classes.

- Referências a tipo muito específicos (métodos de classes que realizam tarefas muito específicos).

Classes muito acopladas são poucos acopladas e pouco reutilizáveis.

---

Refatoração é um elemento chave no dia a dia do desenvolvedor. Significa pensar em novas formas de melhorar a arquitetura do sistema utilizado, de forma a torná-lo mais simples.

- Refatorar significa reestruturar o código, sem alterar sua função, mas tornando-o mais claro e otimizado (melhoria contínua).