---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-09-29T23:31
---
Lógica _first-in_, _first-out_. Uma implementação possível utilizando ponteiros é designar um início e um fim da fila. A cada retirada, avançamos o _front._ A cada entrada, avançamos o _back._

Precisamos lidar com o tamanho da fila, e otimizar o seu uso. Ao remover um elemento da fila de modo que libere-se espaço nas primeiras posições do array, podemos adicionar novos elementos nessas posições, ainda que o _back_ esteja nas posições finais.

- Seguindo essa lógica, o nosso array funciona como um círculo, de modo que, se não houver espaço nas posições finais, podemos inserir elementos na fila nas posições liberadas.

- No entanto, isso faz com que a relação _front_ e _back,_ que poderia nos informar que a fila está cheia, deixa de funcionar. Para identificar uma fila cheia, ao invés disso, usamos um contador de elementos comparando-o ao tamanho do array.

  

## Fila Linear (estática)

A fila linear é a forma de lista mais ineficiente, pois existe um problema onde posições do vetor estejam livres e ainda sim o programa considera o vetor cheio.

- Isso acontece quando removemos elementos. O primeiro é removido, e a posição do front é atualizada. No entanto, o adicionar ao final não preenche esses espaços vazios nas posições iniciais do vetor.

**Header**

```C++
\#ifndef FilaLin
\#define FilaLin

typedef struct Fila {
	int *itens;
	int front; // indice do primeiro elemento na fila
	int back;  // indice do ultimo elemento na fila
	int MAX;   // capacidade da fila
	int qtd;   // quantidade de elementos na fila

	// construtor
	Fila(int n = 100);
	// destrutor
	~Fila();

	// métodos clássicos
	bool empty();
	bool full();

	// insere elemento no FIM fila. algumas implementacoes
	// nomeiam esta funcao de push (como em pilha)
	bool queue(int val);
	// retira elemento do INICIO da fila. Também conhecido como pop()
	bool dequeue(int *); 
	
	int size();
	void printQueue();

}Fila;

\#endif
```

**Implementação**

```C++
\#include <cstdio>
\#include "filaLin.hpp"

/*
Pre-cond: a quantidade n de elementos (default = 100)
Pos-Cond: aloca-se uma fila de tamanho n,
com front sendo o indice do 1o elemento da fila,
back sendo o indice do ultimo inserido.
Como back está sempre atrás de front, entao
faremos: front = 0 e back = -1
*/

Fila::Fila(int n){
	itens = new int[n];
	MAX = n;
	qtd = 0;
	front = 0;
	back = -1;

}

/*
Pre-cond: a fila existe
Pos-cond: libera a heap alocada na construcao
*/
Fila::~Fila(){
	delete[] itens;
}

/*
Pre-cond: A fila existe
Pos-cond: retorna true, caso a fila nao tenha elementos
*/
bool Fila::empty(){
	return qtd == 0 ? true : false;
}

bool Fila::full(){
	return back == MAX-1 ? true : false;
}

/*
Pre-cond: A fila existe
Pos-cond: Insere elemento na fila, se nao cheia.
Se estiver cheia, retorna false; Senao, retorna true
*/
bool Fila::queue(int valor){
	if (full()){
		printf("A fila está cheia\n");
		return false;
	}
	// insere no fim da fila.
	// para isso, primeiro avança back e depois insere
	back++;
	itens[back] = valor;
	qtd++;
	return true;
}


/*
Pre-cond: A fila existe
Pos-cond: em valor elemento da frente da fila, 
se nao vazia.
Se estiver vazia, retorna false; Senao, retorna 1
*/
bool Fila::dequeue(int *valor){
	if (empty()){
		printf("A fila está vazia\n");
		return false;
	}
	// retira do inicio da fila.
	// para isso, primeiro avança back e depois insere
	*valor = itens[front];
	front++;
	qtd--;
	return true;
}

int Fila::size(){
	return qtd;
}

/*
Pre-cond: A fila existe
Pos-cond: Imprime os elementos da fila, do
inicio para o fim
*/
void Fila::printQueue(){
	for (int i = front; i <= back; i++){
		printf("%d ", itens[i]);
	}
	printf("\n");
}
```

## Lista com nó (dinâmica)

**Header**

```C++
\#ifndef FilaLin
\#define FilaLin

typedef struct No{
	int item;
	struct No *prox;
}No;

typedef struct Fila {
	No  *front; // ponteiro para o inicio da fila
	No *back;  // ponteiro para o fim da fila
	int qtd;   // quantidade de elementos na fila

	// construtor
	Fila();
	// destrutor
	~Fila();

	// métodos clássicos
	bool empty();


	// insere elemento no FIM fila. algumas implementacoes
	// nomeiam esta funcao de push (como em pilha)
	bool queue(int val);
	// retira elemento do INICIO da fila.
	// também conhecido como pop()
	bool dequeue(int *); 

	int size();

	void printQueue();

}Fila;

\#endif
```

**Implementação**

```C++
\#include <cstdio>
\#include "filaNo.hpp"


/*
Pre-cond: nada...
Pos-Cond: Uma fila sem elementos tem back e 
front apontando para nullptr !!!
e a qtd = 0; 
*/

Fila::Fila(){
	back = nullptr;
	front = nullptr;
	qtd = 0;
}

/*
Pre-cond: a fila existe
Pos-cond: libera todos os nos do inicio ao fim
*/
Fila::~Fila(){
	No * temp;
	while (front != nullptr){
		No *temp = front->prox;
		delete front;
		front = temp;
	}
}

/*
Pre-cond: A fila existe
Pos-cond: retorna true, caso a fila nao tenha elementos
obs: vc poderia usar front e back para indicar fila
vazia nesta implementacao???
*/
bool Fila::empty(){
	return qtd == 0 ? true : false;
	//return  front == nullptr && back == nullptr ? true : false;
}


/*
Pre-cond: A fila existe
Pos-cond: Insere elemento na fila, se houver heap!
Se memoria cheia, retorna false; Senao, retorna true
*/
bool Fila::queue(int valor){
	No * temp = new No;
	if (temp == nullptr){
		printf("Falha na alocacao do nó\n");
		return false;
	}
	temp->item = valor; // transfere o valor
	temp->prox = nullptr; // eh sempre o ultimo no da lista ligada..
	//se a fila nao possui nenhum elemento ainda
	// front e back devem apontar para temp
	if (empty()){
		//back = temp;
		front = temp;
	} 
	// back sempre aponta para o ultimo inserido
	else {
		back->prox = temp; // liga no anterior a temp
		//back = temp;
	}
	back = temp; // back sempre aponta para o ultimo inserido
	qtd++;

	return true;
}


/*
Pre-cond: A fila existe
Pos-cond: coloca em 'valor' elemento da frente 
da fila, se nao vazia.
Se estiver vazia, retorna false; Senao, retorna 1
*/
bool Fila::dequeue(int *valor){
	if (empty()){
		printf("A fila está vazia\n");
		return false;
	}
	*valor = front->item; // retorna elemento da frente
	qtd--;
	No *temp = front; // auxiliar aponta para front
	front = front->prox; // avanca front

	// caso este seja o unico elemento da fila,
	// back tem que ser atualizado
	if (front == nullptr)
		back = nullptr;
	
	delete temp;

	return true;
}

int Fila::size(){
	return qtd;
}

/*
Pre-cond: A fila existe
Pos-cond: Imprime os elementos da fila, do
inicio para o fim
*/
void Fila::printQueue(){
		for (No *temp = front; temp!= nullptr; temp = temp->prox)
			printf("%d ", temp->item);;

	printf("\n");
}
```

- Os casos especiais já foram tratados, isto é, quando removemos um elemento de uma lista de elemento único, quando adicionamos o primeiro elemento e quando tentamos remover de uma lista vazia ou adicionar em uma cheia.