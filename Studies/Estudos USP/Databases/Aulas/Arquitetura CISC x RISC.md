---
Course:
  - "[[Organização e Arq. de Computadores]]"
Last Edited: 2025-08-23T00:29
---
## CISC - Complex Instruction Set Computer

A arquitetura CISC é conhecida por resumir instruções complexas em poucas linhas. Ela permite acessar a memória a partir de qualquer instrução, o que diminui a quantidade de etapas entre o CPU e a memória, mas que também pode diminuir o desempenho.
- Instruções complexas que demandam um número grande de ciclos para serem executadas 
- Dezenas de modos de endereçamento
- Instruções de tamanhos variados
- Referência a operandos na memória principal

Alguns problemas resultantes dessa complexidade são:
- Nas arquiteturas CISC fica mais difícil implementar o pipeline (quando a instrução é dividida em etapas, de forma que etapas de múltiplas etapas podem ser realizadas paralelamente).
- A taxa média de execução das instruções por ciclo tende a ser bem menor do que 1 IPC (*instruction per cycle*).
- A unidade de controle é microprogramada.
- Instrução complexa significa um maior tempo para decodificar e executar, muitas das quais são raramente usadas.

## RISC - Reduced Instruction Set Computer

O RISC é uma arquitetura muito mais simplificada, na qual a memória só pode ser acessada a partir das instruções `load` e `store`.
- Instruções mais simples, demandando um número fixo de ciclos de máquinas para sua execução
- Uso de poucos e simples modos de endereçamento
- Poucos formatos das instruções
- Apenas instruções de load/store referenciam operandos na memória principal
- Cada fase de processamento da instrução tem a duração fixa igual a um ciclo de máquina

Em resumo, principais características da RISC são:
- Implementadas com o uso do pipeline
	- Formato fixo das instruções facilita o pipeline
	- As instruções são divididas em etapas, permitindo o paralelismo de instruções.
- As instruções são executadas na sua maioria em apenas um ciclo de máquina
- A unidade de controle é em geral hardwired
	- Não há microprograma para interpretar as instruções
- Arquitetura orientada a registrador
	- Todas as operações aritméticas são realizadas entre registradores
	- Define-se um grande conjunto de registradores

## RISC-V

A RISC-V é a arquitetura mais utilizada até os dias de hoje na maioria das máquinas. 
Possui vários requisitos:
- Atender todos os tamanhos de processadores 
- Funcionar bem em uma grande variedade de software e ling. de programação
- Acomodar tecnologias de implementação
- Ser eficiente para todo tipo de microarquitetura (organização)
- Ser estável (ISA base não deve mudar)

A RISC usa como base de operação registradores. Versões mais recentes dessa arquitetura contam com 64 bits, mas essa matéria estudará a versão de 32 bits. Essa versão conta com:
- 32 registradores de propósito geral.
- 32 registradores de ponto flutuante.

São eles
![[Pasted image 20260313160620.png]]

Existem variações da RISC-V para atender a situações específicas, como a necessidade de instruções em formato vetorial.
![[Pasted image 20260313224618.png]]

Como dito anteriormente, a RISC possui duas instruções fundamentais: `load` e `store`. Elas são as instruções responsáveis por acessar e manipular a memória, pois todos os valores devem ser carregados nos registradores antes das operações.
Para programar em RISC-V é necessário manipular a linguagem de baixo nível Assembly.