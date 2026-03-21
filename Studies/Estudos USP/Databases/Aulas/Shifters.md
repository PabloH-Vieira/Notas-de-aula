---
Course:
  - https://www.notion.so/Sistemas-Digitais-24efa7f60cd88051b6bbd3e70ffc8e89?pvs=21
Last Edited: 2025-12-13T13:33
---
## Barrel Shifter

O **Barrel Shifter** (Deslocador de Barril) é um circuito digital capaz de deslocar ou rotacionar uma palavra de dados em um número específico de bits em **um único ciclo de clock**.

Diferente de um registrador de deslocamento comum (que desloca apenas 1 bit por vez), o Barrel Shifter usa lógica combinacional para "teletransportar" os bits para suas novas posições instantaneamente.

Assim, utilizamos um MUX cujas entradas são os bits que a entrada pode receber em razão da quantidade de shifts. Uma mesma chave seletora é comum para todos os MUX.

![[image 89.png|image 89.png]]