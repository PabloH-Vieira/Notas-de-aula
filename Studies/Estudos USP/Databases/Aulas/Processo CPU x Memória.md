---
Course:
  - "[[Organização e Arq. de Computadores]]"
Last Edited: 2025-08-23T00:29
---
![[Pasted image 20260313152850.png]]

Os ciclos de instruções são divididos em duas etapas: o ciclo de busca e o ciclo de execução.

## Ciclo de Busca

O PC, um contador presente na CPU, contém o endereço de todas as instruções a serem realizadas. Ao final do ciclo pré-determinado, ele incrementa e informa o endereço da próxima instrução.
O MAR é um componente intermediário. Ele recebe o endereço da instrução atual do PC e guarda esse valor até o final do ciclo de busca.
O passo a seguir é o de acessar a memória através de um barramento, ir até o endereço fornecido e então voltar para o CPU.
O componente do CPU que recebe os dados da instrução é o MBR (*memory buffer register*). Em seguida, a instrução lida é armazenada no IR (*instruction register*). Depois disso, o ciclo de busca terá encerrado e o PC já pode atualizar, informando o endereço da próxima instrução.
Com isso, a instrução armazenada no IR é levada à Unidade de Controle para dar início ao ciclo de execução.

## Ciclo de Execução

 A unidade de controle é o componente responsável por decodificar a instrução recebida pelo IR e iniciar as operações descritas na instrução.
 ![[Pasted image 20260313154425.png]]
