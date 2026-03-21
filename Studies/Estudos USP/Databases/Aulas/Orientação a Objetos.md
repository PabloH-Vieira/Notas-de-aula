---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-09-04T22:37
Related to Semestres:
  - "[[Estudos Complementares]]"
---
É possível criar uma classe vazia e depois adicionar atributos e métodos. Para denotar que ela é vazia, utilizamos a palavra `pass` .

Para isso, chamamos o objeto e passamos os novos atributos utilizando um ponto depois do nome da classe e então definimos um valor.

- Isso em Python não requer tipagem.

![[image 129.png|image 129.png]]

Ao igualar dois objetos, o objeto à esquerda passa a estar no mesmo endereço do outro objeto. Assim, alterações em qualquer um dos dois alterará o outro.

O construtor é um método essencial para a criação de classes, e são chamadas automaticamente pelo compilador ao instanciar novos objetos. Através da sua declaração, podemos passar variáveis como parâmetros para os atributos.

Em Python, utilizamos a notação `def __init__` e passamos como parâmetro obrigatório `self` (necessário para que o interpretador reserve um espaço de memória para o objeto) e depois dele todos os atributos que poderão ter seus valores definidos pelo usuário.

- Dentro da classe criamos as classes utilizando `self.atribut=variavel_parametro` .

- Instanciamos dando um nome ao objeto e declaramos chamando o nome da classe e passando como argumento os valores que os atributos terão.

- Criamos um método usando a palavra `def` . Em todos os métodos, passamos como primeiro parâmetro o valor `self` .