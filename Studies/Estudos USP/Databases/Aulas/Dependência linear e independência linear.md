---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
{\vec{u}}

{\in}

  

  

## Teorema da combinação linear

Os vetores ${\vec{u}},$ ${\vec{v}}$ ${\in}$ V³ são paralelos e coplanares somente se existem ${\alpha}$, ${\beta} {\in} {\mathbb{R}}$ tais que:

$${\alpha}{\vec{u}}+{\beta}{\vec{v}}=o$$

  

  

## Vetores linearmente dependentes (LD) e linearmente independentes (LI)

Os vetores ${\vec{u¹}}$, …, ${\vec{u^n}}$ ${\in}$ V³ são linearmente dependentes se existem ${\alpha}$, ${\beta} {\in} {\mathbb{R}}$ não todos eles nulos

$${\alpha}{\vec{u¹}}+...+{\beta}{\vec{u^n}}=o$$

Caso contrário, é dito que esses vetores são linearmente independentes.

  

  

Sendo assim, se dois valores são linearmente dependentes, eles serão paralelos, ou ainda, colineares

- Dois ou mais vetores são chamados de **colineares** quando pertencem à **mesma reta** ou a retas **paralelas** no espaço. Isso significa que um vetor pode ser escrito como um múltiplo escalar do outro.

  

  

==Dois vetores linearmente independentes não podem ser escritos como múltiplos escalares um do outro, isto é, não são paralelos, nem pertencem a mesma reta.==

  

  

1. O resultado ${\vec{0}}$ implica que o(s) vetor(es) é/são LD.

1. Se ${\vec{u}}$ ≠${\vec{0}}$, o vetor é LI.

1. Se dois vetores estão sendo somados e ao menos um deles está com coeficiente 0, eles serão LD, pois a soma será ${\vec{0}}$: $1{\vec{u}}+0{\vec{v}}$ = ${\vec{0}}$

1. Os vetores ${\vec{u}}$, ${\vec{v}}$ e ${\vec{w}} {\in}$ V³ são LD somente se esses vetores forem coplanares.

1. Ainda que o resultado da multiplicação escalar de ${\alpha}{\vec{u}}$ seja ${\vec{0}}$ é impossível determinar se o vetor ${\vec{u}}$ é LD, pois podemos supor que apenas ${\alpha}=0$ e ${\vec{u}}≠0$, nesse caso, ${\vec{u}}$ seria LI.

1. Se um conjunto de vetores é LI, então qualquer subconjunto deste será também LI.

  

==O conjunto de quatro ou mais vetores é sempre LD em V³.==

- ==O conjunto de vetores LI só pode ter, ao máximo, três vetores.==

- Como $\mathbb{R}^3$ tem dimensão 3, no máximo **três vetores** podem ser **linearmente independentes.** Se adicionarmos um quarto vetor, ele poderá ser escrito como uma combinação linear dos outros três, tornando o conjunto **linearmente dependente**

  

Se um subconjunto de vetores é linearmente dependente, então o conjunto maior também será.

- O conjunto $\{\vec{u}, \vec{v}, \vec{w}\}$, **contém um subconjunto dependente** $(\vec{u}, \vec{v})$, então o **conjunto todo também é dependente**.

- A dependência linear de três vetores **não garante** que **dois deles** sejam dependentes entre si.  
      
    

  

## Propriedade da desigualdade triangular

  
A **desigualdade triangular** é uma propriedade fundamental da **norma de vetores** e estabelece que, a soma dos comprimentos de dois vetores nunca pode ser menor que o comprimento da soma desses vetores.

  

Sejam dois vetores

$∥u+v∥≤∥u∥+∥v∥$

Ou seja, o comprimento do vetor resultante da soma é sempre **menor ou igual** à soma dos comprimentos dos vetores originais.

  

No espaço $\mathbb{R}^2$ ou $\mathbb{R}^3$, essa propriedade reflete o fato de que, em um triângulo, a soma de dois lados nunca pode ser menor que o terceiro lado.

  

## Teorema da combinação linear

Sejam ${\vec{u}}$, ${\vec{v}}$, ${\vec{w}} {\in}$ V³ LI. Então, para qualquer ${\vec{x}} {\in}$V³, existem únicos ${\alpha}$, ${\beta},$ ${\gamma}$ ${\in}$$\mathbb{R}$ tais que:

$${\vec{x}}={\alpha}{\vec{u}}+{\beta}{\vec{v}}+{\gamma}{\vec{u}}$$

==Em essência, é possível obter um vetor através de outros vetores. Em termos mais específicos, é dito que== ==${\vec{x}}$== ==é a combinação linear desses vetores.==

- Qualquer vetor em V³ pode ser escrito unicamente como combinação linear dos demais vetores nesse espaço.

  

**Não é possível** que a combinação linear de vetores coplanares gere um vetor fora do plano.

- ==Se todos os vetores usados na combinação linear== ==**pertencem ao mesmo plano**====, então== ==**qualquer combinação linear desses vetores também estará no mesmo plano**====.==