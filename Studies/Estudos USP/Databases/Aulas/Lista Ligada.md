---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-09-30T23:24
---
A lista ligada não utiliza a ideia de vetor. Ao invés disso, usa um ponteiro que aponta para o elemento seguinte na lista. Também é dinamicamente alocada.

Além disso, a lista em si possui um ponteiro para o início (_head_) e para o final (_tail_). Outro detalhe é que ela pode ser ordenada ou não.

**Header**

```C++
/*
Adotaremos a implementação com um nó sentinela. Isso significa
que a lista tem um nó especial que contem as seguintes in
formaçoes: um ponteiro para o primeiro nó, um ponteiro
para o último nó (isso faz da inserçao no fim ter complexidade 
constante, igual a 1), além de um contador para a quantidade
de elemtos na lista

\#ifndef LISTA
\#define LISTA

// na lista podemos armazenar qq coisa.
// para fins didáticos, usaremos uma lista de inteiros.
/*typedef struct item {
	int NroUSP;
	string nome;
	int curso;
	//..... etc....
}item;*/

typedef int item;

typedef struct No{
	item data;
	struct No *prox;
}No;

typedef struct Lista{
	No *head;    // ponteiro para o inicio da fila
	No *tail;    // ponteiro para o fim da fila.
	int qtd;     // quantidade de 
	bool sorted; // sorted = true (ordenada)


	Lista(bool ordenada);    // construtor
	~Lista();                // destrutor

	// operações básicas para ambos tipo (ord ou nao ord)
	int size();
	bool empty();
	void printLista();
	bool retiraFim(item *valor);
	bool retiraInicio(item *valor);
	//No *getPos(int pos, item *valor, No **ant);
	bool retiraPos(item *valor, int pos);
	bool busca(item *valor);
	bool insere(item valor);  
	bool retira(item *valor);

	// para a lista não ordenada
	bool insereFim(item valor);
	bool insereInicio(item valor);
	bool inserePos(item valor, int pos);

	// para listas ordenadas
	bool insereOrdenado(item valor);
	bool retiraOrdenado(item valor);
	

}Lista;

\#endif
```

**Implementação**

```C++
\#include <cstdio>
\#include "listaSimpEncadeada.hpp"

using namespace std;

/*
Pre-cond: nenhuma
Pos-cond: cria uma lista (um nó especial) e inicia
os atributos head = tail = nullptr
qtd = 0
e com o tipo da lista ordenada ou nao (true ou false)
*/
Lista::Lista(bool ord){
	head = nullptr;
	tail = nullptr;
	qtd = 0;
	sorted = ord;
}

/*
Pre-cond: A lista existe
Pos-cond: libera todos os nós da lista
DESAFIO: implemente uma versão recursiva !!!!
*/
Lista::~Lista(){
	No *aux = head;
	while(aux != nullptr){
		No *p = aux;
		aux = aux->prox;
		delete p;
	}
}

int Lista::size(){
	return qtd;
}

bool Lista::empty(){
	return  qtd == 0 ? true : false;
	//return (head == nullptr) ? true : false;
}

void Lista::printLista(){
	No *p = head;
	while (p != nullptr){
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

	// se a lista tem somente um elemento
	if (head->prox == nullptr){
		delete tail;   // ou delete head;
		head = nullptr;
		tail == nullptr;
		qtd--;
		return true;
	}

	// A lista tem multiplos elementos. Busca penultimo
	No *p = head;
	while(p->prox != tail)	p = p->prox;

	delete tail;
	tail = p;
	tail->prox = nullptr;
	qtd--;
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

	*valor = head->data;

	// se a lista tem somente um elemento
	if (head->prox == nullptr){
		delete head;  // ou delete tail !!
		head = nullptr;
		tail == nullptr;
		qtd--;
		return true;
	}

	No *p = head->prox; // p aponta para o segundo elemento
	delete head;
	head = p;
	qtd--;
	return true;
}

/*
Pre-cond: A lista existe
Pos-cond: retira o item da posicao pos da lista, e guarda
em valor e retorna true (se a lista nao for vazia e pos for valido)
e retorna true.
pos valida:  0 <= pos < qtd
pos == 0 , indica o primeiro nó da lista e
assim sucessivamente.
CAso esteja vazia, retorna false.
*/
bool Lista::retiraPos(item *valor, int pos){
	if (empty() || pos < 0 || pos >=qtd)
		return false;

	if (pos == 0)
		return retiraInicio(valor);
	if (pos == qtd-1)
		return retiraFim(valor);


	// p aponta para o no anterior ao do indice pos
	No *p = head;
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

	// cria um no
	No *p = new No;
	// atualiza no
	p->data = valor;
	p->prox = head;
	// se a lista for vazia
	if (empty()){
		//head = p;
		tail = p;
	} 
	head = p;
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

	// cria um no
	No *p = new No;
	// atualiza no
	p->data = valor;
	p->prox = nullptr;
	// atacha no p final da lista existente
	// mas e se a lista for fazia?
	if (empty())
		head = p;
	else tail->prox = p;
	// atualiza a nova cauda
	tail = p;
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
	No *p = head;
	int cont = 1;
	while (cont < pos){
		cont++;
		p = p->prox;
	}

	// o valor sera inserido apos o no p
	No *no = new No;
	no->data = valor;
	no->prox = p->prox;
	p->prox = no;
	qtd++;
	return true;	
}

/*
Pre-cond: a lista existe.
Pos-cond: insere o valor tal que a lista eh
mantida ordenada 
retorna falso se nao houver memoria para insercao
*/
bool Lista::insereOrdenado(item valor){
	No *no = new No;
	if (no == nullptr)
		return false;
	no->data = valor;
	// se vazia OU se valor menor que primeiro
	if (empty() || (valor <= head->data)){
		no->prox = head;
		head = no;
		tail = no;
		qtd++;
		return true;
	} 

	// p aponta para o no ANTERIOR ao no a ser inserido !
	No *p = head;
	while (p->prox != nullptr && valor > p->prox->data){
		p = p->prox;
	}

	// liga o  proximo de no ao proximo de p
	no->prox = p->prox;

	// liga p ao proximo de no
	p->prox = no;
	// se for o ultimo no da lista, tem que atualizar tail
	if (p == tail)
		tail = no;
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
	// se valor eh o primeiro elemento (caso especial)
	if (valor == head->data){
		No *aux = head;
		head = head->prox;
		delete aux;
		qtd--;
		return true;
	}

	// busca o elemento no restante lista
	// p é o no ANTERIOR ao no que contem valor
	No *p = head;
	bool achou = false;
	while (p->prox != nullptr && valor >= p->prox->data){
		if (p->prox->data == valor){
			achou = true;
			break;
		}
		p = p->prox;
	}
	if (!achou)
		return false;

	No *aux = p->prox;
	p->prox = aux->prox;
	// se for o ultimo no da lista, tem que atualizar tail
	if (aux == tail)
		tail = p;
	
	delete aux;

	qtd--;
	return true;
}

/*
Pre-cond: a lista existe
Pos-cond: insere o elemento valor na lista.
Se for NAo ordenada, insere no FIM.. 
retorna true, se sucesso
falso, caso contrario
*/
bool Lista::retira(item *valor){

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

Perceba que essa implementação têm de lidar com uma série de casos especiais.