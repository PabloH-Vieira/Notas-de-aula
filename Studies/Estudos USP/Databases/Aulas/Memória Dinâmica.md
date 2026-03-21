---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-1b9fa7f60cd880c9a478ea23cbd908a4?pvs=21
Last Edited: 2025-08-09T11:51
---
A memória dinâmica dá a possibilidade de armazenar dados na memória _run time_, também conhecida como _heap_, a qual pode reservar um bloco de memória alterável.

- É acessada por meio de um ponteiro.

É excelente para otimizar o desempenho de um código, pois pode ser trabalhada para utilizar apenas os recursos estritamente necessários, sem contar a vantagem de poder adaptar-se à mudanças nas variáveis.

Existem quatros funções básicas para trabalhar na memória dinâmica:

### Malloc

Aceita apenas um parâmetro, o tamanho do bloco de memória. Aconselha-se utilizar a função _sizeof(tipo_da_var)_ para reservar uma quantidade de bytes apropriada para o tipo da variável (um ponteiro). Ela inicializa esse espaço da memória com valores imprevisíveis.

- Pode-se reservar um array de n elementos declarando o ponteiro como  
    `var = malloc (n*sizeof(var));`

### Calloc

Semelhante ao malloc, com a diferença que inicializa a memória com todos os espaços definidos como `0` . Aceita dois parâmetros: quantidade de elementos e tamanho.

### Realloc

Usada para modificar o tamanho de um bloco de memória. Aceita dois parâmetros: o nome do ponteiro e o novo tamanho.

Existem dois cenários importantes para se levar em conta:

- Quando houver expansão de memória e houver espaço na memória “vizinha” o bloco simplesmente aumenta de tamanho, sem alterar o endereço do ponteiro e o seu conteúdo.

- Quando não houver espaço nas memórias “vizinhas”, a função vai percorrer toda a memória RAM e buscar por um espaço que caiba o bloco. Encontrando, ela vai copiar todo o bloco do endereço anterior para o novo e liberar o endereço antigo.

Caso não encontre espaço, o ponteiro vai retornar NULL, sem alterar o conteúdo do endereço anterior.

### Free

Importante passo, pois se não houver a liberação da memória, a alocação de diversas variáveis pode acabar por preencher todo o espaço e ocasionar uma _memory leak_, ou vazamento de memória.

Caso você tente utilizar um ponteiro que tenha sido liberado, teremos um caso de _dangling pointer_, no qual o programa tentará acessar um espaço de memória mas não conseguirá, ocasionando em comportamentos inesperados, como sobrescrever o conteúdo daquele espaço (que pode estar sendo utilizado por outro ponteiro), ou receber lixo.