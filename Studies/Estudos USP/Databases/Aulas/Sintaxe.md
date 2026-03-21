---
Course:
  - "[[Organização de Arquivos]]"
Last Edited: 2025-08-23T00:29
---
É importante adicionar uma linha para abrir o arquivo como forma de leitura/escrita e ao final uma linha para fechar o arquivo. (**critério de avaliação do trabalho**).
Podemos escrever a estrutura da memória como forma de pilha dinâmica. Nela, os nós são registros, e cada registro possui um apontador para o próximo nó/registro. 
Para registros removidos, criamos um algoritmo que une os nós removidos em uma pilha.


~~~ 
#Algoritmo de Remoção
abrir o arquivo para escrita
ler o valor do próximo RRN do registro de cada cabeçalho
se RRN < prox RN
	então byteoffset <- RRN * tamREG
	ler o registro
	se o registro não estiver marcado como logicamente removido
		então marca oo registro como logicamente removido
			#empilha os registros removidos
			escrever o RRN do topo no campo de pilha do registro
			escrever o RRN atual no topo
	senão escreve na tela "registro removido/registro não encontrado"
senão escreve na tela "registro removido/registro não encontrado"
~~~

O algoritmo de empilhamento cria uma pilha, com cada nó contendo o RRN do último registro removido (o RRN do topo mencionado).
- O topo consiste em uma variável presente no cabeçalho do arquivo, assim como o próximo RRN.

O RRN do topo também é útil para sobrescrever em registros removidos. Ao invés de acessar o byte offset do próximo RRN, utilizamos o do topo e na inserção de um novo registro utilizamos essa posição.
- Antes disso é importante atualizar o RRN do topo para o registro removido antes do atual, sendo que esse valor vai estar no registro atual.
- Marcamos o topo com -1 para dizer que não houve remoções. Por isso é importante verificar se de fato houve registros removidos, e se o valor do topo for -1 usamos o valor do próximo registro.