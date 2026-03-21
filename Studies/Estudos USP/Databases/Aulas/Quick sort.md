---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-II-24efa7f60cd880bbbbcaf479fda73ab6?pvs=21
Last Edited: 2025-11-15T01:03
---
O quick sort é considerado um algoritmo de ordenação mais eficiente.

Ele funciona com base em um pivô, que a cada loop divide a lista em duas partes: um lado menor que o pivô e outro maior.

- Para realizar essa divisão, usamos ponteiros para percorrer a lista.

- A primeira etapa é a definição do pivô, que recomenda-se ser o último elemento da lista.

- Inicializamos os ponteiros _i_ e _j._ O ponteiro _j_ aponta para o primeiro elemento, o índice _0,_ e _i_ aponta para o nada.

- O passo seguinte é percorrer a lista comparando o valor atual com o pivô: se o elemento for menor que o pivô incrementamos _i_ e trocamos os valores entre os ponteiros.

- Se o elemento for maior, não ocorre nada, simplesmente incrementamos _j_.

- O primeiro loop termina quando _j_ chega no pivô. Nesse passo, incrementamos _i_ uma última vez e trocamos pelo _j_. Esse é o passo onde posicionamos o pivô no seu lugar certo.

![[image 113.png|image 113.png]]

- No exemplo, o 5 era o pivô, e observa-se que após o primeiro loop podemos dividir a lista entre os valores menores e os maiores que o pivô.

- Podemos concluir que o valor do nosso primeiro ponteiro é exatamente depois de _i._

- O passo seguinte é fazer um quick sort para cada parte da lista. Isso ocorre por recursão.

![[image 1 87.png|image 1 87.png]]

- O formato assemelha-se a uma árvore binária. A cada execução encontramos a posição do pivô.

- No exemplo, ao executar pela segunda vez também encontramos a posição de _i._

![[image 2 70.png|image 2 70.png]]

- Na implementação, usamos os ponteiros _left_ e _right_ como ponteiros de início e final da lista (inclusive as particionadas).

- A função _partition_ é responsável por encontrar a posição correta do pivô.
    
    - primeiro definimos o pivô como sendo o último elemento da lista.
    
    - no loop, comparamos cada elemento com o pivô. Se maior, incrementamos _i_ e trocamos a posição entre _i_ e _j._ Se menor, simplesmente incrementamos j.
    
    - ao final, trocamos a posição seguinte de _i_ pelo pivô, sendo esta a sua posição correta.
    
    - retornamos a posição correta de _i._
    

- A função _quicksort_ é recursiva. O caso base é quando _left = right_, que é quando só existe um elemento na lista.
    
    - a cada execução, chamamos um _quicksort_ para a esquerda e para a direita. A posição dos ponteiros _left_ e _right_ será:
        
        - para o primeiro caso: right _= pi-1_ (uma posição antes do pivô).
        
        - para o segundo caso: _left = pi+1_ (uma posição após o pivô).
        
        - _pi_ é a posição de _pi_.