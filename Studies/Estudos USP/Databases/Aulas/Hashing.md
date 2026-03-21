---
Course:
  - https://www.notion.so/Introdu-o-Ci-ncia-da-Computa-o-II-24efa7f60cd880bbbbcaf479fda73ab6?pvs=21
Last Edited: 2025-11-16T14:36
---
## O que é?

Utilizar a busca por hash é uma forma muito eficiente de busca. Você insere uma _string_ (a chave) e a função de busca retorna um valor (o endereço) na complexidade $O(c)$, isto é, uma constante (o que independe do tamanho do vetor).

A função _hashing_ não possui um padrão que indique qual número será retornado após inserir uma _string,_ mas ela deve seguir alguns requisitos:

- Consistência: a mesma chave deve gerar sempre o mesmo endereço.

- Variabilidade: a função deve mapear diferentes endereços para diferentes chaves, de forma que evitemos a repetição do mesmo resultado múltiplas vezes.

A sua utilização consiste em guardar informações referentes à chave no endereço que a função fornece para aquela chave. Assim, quando inserirmos a chave na função, vamos acessar o endereço no qual a informação referente a ela está guardada.

- Exemplo: gostaríamos de guardar o preço das mercadorias em um mercado. Inserimos as chaves e guardamos nos endereços gerados para cada mercadoria o valor correspondente.

- Detalhe: por isso é importante seguir os requisitos, para que possamos sempre acessar o endereço correspondente a chave e para não gerar conflitos, isto é, quando a função destina o mesmo endereço para chaves diferentes.

Essa é a definição de tabela _hashing._ A relação entre um vetor e uma função de _hash_, que guarda os valores referentes às chaves em endereços calculados pela função.

A maioria das linguagens já vem com a tabela de _hashing_ implementada, muitas vezes com outros nomes como dicionário, mapas entre outros. Em Python, podemos criar uma tabela _hashing_ utilizando a função `book = dict()` , e inserimos os valores na forma `book["apple" = 1.50` .

# Colisões

As colisões ocorrem quando a função _hashing_ retorna o mesmo endereço para diferentes chaves. É muito difícil escrever uma função que gere endereços diferentes para incontáveis chaves. Portanto, existem outras maneiras de contornar essa situação.

A forma mais simples de resolver isso é criando uma lista encadeada dentro do endereço e lá dentro armazenar as informações das diferentes chaves localizadas naquele endereço.

- Essa é a abordagem de _hashing_ estático aberto.

- Outra abordagem é o _hashing_ estático fechado, onde utilizamos técnicas de _rehash_ para evitar colisões (segunda função _hash_).

![[image 116.png|image 116.png]]

A função _hash_ pode ser muito eficiente, tanto na busca, na inserção ou remoção de itens. No entanto, para garantir essa eficiência, é necessário evitar ao máximo as colisões. Para isso, é preciso:

- Um baixo fator de carga, dado pela razão entre a quantidade de itens ocupando a tabela e o total de espaços.
    
    - Quanto maior o fator de carga, mais ocupado está o array onde a tabela guarda as informações. Para garantir que haja espaço para todos, devemos aumentar o tamanho do array, o que é conhecido como redimensionamento.
    
    - Um bom fator de carga reduz a probabilidade de colisões.
    

![[image 1 89.png|image 1 89.png]]

Também é importante criar funções _hashing_ que produzam endereços de forma simétrica, diminuindo a quantidade de colisões ao máximo. Um exemplo é o método SHA.

Outro exemplo de função eficiente é usar o módulo da divisão $k \% B$, sendo _k_ o valor da chave (para strings, somamos os valores ASCII de cada caractere) e _B_ o tamanho do vetor.

## _Hashing_ fechado

### _Rehashing_

O _rehashing_ é uma abordagem de tratamento de colisões que consiste em utilizar uma segunda função _hashing_.

Uma boa técnica de _rehashing_ possibilita:

- cobrir o máximo de índices dentro do vetor.

- evitar agrupamento de dados.

Primeiro calculamos a função _hashing_ e verificamos se o endereço (ou _bucket_) $h(k)$ já está ocupado. Se estiver, aplicamos a função _hashing_ para aquele _bucket._

  

**Exemplo de implementação (sondagem linear)**

Rehash de $h(k) = (h(k) + i) \% B$, com $i$ variando de 1 a $B-1$($i$ é incrementado a cada tentativa).

- Essa função faz com que a função percorra os próximos _buckets_ após o _bucket_ de $h(k)$, até encontrar um vazio. O problema é que isso pode levar vários passos (no pior caso, checamos todas as posições da tabela).

![[image 2 71.png|image 2 71.png]]

Outro problema que pode surgir é que caso um valor seja removido antes do _Smith_ a busca pode retornar que esta chave não está na lista.

- Uma forma de tratar isso é sinalizar que a busca pode continuar após o elemento removido.

  

**Exemplo de implementação (sondagem quadrática)**

Rehash de $h(k) = (h(k) + c1i + c2i2) \% B$, com $i=1...\space B-1$ e constantes $c\footnotesize1$e $c\footnotesize2$.

  

### _Hash_ duplo

Utilizamos uma segunda função _hash_ auxiliar para encontrar o _bucket_.

**Exemplo**

Rehash de $h(k) = (h(k) + i*h{\footnotesize{aux}}(k)) \% B$, com $i=1... \space B-1$, sejam $h(k)= k\%B$ e $h{\footnotesize{aux}}(k)=1+k\%(B-1)$.

## _Hashing_ aberto

Essa é a abordagem em que a tabela de _buckets_ contém ponteiros para listas encadeadas de elementos.

Se os elementos dentro da lista estiverem ordenados, reduz-se a busca dentro dela.