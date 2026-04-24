---
Course:
  - "[[Programação Funcional]]"
Last Edited:
---
A palavra chave para criar tipos é o `data`. Nomeamos o tipo e passamos os construtores, seguidos pelos valores (que podem existir ou não), separados por pipes |.

``` haskell
data Talvez = Nada | Apenas a

data Shape = Circle Float Float Float | Rectangle Float Float Float Float
```
Podemos criar uma instância, para tratar cada possível valor da classe. Pode ser necessário para imprimir o valor de um tipo que não é Show.

``` haskell
data Clima = Bom | MaisOuMenos | Ruim

instance Show Clima where
	show Bom = "O clima está bom"
	show MaisOuMenos = "O clima está mais ou menos"
	show Ruim = "O clima está mais ou menos"
```
Outras instâncias possíveis seriam, por exemplo, permitir comparações, ordenações etc.
A palavra chave `deriving` permite realizar as conversões básicas, bastando passar os tipos.

``` haskell
data Clima = Bom | MaisOuMenos | Ruim
	deriving (Show, Eq, Ord)
```
