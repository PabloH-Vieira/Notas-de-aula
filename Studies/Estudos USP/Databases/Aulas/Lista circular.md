---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-10-01T11:04
---
A lista circular soluciona um problema da fila usual. Ao removermos elementos das primeiras posições, a fila agora não será mais vista como cheia ao chegar à extremidade do vetor. Ao invés disso, novas inserções vão ocupar as primeiras posições, ainda assim mantendo a lógica de fila.

**Header**

```C++
/*
Só que desta feita, a lista tem o que chamamos de NO SENTINELA (cabeça)
Mas que usaremos para armazenar o valor da chave durante a busca....

Ja que a lista é circular, vamos precisar somente de um ponteiro
para o FIM da fila, pois este apontará para o nó sentinela !!!!
*/


\#ifndef LISTA
\#define LISTA

// na lista podemos armazenar qq coisa.
// para fins didáticos, usaremos uma lista de inteiros.

typedef int item;

typedef struct No{
	item data;
	struct No *prox;

	// vamos criar um construtor para o No, de forma que já deixamos
	// ele pronto para uso !!!!!
	No(item valor = -1){
		data = valor;
		prox = nullptr;
	}

	void set(item valor){
		data = valor;
	}

	item get(){
		return data;
	}

}No;

typedef struct Lista{
	No *head;    // ponteiro para o inicio da fila 
	No *tail;    // ponteiro para o fim da fila.
	int qtd;     // quantidade de elementos
	bool sorted; // sorted = true (ordenada)

	Lista(bool ordenada = false);    // construtor
	~Lista();                // destrutor

	// operações básicas para ambos tipo (ord ou nao ord)
	int size();
	bool empty();
	void printLista();
	bool retiraFim(item *valor);
	bool retiraInicio(item *valor);
	bool retiraPos(item *valor, int pos);
	bool busca(item valor, No **ant, int *pos);
	bool insere(item valor);  
	bool retira(item *valor);

	// para a lista não ordenada
	bool insereFim(item valor);
	bool insereInicio(item valor);
	bool inserePos(item valor, int pos);

	// para listas ordenadas
	bool insereOrdenado(item valor);
	bool insereOrdenado2(item valor);
	bool retiraOrdenado(item valor);
	

}Lista;

\#endif
```

**Implementação do construtor, destrutor e funções básicas**

```C++
\#include <cstdio>
\#include "listaEncCircular.hpp"

using namespace std;

/* CONSTRUTOR
Pre-cond: nenhuma
Pos-cond: cria uma lista (um nó especial) e inicia os atributos head-> prox = null,  
tail = nullptr, qtd = 0 e com o tipo da lista ordenada ou nao (true ou false)
*/
Lista::Lista(bool ord){
	head = new No; // cria um no que aponta para null (e valor -1)
	head->prox = head; // head aponta pra si proprio
	tail = nullptr;
	qtd = 0;
	sorted = ord;
}

//DESTRUTOR
Lista::~Lista(){
	head->set(-1000);
	No *aux = head->prox;
	while(aux->data != -1000){
		No *p = aux;
		aux = aux->prox;
		delete p;
	}
	delete aux;
}

int Lista::size(){
	return qtd;
}

bool Lista::empty(){
	return  qtd == 0 ? true : false;
}

void Lista::printLista(){
	head->set(-1000);
	No *p = head->prox;
	while (p->data != -1000){
		printf("%d ", p->data);
		p = p->prox;
	}
	printf("\n");
}

/*
Pre-cond: a lista existe
Pos-cond: retorna em valor o elemento do fim da lista e indica true.
Se a lista for vazia retorna false;
*/
bool Lista::retiraFim(item *valor){
	if (empty())
		return false;

	*valor = tail->data;

	No *p = head; // no cabeca.

	// procura o no anterior a tail.
	while(p->prox != tail)	 p = p->prox;

	delete tail; // remove o no tail...
	p->prox = head;
	
	qtd--;
	if (qtd == 0) // a lista se tornou vazia
		tail = nullptr;
	else tail = p;
	
	return true;
}

/*
Pre-cond: a lista existe
Pos-cond: retorna em valor o elemento do inicio da lista e indica true.
Se a lista for vazia retorna false;
*/
bool Lista::retiraInicio(item *valor){
	if (empty())
		return false;

	*valor = head->prox->data;

	No *p = head; // no cabeca...
	No *first = p->prox;   // primeiro elemento valido

	if (first == tail) // a lista tem somente um elemento
		tail == nullptr;

	p->prox = first->prox;
	delete first;

	qtd--;

	return true;
}

/*
Pre-cond: A lista existe
Pos-cond: retira o item da posicao pos da lista, e guarda em valor e retorna true
(se a lista nao for vazia e pos for valido) e retorna true.
Caso esteja vazia, retorna false.
*/
bool Lista::retiraPos(item *valor, int pos){
	if (empty() || pos < 0 || pos >=qtd) //validando pos
		return false;

	if (pos == 0)
		return retiraInicio(valor);
	if (pos == qtd-1)
		return retiraFim(valor);

	// p aponta para o no anterior ao do indice pos
	No *p = head->prox;
	int cont = 1;
	while (cont < pos){
		cont++;
		p = p->prox;
	}

	*valor = p->prox->data;
	No *aux = p->prox;
	p->prox = aux->prox;
	delete aux;

	qtd--;
	
	return true;
}

/*
Pre-cond: A lista existe e nao é ordenada
Pos-cond: insere o item no INICIO da lista,
e retorna true.
CAso a lista seja ordenada, retorna false.
*/
bool Lista::insereInicio(item valor){
	if (sorted)
		return false;

	No *p = head;  // no cabeca


	// cria um no
	No *aux = new No(valor);
	aux->prox = p->prox;
	// cabeca aponta para o no criado
	p->prox = aux;
	// se a lista for vazia, tail tem que apontar para aux...
	if (empty())
		tail = aux;
	
	qtd++;

	return true;
}


/*
Pre-cond: A lista existe e nao é ordenada
Pos-cond: insere o item no FIM da lista, se houve espaco
e retorna true.
CAso esteja cheia ou a lista seja ordenada, retorna false.
*/
bool Lista::insereFim(item valor){
	if (sorted)
		return false;


	No *p = head; // no cabeca

	// cria um no
	No *aux = new No(valor); // com o valor e prox = null
	aux->prox = p; // o ultimo no sempre aponta para a sentinela
	
	// atacha no p final da lista existente
	// mas e se a lista for vazia?
	if (empty())
		p->prox = aux;
	else tail->prox = aux;
	// atualiza a nova cauda
	tail = aux;
	qtd++;

	return true;
}

/*
Pre-cond: A lista existe e nao é ordenada
Pos-cond: insere o item na posicao pos da lista, 
se por for um indice válido e retorna true.
pos 
pos válida: pos >=0 e pos <= fim !!!!
CAso contrario, retorna false.
*/
bool Lista::inserePos(item valor, int pos){
	if (pos<0 || pos > qtd || sorted)
		return false;

	if (pos == 0)
		return insereInicio(valor);
	if (pos == qtd)
		return insereFim(valor);

	// p aponta para o no anterior ao do indice pos
	No *p = head->prox;
	int cont = 1;
	while (cont < pos){
		cont++;
		p = p->prox;
	}

	// o valor sera inserido entre pant e p
	No *no = new No(valor);
	no->prox = p->prox;
	p->prox = no;
	qtd++;
	return true;	
}
```

Existe o conceito do nó sentinela. É um nó especial que não armazena dados "reais" da lista. Ele serve para simplificar as operações de inserção e remoção, evitando tratar casos especiais (como lista vazia ou inserir no início).

- Perceba que no construtor, o nó sentinela, `head` aponta para si próprio, pois estamos lidando com uma lista vazia.

- O último nó da lista `tail` aponta para o sentinela, o `head` .

Em vários casos, definimos o valor do nó sentinela como `-1000` . Esse é o identificador do nó sentinela. Somente este nó terá esse valor, então podemos afirmar que percorremos toda a lista ao chegarmos nele.

Detalhes importantes sobre a lista vazia:

- `head` aponta para si próprio.

- `tail` aponta para `nullptr` .

Um caso especial que foi tratado é quando removemos um elemento de uma lista com um único elemento. Neste caso, `tail` aponta para `nullptr` e `head` volta a apontar para si próprio.

_**Implementação das demais funções**_

```C++

/*
Pre-cond: A lista existe e NAO é vazia...
Pos-cond: busca o valor na lista (ordenada ou não)
Se o elemento for encontrado, retorna true.
Caso contrário, retorna false.
Usaremos o nó sentinela para armazenar a chave (valor) e
poder para a busca. Obviamente, neste caso, a lista NAO terá 
valores repetidos.
ant: retorna um ponteiro para o nó anterior ao no
encontrado (Se valor nao encontrado, ant aponta para a 
cauda da lista)
pos: retorna a posicao ('indice') do elemento, quando
existir. Se nao existir, o valor é indefinido.
*/

bool Lista::busca(item valor, No **ant, int *pos){
	if (empty()){
		return false;
	}

	head->set(valor);// armazena valor no sentinela !
	*ant = head;
	*pos = 0; // indice do primeiro elemento
	No *p = head->prox; // p eh o primeiro no valido

	if (!sorted){
		while(valor != p->get()){
			*ant = p;
			(*pos)++;
			p = p->prox;
		}
	} else {
		while(valor > p->get()){
			*ant = p;
			(*pos)++;
			p = p->prox;
		}
	}

	if (p->get() == valor && p != head)
		return true;
	return false;

}

/*
VERSAO QUE NAO USA BUSCA
Pre-cond: a lista existe.
Pos-cond: insere o valor tal que a lista eh
mantida ordenada
retorna falso se nao houver memoria para insercao OU
se o elemento já se encontra na lista.
Como o no sentinela conterá a chave a ser inserida, entao este 
tipo de lista NAO ACEITA ELEMENTOS Repetidos
*/
bool Lista::insereOrdenado2(item valor){
	No *no = new No(valor);
	if (no == nullptr)
		return false;

	No *p = head; // no cabeca...
	// p aponta para o no ANTERIOR ao no a ser inserido !
	while (p->prox != head && valor >= p->prox->data){
		if (valor == p->prox->data)
			return false;
		p = p->prox;
	}

	// se o valor a ser inserido é o ultimo, atualiza tail
	if (p->prox == head)
		tail = no;

	no->prox = p->prox;
	p->prox = no;

	qtd++;
	return true;
}

/*
VERSAO COM BUSCA
Pre-cond: a lista existe.
Pos-cond: insere o valor tal que a lista eh
mantida ordenada
retorna falso se nao houver memoria para insercao OU
se o elemento já se encontra na lista.
Como o no sentinela conterá a chave a ser inserida, entao este 
tipo de lista NAO ACEITA ELEMENTOS Repetidos
*/
bool Lista::insereOrdenado(item valor){
	No *p;
	int pos;

	if (empty()){ // se alista for vazia, insere no inicio.
		sorted = false;
		insereInicio(valor);
		sorted = true;
		return true;
	}

	if (busca(valor, &p, &pos)){ // valor já existe, tchau
		return false;
	}

	No *no = new No(valor);
	if (no == nullptr)
		return false;
	
	// se o valor a ser inserido é o ultimo, atualiza tail
	if (p->prox == head)
		tail = no;

	no->prox = p->prox;
	p->prox = no;

	qtd++;
	return true;
}


/*
Pre-cond: a lista existe.
Pos-cond: remove o valor tal que a lista eh
mantida ordenada 
retorna falso se o valor nao for encontrado
*/

bool Lista::retiraOrdenado(item valor){
	if (empty())
		return false;

	No *p;
	int pos;
	if (!busca(valor, &p, &pos)){ // valor nao existe, tchau
		return false;
	}

	retiraPos(&valor, pos);
	return true;
}

/*
Pre-cond: a lista existe
Pos-cond: retira o elemento valor na lista.
Se for NAo ordenada, insere no FIM.. 
retorna true, se sucesso
falso, caso contrario
*/
bool Lista::retira(item *valor){;;
	// se for ordenada, insereOrd
	if (sorted)
		return retiraOrdenado(*valor);
	
	return retiraFim(valor);

}


/*
Pre-cond: a lista existe
Pos-cond: insere o elemento valor na lista.
Se for NAo ordenada, insere no FIM.. 
retorna true, se sucesso
falso, caso contrario
*/
bool Lista::insere(item valor){
	//if (full())
	//	return false;

	// se for ordenada, insereOrd
	if (sorted)
		return insereOrdenado(valor);
	
	return insereFim(valor);
	//return true;
}
```