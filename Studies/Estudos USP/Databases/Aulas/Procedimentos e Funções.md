---
Course:
Last Edited:
---
A função `jal` (jump  and link)é fundamental, ela faz um desvio incondicional. Sua sintaxe é `jal <reg>, label`, onde `label` é o trecho para onde ocorrerá o desvio e `<reg>` é onde estará o endereço da próxima função depois de `jal`.
- Essa função tem como princípio fazer um desvio, mas também guardar a informação de onde veio o desvio. Essa é a base para o funcionamento de uma função: chamá-la em um trecho específico do código.
- A função funciona sem o registrador, com o compilador interpretando que basta seguir o código.

Existem variações de instruções e pseudo-instruções do `jump`.
- `j fatorial` é um desvio incondicional, mas que -- diferentemente do `jal` -- não guarda de onde veio o desvio.

~~~
#fatorial com função
	
	.data
	.align 0
	str_oi: .asciz "Digite um número maior ou igual a 0: "
	str_res1: .asciz "O fatorial de "
	str_res2: .asciz " é "
	str_erro: .asciz "Entrada inválida!"
	
	.text
	.align 2
	.globl main

main:
	#imprimir str_oi
	addi a7, zero, 4
	la a0, str_oi
	ecall
	
	#ler um número inteiro
	addi a7, zero, 5
	ecall
	beq a0, continua
	

~~~

É importante definir os registradores que servirão como parâmetro e retorno ao declarar uma função. Pela convenção:
- Parâmetros: a0 a a7
- Retorno: a0 e a1