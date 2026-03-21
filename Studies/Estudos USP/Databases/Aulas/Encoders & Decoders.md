---
Course:
  - https://www.notion.so/L-gica-Digital-1c1fa7f60cd88012b3fee27ba8aaeae7?pvs=21
Last Edited: 2025-08-09T11:53
---
# Decodificadores

No circuito decodificador, transformamos uma entrada de _n_ bits em no máximo 2$^n$ saídas, mas pode ter outros valores.

Ao passar pelo decodificador, os bits de entrada corresponderão a apenas uma saída (escolhido a depender dos valores de entrada), e essa será a única com valor 1.

Decodificadores comuns:

- 2x4.

- 3x8 (Binário → Octal).

- 4x10.

- 4x16(Binário → Hexadecimal).

![[image 61.png|image 61.png]]

A expressão para cada saída é simplesmente o minitermo das entradas.

![[image 1 45.png|image 1 45.png]]

Para os casos em que a quantidade de saídas possíveis é maior do que as saídas existentes, existem duas alternativas:

- **Mínimo risco**: as entradas não mapeadas não ativam nenhuma saída.

- **Mínimo custo:** utilizar _don’t care_ em todas as entradas não mapeadas.

  

Em alguns casos pode ser necessário utilizar mais uma entrada, a de habilitação. Ela indica se o decodificar vai funcionar ou não.

- Para tal, essa entrada vai estar presente em cada saída como um AND junto ao minterm.

![[image 2 36.png|image 2 36.png]]

Um dos usos disso é para interligar dois decodificadores.

![[image 3 29.png|image 3 29.png]]

---

# Codificador

O codificar realiza a operação inversa de um decoder.

- A entrada é a dado de informação, enquanto a saída é o código binário que corresponde àquela entrada.

- Possui até 2$^n$ entradas e _n_ saídas.

Apenas uma entrada possui valor lógico 1.

![[image 4 26.png|image 4 26.png]]