---
Course:
  - https://www.notion.so/Algoritmos-e-Estruturas-de-Dados-256fa7f60cd880998a2ed44465b8be27?pvs=21
Last Edited: 2025-09-29T23:01
---
Pilhas são estruturas de dados que seguem uma lógica de _last in, first out_. Isso quer dizer que removemos ou inserimos elementos sempre a partir do último elemento.

Podemos implementar essa estrutura em memória estática ou dinâmica (maior desempenho).

### Pilha Estática

**Código do header (implementação em C++)**

```C++
//HEADER
\#ifndef STACK2
\#define STACK2

typedef  struct StackInt{
	int *itens;
	int topo;
	int tam;

	// construtor
	StackInt(int n = 100);
	StackInt(StackInt &);
	// destrutor
	~StackInt();
	
	// funcoes utilitárias
	No *push(int valor);
	int pop();
	int top();

	bool empty();
	bool full ();
}StackInt;

\#endif
```

  

**Implementação:**

```C++
//Construtor
StackInt::StackInt(int n){
	printf("Criando uma pilha...\n");
	itens = new int[n];
	tam = n;
	topo = 0;
}

StackInt::StackInt(StackInt &p){
	printf("Criando uma pilha a partir de outra\n");
	itens = new int[p.tam];
	tam = p.tam;
	topo = p.topo;
	for (int i = 0; i < tam; ++i)
		itens[i] = p.itens[i];
}

//Destrutor
StackInt::~StackInt(){
	printf("Desalocando a pilha..\n");
	delete[] itens;
}

void StackInt::push(int valor){
	itens[topo++] = valor;
}

int StackInt::pop(){
	topo--;
	return itens[topo];
}

int StackInt::top(){
	return itens[topo];
}

bool StackInt::empty(){
	return topo == 0 ? true : false;
}

bool StackInt::full(){
	return topo == tam ? true : false;
}
```

### Pilha Dinâmica

**Header**

```C++
//Nota: topo aponta para a PRIMEIRA posicao LIVRE da pilha....

\#ifndef STACK2
\#define STACK2

typedef struct No{
	int item;
	struct No *prox;
}No;

typedef  struct StackInt{
	No *topo;
	int tam;
	
	// construtor
	StackInt(int n = 100);
	StackInt(StackInt &);
	// destrutor
	~StackInt();

	// funcoes utilitárias
	No *push(int valor);
	int pop();
	int top();
	int size();
	bool empty();
	bool full ();
}StackInt;

\#endif
```

  

```C++
\#include <cstdio>
\#include "stackIntDin.hpp"

StackInt::StackInt(int n){
	printf("Criando uma pilha...\n");
	topo = nullptr;
	tam = 0;
}


StackInt::StackInt(StackInt &p){
	printf("Criando uma pilha a partir de outra\n");
	if (p.topo == nullptr){
		topo = nullptr;
		tam = 0;
		return;
	}
	tam = p.tam;

	topo = new No;
	topo->item = p.topo->item;
	topo->prox = nullptr;
	
	No *no = p.topo->prox; // no comeca no segundo elemento

	// no aponta para o topo de p.
	// Enquanto houver nos, faz um push na nova pilha
	No *aux = topo;
	while (no != nullptr){
		aux->prox = new No;
		aux = aux->prox;
		aux->item = no->item;
		aux->prox = nullptr;
		
		no = no->prox; // para para o prox no
	}
}

//Destrutor
StackInt::~StackInt(){
	printf("Desalocando a pilha..\n");
	while(!empty())
		pop();
	tam = 0;
}

No *StackInt::push(int valor){
	No *no = new No;
	if (!no) return nullptr;
	no->item = valor;
	no->prox = topo;
	topo = no;
	tam++;
	return no;

}

int StackInt::pop(){
	int valor = topo->item;
	No *aux = topo->prox;
	delete topo;
	topo = aux;
	tam--;

	return valor;
}

int StackInt::size(){
	return tam;
}

int StackInt::top(){
	return topo->item;
}

bool StackInt::empty(){
	return topo == nullptr ? true : false;
}

```

  

### Casos especiais

Em alguns casos, é necessário tratar condições especiais para tornar o código mais robusto.

- Quando a lista só tiver um elemento e realizarmos o `pop` . Nesse caso, é importante que o topo aponte para `nullptr` novamente. Por isso, o primeiro nó aponta para onde o topo aponta primeiramente. Assim, quando realizamos o `pop`, o topo deve apontar para `no -> prox`

- Em consonância com o último caso, esta é uma das condições para que ela funcione: o primeiro nó em uma pilha vazia. Para funcionar adequadamente, precisamos garantir que esse nó aponte para `nullptr` .