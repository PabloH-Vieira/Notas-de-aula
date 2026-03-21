---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-09-21T13:59
---
O significado de polimorfismo significa muitas formas. Existem três tipos em Java:

- Paramétrico;

- Sobrecarga (overloading);

- Sobreescrita de métodos (overiding)

### Paramétrico

Relacionado à programação genérica. Fazemos tipos genéricos funcionar a partir de outros tipos.

- É o caso do array list. Ele recebe como parâmetro um outro tipo.

- Dessa forma, uma classe funciona para diferentes tipos.

![[image 133.png|image 133.png]]

### Sobrecarga de métodos

Dois ou mais métodos podem ter o mesmo nome, mudando apenas os tipos dos parâmetros.

- Um mesmo método recebe dois parâmetros definidos pelo usuário. O método vai funcionar de acordo com os parâmetros, ainda que o usuário chame o mesmo nome.

![[image 1 101.png|image 1 101.png]]

### Sobreescrita

Relacionado à herança/subtipos. Pensamos em uma classe filha que possui a mesma assinatura do método da classe mãe.

Escrevemos o método pensando unicamente na classe mãe, mas a depender de qual classe filha o usuário utilizar, o método será diferente.

- Os métodos da classe filha possuem versões polimórficas do método da mãe.

- Desta forma escrevemos um método que poderá ser utilizados em subclasses que sequer existem ainda, mas que, quando existirem, funcionarão.

![[image 2 80.png|image 2 80.png]]

---

**Exemplo**

![[image 3 68.png|image 3 68.png]]

No exemplo, o método main recebe o custo total e o imprime.

Outra forma de mostrar o custo total seria através do `System.out.println(Empregado)` , isto é, fazemos o print com um objeto. Isso vai fazer com que se execute o método `public string toString` de cada objeto no `ArrayList` . Não havendo esse método no objeto, ele vai procurá-lo na classe mãe até achar (ele sempre acha na classe `Object`, que imprime o nome do objeto e o endereço na memória).