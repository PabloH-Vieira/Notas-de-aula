---
Course:
  - "[[Modelagem Comp. em Grafos]]"
Last Edited:
---
Processamento X Busca?

## Busca em profundidade

Em grafos, não basta encontrar um nó. É necessário saber o caminho percorrido para chegar até ele. Para isso, existem algumas estratégias:
- Colorização: marcamos os nós levando em consideração se eles foram visitados ou não: um grafo não visitado tem a cor branca, um grafo visitado uma única vez tem cor cinza, enquanto um grafo que, além de ter sido visitado, ter seus filhos visitados, tem cor preta.
- Time-stamp: cada grafo guarda um campo onde será registrado em que momento da sequência de busca ele foi visitado. É como um índice que marca o momento em que o grafo foi visitado na linha do tempo.
- Guardamos um vetor predecessor, com a sequência de nós visitados até chegar no destino.

A ordenação topológica segue a lógica de uma busca em profundidade, com o objetivo de alinhar os vértices de um grafo em uma sequência, de forma que se (u, v) pertencer ao vértice V, u aparece antes de v na sequência.
![[Pasted image 20260408105237.png]]
Na imagem acima, o algoritmo de ordenação topológica utiliza uma lógica de dois tempos para o vértice: o tempo de descoberta (primeiro acesso) e do tempo de término (quando verifica que acessou todos os vizinhos).
O algoritmo inicia escolhendo um nó não visitado e vai percorrendo o caminho pelas setas, marcando os tempos de descoberta. Ao chegar no fundo, ele faz o caminho inverso com recursão, marcando os tempos de término.
Se ainda houver nós ou grupos isolados ele recomeça a ordenação a partir deles.
Por fim, exibimos a lista em ordem decrescente dos tempos términos.

O algoritmo para esse processo consiste em chamar a função DFS para todos os vértices do grafo (isto é, enquanto existirem brancos), e a cada vértice terminado (isto é, se tornaram pretos), inserimos-no na cabeça de uma lista.
- Assim, a lista vai sendo preenchida como uma pilha. A cada novo vértice completado, adicionamos-no no início da lista.
- Um vértice só é marcado como preto se o vizinho ao qual ele apontar já ter sido visitado.
- Após um vértice ter sido marcado como finalizado, voltamos recursivamente para o nó que nos levou até aquele.

![[Pasted image 20260408111240.png]]

## Busca em largura

A busca em largura consiste em um algoritmo capaz de visitar todos os vértices de um grafo. Dado um vértice inicial, descobre todos os vértices alcançáveis, calcula a distância até cada um deles e cria uma árvore com raiz no vértice inicial.
No BFS, a lógica é visitar todos os vizinhos adjacentes, e enquanto estiverem cinzas, eles ficam na pilha. Ao acessar os adjacentes deste, ele fica preto, e o desimpilhamos, isto pe, adicionamos os adjacentes dele (agora cinzas) em seu lugar na pilha.
Ao final, a pilha estará vazia, pois não haverá mais vértices para desempilhar.![[Pasted image 20260413104956.png|579]]![[Pasted image 20260413105006.png|586]]

A complexidade é de O (V + E), seja V os vértices e E as arestas. 
Todos os vértices são empilhados/desempilhados no máximo uma vez.