---
Course:
  - https://www.notion.so/Sistemas-Digitais-24efa7f60cd88051b6bbd3e70ffc8e89?pvs=21
Last Edited: 2025-12-13T13:33
---
Um circuito combinatório não guarda valores das entradas para que possam ser utilizados posteriormente. Tal característica é exclusiva dos circuitos sequenciais.

- Circuitos sequenciais têm memória, e guardam valores introduzidos no circuito anteriormente.

Os circuitos responsáveis por guardar essa memória são os _latches_ ou _flip-flops._

- _Latches_ são sensíveis ao nível de entrada do sinal.

- _Flip-flops_ são sensíveis à borda do sinal de entrada.

Existem alguns tipos de cada um desses circuitos.

### Latch RS (Set-Reset)

Esse circuito tem as entradas _set_ e _reset_ e as saídas $Q$ e $\overline{Q}$.

- Set torna a saída Q para valor 1.

- O Reset torna a saída Q para valor 0.

- Uma entrada proibida é 1 para Set e Reset, pois isso quebra a lógica do circuito definindo as saídas $Q$ e $\overline{Q}$ para o mesmo valor, o que levar a comportamento imprevisível.

  

![[image 86.png|image 86.png]]

![[image 1 64.png|image 1 64.png]]

### Gated RS

O gated latch RS funciona igualmente ao latch RS usual, com a diferença de que existe uma terceira entrada, o ENABLE, que dita se a entrada R ou S vão funcionar. Se ela estiver desabilitada, independentemente dos valores de R e S, a saída permanecerá a mesma. Essa terceira entrada é o _clock._

![[image 2 52.png|image 2 52.png]]

![[image 3 44.png|image 3 44.png]]

Circuito do gated latch RS

### Circuito sequencial: síncrono e assíncrono

Circuitos sequenciais podem ser síncronos ou assíncronos.

- Assíncrono: a alteração nas saídas ocorre em qualquer instante, de acordo com a alteração na entrada.

- Síncrono: as alterações nas saídas acontecem em momentos específicos, sincronizadas com o sinal de uma entrada especial chamada clock.
    
    - é um sinal periódico, com valores de 1 e 0. A passagem do sinal pode ser definido para qualquer um dos dois, mas existe um intervalo de oscilação para passar o sinal.
    

![[image 4 38.png|image 4 38.png]]

![[image 5 27.png|image 5 27.png]]

### Latch D

O latch D tem apenas uma entrada D. O circuito funciona a partir dessa entrada e de seu complemento.

Seu comportamento visa prevenir a combinação proibida no Set e Reset.

- Quando o _clock_ tem valor 1, o valor da entrada é passado para a saída. Quando 0, esse valor fica retido.

![[image 6 19.png|image 6 19.png]]

![[image 7 16.png|image 7 16.png]]

### Latch JK

Possui duas entradas J e K, análogas ao _set_ e _reset._

![[image 8 12.png|image 8 12.png]]

![[image 9 8.png|image 9 8.png]]

O clock faz com que a saída oscile em valor, e por isso é desejável reduzir ao máximo o período de oscilação.

Para minimizar esse efeito, podemos utilizar a configuração mestre-escravo.

- Utilizamos dois flip-flops: um é o mestre e o outro é o escravo.

![[image 10 6.png|image 10 6.png]]

## Flip-Flops sensíveis à borda

Borda refere-se a um instante específico para armazenar a informação. A borda trata-se do exato momento em que o sinal muda de valor.

Isso é importante porque em alguns casos os valores das variáveis mudam múltiplas vezes durante um mesmo ciclo do _clock_, o que causa resultados inconsistentes na saída.

O tempo de borda é muito curto, o que inibe o circuito de atualizar o valor das variáveis múltiplas vezes.

- Borda de subida: 0 → 1.

- Borda de descida: 1 → 0.

![[image 11 5.png|image 11 5.png]]

Uma das formas de aplicar os flip-flops é a partir do **Flip-Flop D Mestre-Escravo.**

- Usamos dois _latches_ D (o primeiro é o mestre e o segundo o escravo) e uma porta NOT no _clock_.

- A saída do bloco de memória é a saída do escravo, e a entrada do escravo é a saída do mestre.

![[image 12 3.png|image 12 3.png]]

![[image 13 3.png|image 13 3.png]]

- Perceba que o valor da saída QM muda apenas quando o mestre está habilitado.

- O valor da saída QE muda apenas quando o escravo está habilitado, copiando o último valor da saída QM.

Esse exemplo funciona a base da borda de descida, mas é possível fazer isso para uma borda de subida alterando duas coisas: mudamos a posição da porta NOT e invertemos o sinal do _clock._

![[image 14 3.png|image 14 3.png]]

Diferenciamos um _latch_ de um _flip-flop_ a partir de um triângulo na entrada do _clock._ O funciona é por porta de descida se houver um outro triângulo e de subida se houver um círculo

![[image 15 3.png|image 15 3.png]]

### Flip-Flop JK

O flip-flop JK pode ser construído a partir do flip-flop D. Possui duas entradas, Je K: elas controlam o sinal que está armazenado.

Há quatro ações possíveis:

- Setar (10): saída Q vai para 1.

- Resetar(01): saída Q vai para 0.

- Manter(00): saída Q mantém o valor atual.

- Complementar(11): invertemos o sinal da saída Q.

![[image 16 2.png|image 16 2.png]]

![[image 17 2.png|image 17 2.png]]

![[image 18 2.png|image 18 2.png]]

### Flip-Flop T

O flip-flop T pode ser construído utilizando um flip-flop JK o qual ambas as entradas tem o mesmo sinal T.

Existem apenas duas combinações possíveis.

![[image 19 2.png|image 19 2.png]]

A partir de um FF-D:

![[image 20 2.png|image 20 2.png]]