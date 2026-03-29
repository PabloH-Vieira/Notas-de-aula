---
Course:
  - "[[Modelagem Comp. em Grafos]]"
Last Edited:
---
## Busca em profundidade

Em grafos, não basta encontrar um nó. É necessário saber o caminho percorrido para chegar até ele. Para isso, existem algumas estratégias:
- Colorização: marcamos os nós levando em consideração se eles foram visitados ou não: um grafo não visitado tem a cor branca, um grafo visitado uma única vez tem cor cinza, enquanto um grafo que, além de ter sido visitado, ter seus filhos visitados, tem cor preta.
- Time-stamp: cada grafo guarda um campo onde será registrado em que momento da sequência de busca ele foi visitado. É como um índice que marca o momento em que o grafo foi visitado na linha do tempo.
- Guardamos um vetor predecessor, com a sequência de nós visitados até chegar no destino.


- [ ] 