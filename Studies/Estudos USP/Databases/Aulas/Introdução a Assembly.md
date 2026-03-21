---
Course:
  - "[[Organização e Arq. de Computadores]]"
Last Edited: 2025-08-23T00:29
---
Um programa em Assembly é dividido em partes:

- Estrutura do código
	- Rótulos e Diretivas
	- Chamada ao sistema para fazer E/S - ecall
- Instruções básicas
- Ferramenta de simulação da arquitetura
	- RARS (RISC-V Assembler and Runtime Simulator)

A memória interpreta o código de duas maneiras:

- Segmento de texto (código) – endereço `0x00010000` 
- Segmento de dados – endereço `0x10000000`
- `.data` 
	- diretiva que indica o início do segmento de dados
	- variáveis estáticas 
- `.text`
	- diretiva que indica o início do segmento de texto
	- código fonte

### Rótulos
Rótulos são indicadores para sessões do programa. Eles são úteis em casos de desvios condicionais (estruturas condicionais e loops), desvios incondicionais e chamadas de procedimentos.
Eles são identificados pelos dois pontos logo após a sua declaração.

![[Pasted image 20260313225608.png]]

Exemplos:
![[Pasted image 20260313225720.png]]

### Diretivas do Montador

São linhas que determinam configurações do código. 
São identificadas pelo ponto que precede sua declaração.

![[Pasted image 20260313225828.png|559]]

Exemplos:
![[Pasted image 20260313225923.png]]

### Comandos de chamada ao sistema (*ecall*)
![[Pasted image 20260313230042.png]]

#### Exemplo de programa: `hello world!`
![[Pasted image 20260313230140.png]]