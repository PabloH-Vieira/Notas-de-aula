---
Course:
  - https://www.notion.so/L-gica-Digital-1c1fa7f60cd88012b3fee27ba8aaeae7?pvs=21
Last Edited: 2025-10-06T21:47
---
A ideia do MUX é combinar/selecionar uma certa quantidade de entradas para uma outra quantidade inferior de saídas.

- Paralelo → Serial.

- Os bits de seleção devem contemplar todas as possibilidades de entrada.

![[image 60.png|image 60.png]]

Os seletores são o fator que determina como as entradas será combinada para resultar na saída.

- No exemplo, S0 e S1 vai selecionar qual valor entra em C para repetir na saída.

  

É possível fazer uma tabela verdade com os resultados da saída e a partir dela construir um circuito que retorna o mesmo resultado do multiplexador.

![[image 1 44.png|image 1 44.png]]

Para uma quantidade grande de entradas, como o mux 4 para 1, não é prático fazer tabelas verdades ou mapas de Karnaugh, mas podemos resumir tudo em uma tabela de funcionamento.

![[image 2 35.png|image 2 35.png]]

Para simular o funcionamento de um multiplexador, podemos utilizar um [decodificador,](https://www.notion.so/Encoders-Decoders-20ffa7f60cd880dc8451f5e2e7446d72?pvs=21) o qual seleciona apenas uma saída para ter valor 1.

- Haverá uma chave para cada entrada, e somente aquela que corresponde à saída selecionado pelo decoder vai permitir a continuidade do circuito. Essa chave pode ser implementada por um simples AND.

![[image 3 28.png|image 3 28.png]]

Ou ainda

![[image 4 25.png|image 4 25.png]]

## Associação de Multiplexadores

Podemos utilizar multiplexadores para construir um circuito com o funcionamento de um multiplexador que tenha mais bits ou que tenha mais entradas.

**Multiplexador com entradas de 4 bits e saída com os 4 bits da entrada selecionada**

![[image 5 19.png|image 5 19.png]]

Outro exemplo é para implementar circuitos com informações mais extensas, como no exemplo:

![[image 6 13.png|image 6 13.png]]

### Associação em Cascata

É utilizado para construir um multiplexador de mais entradas usando multiplexadores de menos entradas.

![[image 7 12.png|image 7 12.png]]

![[image 8 9.png|image 8 9.png]]

---

# Demux

Inversamente ao multiplexador, o demux vai ter como entrada uma certa quantidade de entradas e terá como saída uma outra quantidade superior de saídas.

- A informação dessa entrada será transmitida para alguma das saídas, enquanto as demais terão valor 0.

- Serial → Paralelo.

![[image 9 5.png|image 9 5.png]]

- No exemplo, os seletores A e B vão indicar para qual saída o valor de Z irá.

A lógica de funcionamento de um decodificador com entrada de habilitação corresponde ao funcionamento de um demultiplexador.