---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-II-24efa7f60cd880bbbbcaf479fda73ab6?pvs=21
Last Edited: 2025-11-16T01:56
---
A busca por interpolação pode ser extremamente rápida, mas necessita ter um vetor muito bem organizado.

- É necessário que as chaves, os valores do vetor, estejam uniformemente distribuídos.

- Fazemos um chute de onde o valor pode estar com base em resultados de probabilidade.

- Se o chute estiver errado, a área de busca é diminuída, e um novo cálculo de probabilidade é realizado.

O cálculo para encontrar a provável posição do valor buscado segue uma fórmula, implementada no algoritmo abaixo, dentro de um loop que, quando não encontra o valor define novos limites da área de busca.

- Caso o valor calculado for menor que o buscado, então o limite inferior da busca será igual a posição `probe+1` .

- Caso o valor calculado for maior que o buscado, então o limite superior da busca será igual a posição `probe-1` .

![[image 118.png|image 118.png]]

### Complexidade

O caso médio tem complexidade $O(\log {(\log n))}$ e o pior $O(n)$.