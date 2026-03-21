---
Course:
  - https://www.notion.so/Sistemas-Digitais-24efa7f60cd88051b6bbd3e70ffc8e89?pvs=21
Last Edited: 2025-12-13T12:47
---
Registradores são circuitos compostos por uma sequência de flip-flops, sendo capaz de guardar bits de informação.

- _n_ flip-flops guardam _n_ bits.

- Todos os flip-flops compartilham de um mesmo clock.

- Podemos carregar os bits um por vez, a cada ciclo de clock um novo bit entrando, e isso se faz ligando a entrada dos bits no primeiro FF e, a partir dele, ligando a saída de um FF na entrada do próximo. Esse tipo de entrada é chamada de serial.

![[image 87.png|image 87.png]]

- Podemos carregar os bits nos registradores todos de uma vez, o que se faz ligando uma entrada diferente para cada flip-flop, e esse tipo de entrada é chamada de paralela.

### Shift Register

Shift register são capazes de multiplicar ou dividir o número em bits guardados ao deslocá-lo para a direita ou para a esquerda.

![[image 1 65.png|image 1 65.png]]

# Contadores

Contadores são circuitos também compostos por FF’s e que são capazes de a cada ciclo de clock, aumentar (ou diminuir em algumas aplicações), o valor da saída em uma quantidade sempre igual.

O tipo de FF mais utilizado é o tipo T, tendo em vista que ele detém a propriedade de _toggle_ na saída.

Duas outras entradas podem aparecer:

- Clear: zera todos os FFs. É importante para recomeçar a contagem.

- Preset: é um valor que é carregado independentemente da entrada.

### Assíncronos

Os contadores assíncronos são caracterizados pelo fato de que um FF só funciona quando o antecessor estiver desligado. Isso acontece porque a entrada de clock de um FF é alimentada pela saída Q’ do FF anterior.

- Devido ao fato de que a entrada do clock depende da saída do FF anterior, existe um grande delay para contar números muito grandes.

![[image 2 53.png|image 2 53.png]]

### Síncronos

Os contadores síncronos são caracterizados pelo fato de que todos os FFs compartilham de um mesmo _clock_.

![[image 3 45.png|image 3 45.png]]

![[image 4 39.png|image 4 39.png]]

De forma geral, a entrada D de cada flip-flop é dada por:

![[image 5 28.png|image 5 28.png]]

Uma entrada paralela necessita simplesmente de um MUX na entrada D de cada FF, cujos valores são o valor a ser carregado ou o valor que o contador normalmente geraria.

![[image 6 20.png|image 6 20.png]]

## Ring Counter

A diferença consiste no fato de que a saída do último FF conecta-se na entrada do primeiro.

![[image 7 17.png|image 7 17.png]]

o Ring Counter necessita que no primeiro ciclo de clock o FF-0 seja carregado com 1 pelo preset. Nos próximos ciclos ele é igual a 1, e a contagem segue normalmente.

No segundo ciclo, o FF-1 é carregado com 1 da saída FF-0 e o FF-0 é carregado com 0 da saída FF-3.

![[image 8 13.png|image 8 13.png]]

### Johnson Counter

![[image 9 9.png|image 9 9.png]]

![[image 10 7.png|image 10 7.png]]