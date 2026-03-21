---
Course:
  - https://www.notion.so/Matem-tica-Discreta-24efa7f60cd88002b1c7c5a007d3faeb?pvs=21
Last Edited: 2025-09-24T18:16
---
## Divisão de inteiros

![[image 73.png|image 73.png]]

Por exemplo, a divisão inteira $3/2$ pode ser escrita como $3=2q+r$.

- A solução única para este caso é $q = 1, {\space}r=0$.

- A única restrição é que $0<=r<d-1$

- Na divisão de reais, não existe um _r._

- Outra restrição é que se o denominador ou o divisor forem negativos, contraria-se o teorema de Euclides, e devemos manipular o quociente para evitar isso.

### Módulo e Propriedades

![[image 1 55.png|image 1 55.png]]

![[image 2 45.png|image 2 45.png]]

**Propriedades**

![[image 3 38.png|image 3 38.png]]

![[image 4 34.png|image 4 34.png]]

![[image 5 24.png|image 5 24.png]]

![[image 6 16.png|image 6 16.png]]

![[image 7 14.png|image 7 14.png]]

![[image 8 11.png|image 8 11.png]]

---

### Conjunto ${\mathbb{Z}}{\small{d}}$

![[image 9 7.png|image 9 7.png]]

Com o conceito de classe entendido, a definição de Zd fica mais clara. O conjunto Zd é o conjunto de **todas as classes de equivalência possíveis** para um divisor d.

No exemplo com d=5:

- Os únicos restos possíveis na divisão por 5 são 0, 1, 2, 3 e 4.

- Cada um desses restos define uma classe de equivalência única.

- Portanto, existem exatamente 5 classes de equivalência distintas, como mostra a anotação na imagem.

O conjunto Z5 é, então, o conjunto formado por essas 5 classes:

![[image 10 5.png|image 10 5.png]]

Resumindo, Z5 não é um conjunto de números, mas sim um conjunto que contém 5 conjuntos (as classes de equivalência), onde cada classe agrupa todos os infinitos inteiros que compartilham o mesmo resto na divisão por 5.

![[image 11 4.png|image 11 4.png]]

Podemos reescrever o teorema da divisão de Euclides como:

![[image 12 2.png|image 12 2.png]]

### 1. `n (mod d) = r` implica `[n]_d = [r]_d`

Esta primeira linha diz que se um número inteiro

`n` tem um resto `r` quando dividido por `d`, então a classe de equivalência de `n` é exatamente a mesma que a classe de equivalência de `r`.

- **Em outras palavras:** Todo número pertence à classe do seu resto.

- **Exemplo prático:** Vamos usar `d=5`. O número 18, quando dividido por 5, deixa resto 3. Ou seja, `18 (mod 5) = 3`. A propriedade nos garante que a classe
    
    `[18]_5` é idêntica à classe `[3]_5`. Isso simplifica as coisas, pois podemos sempre usar o resto (um número entre 0 e d-1) como o "nome" da classe.
    

### 2. `[n]_d = [r]_d` e `r ∈ {0, ..., d-1}` implica `n (mod d) = r`

Esta segunda linha é a implicação inversa e estabelece que esses "nomes" de classes são únicos. Ela diz que se um número

`n` pertence à classe de um resto padrão `r` (um número de 0 a d-1), então podemos garantir que o resto da divisão de `n` por `d` é, de fato, `r`.

- **Em outras palavras:** Se um número está na "classe do 3", o resto dele _tem_ que ser 3.

- **Exemplo prático:** Se eu te digo que um número `n` pertence à classe `[4]_5`, e como 4 está no conjunto `{0, 1, 2, 3, 4}`, você sabe com certeza que `n (mod 5) = 4`.

![[image 13 2.png|image 13 2.png]]

![[image 14 2.png|image 14 2.png]]

- O professor reduziu a notação, não estranhe.

![[image 15 2.png|image 15 2.png]]

---