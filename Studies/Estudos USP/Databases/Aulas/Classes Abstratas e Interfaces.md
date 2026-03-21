---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-09-23T23:01
---
Define que um objeto terá um determinado método, mas sem implementá-lo.

Nesse caso, a implementação do método abstrato acontece em uma subclasse da classe abstrata.

- Uma classe não é abstrata apenas se não tiver nenhum método abstrato. Por isso, as subclasses devem implementar os métodos da superclasse.

![[image 131.png|image 131.png]]

No entanto, as interfaces são muito mais utilizadas para desempenhar essa mesma função.

## Interface

Consiste em uma classe puramente abstratas, pois todos os seus métodos são abstratos. É um conjunto de operações que outras classes vão implementar.

Declaramos a classe com a palavra-chave `implements` para determinar que ela herda os métodos da interface e os implementa.

- Várias classes podem implementar a mesma interface.

Uma mesma classe pode herdar várias interfaces, diferentemente do que ocorre com classes.

Também existe herança de interfaces.