---
Course:
  - https://www.notion.so/C-lculo-I-1adfa7f60cd88014a75fd9bc3add5134?pvs=21
Last Edited: 2025-08-10T22:08
---
Dizemos que um conjunto X com duas operações $+$ e $*$ é um corpo se

### **1. Propriedades da Adição**

1. **Fechamento da adição**: Para quaisquer , temos:
    
    $a,b∈Ka, b \in K$
    
    $a+b∈Ka + b \in K$
    

1. **Associatividade da adição**: Para quaisquer a, b, c $\in$ X
    
    $(a+b)+c=a+(b+c)(a + b) + c = a + (b + c)$
    

1. **Elemento neutro aditivo (zero)**: Existe um elemento 0x $\in$ X tal que, para todo x $\in$ X:
    
    $a+0x=a$
    

1. **Elemento oposto (inverso aditivo)**: Para todo $a∈X$, existe um $b \in X$ tal que:
    
    $a+(b)=a + (-a) = 0$
    

1. **Comutatividade da adição**: Para quaisquer $a,b∈X$, temos:
    
    $a+b=b + a$
    

---

### **2. Propriedades da Multiplicação**

1. **Fechamento da multiplicação**: Para quaisquer $a,b∈X,$ temos:
    
    $a⋅b∈K$
    

1. **Associatividade da multiplicação**: Para quaisquer $a,b,c∈X,$ vale:
    
    $(a⋅b)⋅c=a⋅(b⋅c)(a \cdot b) \cdot c = a \cdot (b \cdot c)$
    

1. **Elemento neutro multiplicativo (um)**: existe um elemento especial 1x $\in$ X tal que para todo $a\in X$
    
    $a⋅1x=a$
    

1. **Elemento inverso multiplicativo**: Para todo $a≠0$ em X, existe um b $\in X$ tal que:
    
    $a⋅b=a⋅a^{−1}=1$
    

---

### **3. Propriedade Distributiva (Ligação entre as Operações)**

Além dessas **9 condições**, o conjunto deve satisfazer a **distributividade**:

$a⋅(b+c)=a⋅b+a⋅c$, $∀a,b,c∈X.a \cdot (b + c) = a \cdot b + a \cdot c, \quad \forall a, b, c \in X.$

Essa propriedade garante que a multiplicação interage corretamente com a adição.

---

A partir dessas propriedades pode-se observar que os conjuntos $\mathbb{N}$ e $\mathbb{Z}$ não são corpos, mas $\mathbb{R}$ e $\mathbb{Q}$ sim.

  

## Proposição

Se X com + e $\cdot$ é um corpo e x, y, z $\in$ X são tais que $x+y=z+y$ então $x=y$.

  

# Conjunto Ordenado

Dizemos que um conjunto X é totalmente ordenado por ≤ se as seguintes condições forem verdadeiras:

1. x ≤ x para todo x $\in$ X.

1. se x ≤ y e y ≤ z, então x ≤ z.

1. se x ≤ y e y ≤ x, então x=y.

1. Dados x, y $\in$ X, temos que x ≤ y ou y ≤ x.

  

### Corpo totalmente ordenado

Dizemos que um corpo X, com operações + e $\cdot$, que é totalmente ordenado por ≤ é um corpo totalmente ordenado se as seguintes condições forem atendidas:

1. Se x ≤ y então x+z ≤ y+z ∀ x, y, z $\in X$.

1. Se x ≥ 0x e y ≥ 0x, então $x\cdot y$ ≥ 0x.

  

$\mathbb{R}$ e $\mathbb{Q}$ com as operações usuais e com a ordem usual são corpos totalmente ordenados.

  

Dado um corpo ordenado X totalmente ordenado por ≤, dizemos que $I ⊂ X$ é um intervalo se, para quaisquer x, y $\in I$, um z é tal que x ≤ z ≤ y, então z $\in I$.

  

Até aqui, estudamos propriedades dos conjuntos dos reais e dos racionais, mas é importante separá-los para dar continuidade ao estudo. Para isso, utiliza-se o Axioma da Completude.

## Axioma da Completude

Suponha que X é um corpo totalmente ordenado e, para cada n $\in \mathbb{N}$, fixe $a{\tiny{n}}$, $b{\tiny{n}} \in X$ de forma que:

- [$a{\footnotesize{n}}$, $b{\footnotesize{n}}$] é não vazio.

- [$a{\footnotesize{n+1}}$, $b{\footnotesize{n+1}}$] ⊂ [$a{\footnotesize{n}}$, $b{\footnotesize{n}}$] ∀ n $\in \mathbb{N}$.

Se sempre que isto for um fato, existe pelo menos um elemento em todos os [$a{\footnotesize{n}}$, $b{\footnotesize{n}}$] , dizemos que X é completo.

- $\mathbb{R}$ com as operações usuais e ordem usual, é completo.