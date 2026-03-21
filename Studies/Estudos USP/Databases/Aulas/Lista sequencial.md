---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-09-30T23:04
---
A implementação da lista a seguir segue a lógica de uma pilha, mas permite métodos adicionais, tal como remover e inserir em uma posição específica e fazer buscas.

## Linear

**Header**

```C++
\#ifndef LISTA
\#define LISTA

// na lista podemos armazenar qq coisa.
// para fins didáticos, usaremos uma lista de inteiros.

typedef int item;

typedef struct Lista{
	item *itens;
	int fim;  // equivale à qtd de elementos na lista
	//int qtd; // não haveria problema em criar um campo qtd, mesmo que seja redundante
	int MAX;


	Lista(int n);
	~Lista();

	bool insereFim(item valor);
	bool retiraFim(item *valor);
	bool inserePos(item valor, int pos);
	bool retiraPos(item *valor, int pos);
	bool buscaPos(int pos, item *valor);
	//bool buscaValor(item valor, int *pos);
	int size();
	bool empty();
	bool full();
	void printLista();
}Lista;

\#endif
```

**Implementação**

```C++
\#include <cstdio>
\#include "listaSeqLin.hpp"

using namespace std;

/*
Pre-cond: nenhuma
Pos-cond: cria uma lista sequencial de tamanho
n, com zero elementos e de capacidade MAX
*/
Lista::Lista(int n){
	itens = new item[n];
	fim = 0;  // lista nao tem elementos
	MAX = n; // maximo de elem possiveis
}


Lista::~Lista(){
	delete[] itens;
}


/*
Pre-cond: A lista existe
Pos-cond: insere o item no FIM da lista, se houve espaco
e retorna true.
CAso esteja cheia, retorna false.
*/
bool Lista::insereFim(item valor){
	if (full())
		return false;

	itens[fim] = valor;
	fim++;

	return true;
}

/*
Pre-cond: A lista existe
Pos-cond: retira o item no FIM da lista, e guarda
em valor e retorna true (se a lista nao for vazia)
e retorna true.
CAso esteja vazia, retorna false.
*/
bool Lista::retiraFim(item *valor){
	if (empty())
		return false;

	fim--;
	*valor = itens[fim];
	

	return true;
}

/*
Pre-cond: A lista existe
Pos-cond: insere o item na posicao pos da lista, se houve espaco
e se por for um indice válido e retorna true.
pos válida: pos >=0 e pos <= fim !!!!
CAso contrario, retorna false.
*/
bool Lista::inserePos(item valor, int pos){
	if (full() || pos<0 || pos > fim)
		return false;

	// desloca todo mundo para 'direita': de fim-1 ate pos uma casa para frente
	for (int i = fim-1; i >= pos; i--)
		itens[i+1] = itens[i];

	itens[pos] = valor;
	fim++;

	return true;
}

/*
Pre-cond: A lista existe
Pos-cond: retira o item da posicao pos da lista, e guarda
em valor e retorna true (se a lista nao for vazia e pos for valido)
e retorna true.
pos valida:  0 <= pos < fim
CAso esteja vazia, retorna false.
*/
bool Lista::retiraPos(item *valor, int pos){
	if (empty() || pos < 0 || pos >=fim)
		return false;
	*valor = itens[pos];
	// desloca todo para 'esquerda': de pos+1 até fim-1 
	for (int i = pos+1; i < fim; ++i)
		itens[i-1] = itens[i];
	fim--;
	
	return true;
}

int Lista::size(){
	return fim;
}

bool Lista::full(){
	return fim == MAX ? true : false;  
}

bool Lista::empty(){
	return fim == 0 ? true : false;  
}

/*
Pre-cond: a lista existe
Pos-cond: retorna em valor o item na posicao pos.
Se a pos for invalida, retorna false.
Caso contrario, retorna true
*/
bool Lista::buscaPos(int pos, item *valor){
	if (pos < 0 || pos >=fim)
		return false;

	*valor = itens[pos];
	return true;
}

void Lista::printLista(){
	for (int i = 0; i < fim; ++i)		
		printf("%d ", itens[i]);
	printf("\n");
}

```

Um detalhe importante dessa implementação está nos ponteiros. Só é possível guardar os elementos dentro do vetor em um ponteiro.