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


Uma palavra diz respeito à quantidade de bytes utilizados para representar um inteiro. Esse valor vai depender da arquitetura, mas por padrão assumimos o valor quatro.

## A função `align`

A função `align` é muito utilizada em VHDL e assume um papel importantíssimo na alocação de espaço na memória. Ela indica a posição que uma informação vai ocupar na memória. Isso está diretamente relacionado ao tamanho (e consequentemente o tipo) da informação, pois o parâmetro dessa função é o expoente de 2, e diz que a posição a ser ocupada será um múltiplo daquele número.
- `align 2` serve para int's, pois 2² = 4 bytes. O índice do espaço ocupado na memória será um múltiplo de 4.
- `align 0` serve para strings, pois 2$^0$ = 1 byte. A informação pode ser armazenada em qualquer posição da memória.

É necessário utilizar um `align` para a sessão de texto/código pois existem dois conjuntos de instruções: RV321 (instruções de 32 bits) e RV32C (instruções compactas, de 16 bits). Por esse motivo, logo após o montador `.text` tem-se um `align 2`, definindo o tamanho de uma palavra para memórias de 32 bits.

Para adicionar um elemento na memória precisamos carregá-lo em um registrador. Para tal, buscamos um registrador que tenha a função de armazenar inteiros.
~~~ armasm
addi a7, zero, 5
ecall

add s0, a0, zero
~~~

O registrador `a7` executa uma função do tipo I/O a depender do parâmetro que ele recebe. O valor 5 (a soma entre 5 e 0 - o zero do registrador) faz uma leitura de um inteiro. O `ecall` é essencial para garantir a leitura.
A linha 4 adiciona o valor lido - que é adicionado por padrão ao registrador `a0` - ao registrador `s0`.


### A função `addi` e os tipos de instruções

As funções `addi` e `add` tem funcionalidade parecida, mas cada uma tem sua particularidade. Ambas guardam o resultado de uma soma em um registrador.
- A primeira passa como parâmetro um valor especificado, por exemplo `addi a7, zero, 5`
- A segunda passa o registrador que guarda um valor, por exemplo, `add a7, zero, t0`

`addi` é uma instrução do tipo I. Ela ocupa 32 bits, divididos da seguinte forma:
![[Pasted image 20260321132947.png]]
- opcode: uma informação importante para acessar o endereço do registrador de destino
- funct3: uma extensão do opcode
- rs1: endereço do registrador de origem
- rd: endereço do registrador de destino
- imm[11:0] - valor imediato 12 bits

Percebe-se que restam apenas 12 bits para a informação, sendo que estamos trabalhando com inteiros (32 bits). Assim, utilizamos uma instrução do tipo U para complementar os bits faltantes.
![[Pasted image 20260321133556.png]]
Essa instrução guarda os 20 bits mais significativos, enquanto o tipo I, os 12 menos significativos.
Então, utiliza-se duas instruções para armazenar um valor no registrador. No entanto, a pseudo-instrução `la` (load address) já faz isso, facilitando o processo.
- A pseudo-instrução load immediate (`la`) tem a mesma funcionalidade que o `addi`, com a única diferença de que não precisa do parâmetro do registrador `zero`.

## Instruções de load e store

Há instruções de load e store, tanto para bytes quanto para palavras:
- load byte (`lb`) - carrega um byte da memória em um registrador
- load word (`lw`) - carrega uma palavra da memória em um registrador
- formato : `lb <reg>, offset(<reg_base>) => <reg> = mem(reg_base + offset)`
- exemplo: `lb t0, 0(s0) => t0 = mem(s0 + 0)`

- store byte (`sb`) - armazena um byte de um registrador na memória
- store word (`sw`) - armazena uma palavra de um registrador na memória
- formato `sw <reg>, offset(<reg_base>) => mem(reg_base + offset) = <reg>`
- exemplo: `sw ra, 4(sp) = mem (sp+4) = ra`

Observações:
- O offset é um valor que, somado ao endereço armazenado no registrador base, vai dar o endereço no qual ocorrerá a operação (o endereço do registrador destino).
	- seja a0 um registrador cuja posição na memória é 16. Assim, `lw 12, 0(a0)` vai carregar o valor 12 no endereço 0+16. Isto é, carregará no próprio a0.
- `sp` é space memory.

