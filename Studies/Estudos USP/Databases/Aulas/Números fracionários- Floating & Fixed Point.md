---
Course:
  - https://www.notion.so/L-gica-Digital-1c1fa7f60cd88012b3fee27ba8aaeae7?pvs=21
Last Edited: 2025-08-09T11:53
---
## Representação de Números Fracionários em Binários

Convertemos separadamente a parte inteira e a fracionária do número.

- A parte inteira consiste em dividir o número por 2 e, a cada divisão, escrever o resto como o dígito binário, até chegar em 1 ou 0. Lembrando que a ordem é inversa, ou seja, o último resto é o bit mais significativo.
    
    - 10 (0) → 5(1) → 2(0) → 1(1) = 1010.
    

- A parte fracionária é multiplicada por 2.
    
    - 0,5 * 2 = 1.
    

- 10,5 = 0101,1

  

Quando a parte fracionária não resulta exatamente em 1, como no exemplo, vamos realizar a multiplicação por 2 e copiar apenas a parte inteira desse resultado. Em seguida, vamos multiplicar a parte fracionária por 2 novamente e copiar a parte inteira. Esse processo se repete até que voltemos a ter o mesmo número fracionário do início.

![[image 63.png|image 63.png]]

## Fixed Point

![[image 1 47.png|image 1 47.png]]

A representação por ponto fixo consiste em reservar bits para a representação de números fracionários. Cada bit representa uma potência de 2, cada vez mais negativo, diminuindo o tamanho do valor subsequentemente.

- No entanto, essa representação não é a ideal para números que não sejam múltiplos das potências de 2 e nesse caso fazemos uma aproximação.

![[image 2 38.png|image 2 38.png]]

- Outro problema é que reservamos parte dos bits para a parte fracionária, reduzindo assim a amplitude de representação dos bits.

# Floating

A representação por ponto flutuante usa o conceito de mantissa e expoente, também usadas na notação científica.

- A mantissa corresponde ao número entre 1 e 9.99.

- O expoente corresponde ao valor que é o expoente da base 10.

![[image 3 31.png|image 3 31.png]]

Para os binários usamos uma certa quantidade de bits para a mantissa, que varia entre 1 e 2, e uma para o expoente, que nesse caso, possui base 2. Isso garante uma maior amplitude de representação dos bits.

![[image 4 28.png|image 4 28.png]]

Existem ainda duas formas de representação por ponto flutuante: single-precision e double-precision.

- Single-precision: usa 32 bits para representar o número:
    
    - 1 para sinal;
    
    - 8 para expoente, sendo 1 para sinal (-127 → 128). Para saber o valor, calculamos o valor decimal representado e subtraímos 127.
    
    - 23 para mantissa, mas assumindo que o primeiro bit é sempre 1, podemos usar 23 para representação fracionária, com o número indo de 1/2, 1/4 até a 23º potência negativa de 2.
    

![[image 5 20.png|image 5 20.png]]

- Double-precision: usa 64 bits para representar o número.
    
    - 1 para sinal;
    
    - 11 para expoente;
    
    - 52 para a mantissa;