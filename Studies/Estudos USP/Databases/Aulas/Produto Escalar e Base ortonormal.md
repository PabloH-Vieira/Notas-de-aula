---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
O produto escalar entre vetores é uma operação que resulta em um número real,

![[image 13.png|image 13.png]]

Dados os vetores ${\vec{u}}$ e ${\vec{v}}$ o produto escalar entre eles, isto é ${\vec{u}}*{\vec{v}}$:

- Se ${\vec{u}}$ ou ${\vec{v}}$ é nulo, então ${\vec{u}}*{\vec{v}}=0$;

- Se ${\vec{u}}$ e ${\vec{v}}$ são não nulos e ${\Theta}$ é a medida entre eles, calculamos o produto escalar por:

$${\vec{u}}*{\vec{v}}= ||{\vec{u}}||*||{\vec{v}}||*cos{\Theta}$$

Sendo {\vec{u}} e {\vec{v}} vetores de uma mesma base ortonormal podemos calcular o produto escalar entre eles por:

![[image 1 3.png|image 1 3.png]]

  

Sendo $||{\vec{u}}||$ a notação para o comprimento/módulo do vetor, que pode ser calculado por:

![[image 2 3.png|image 2 3.png]]

### Propriedades

![[image 3 2.png|image 3 2.png]]

Sendo a segunda propriedade a notação de vetores perpendiculares entre si.

- São perpendiculares/ortogonais se o ângulo ${\Theta}$ entre eles for igual a 90º, ${\pi}/2$

  

Outra importante propriedade é aquela em que o produto de dois vetores iguais é igual ao módulo do vetor ao quadrado.

![[image 4 2.png|image 4 2.png]]

---

## Base Ortonormal

Uma base ordenada $B=({\vec{u}}, {\vec{v}}, {\vec{w}})$ é dita ortonormal quando atende às condições:

- Os vetores são todos unitários, isto é $||{\vec{u}}||=||{\vec{v}}||=||{\vec{w}}||=1$

- Os vetores de B são dois a dois ortonormais, isto é: ${\vec{u}} \perp {\vec{v}}$, ${\vec{u}} \perp {\vec{w}}$, ${\vec{w}} \perp {\vec{v}}$

![[image 5 2.png|image 5 2.png]]

**Teorema**

Um produto escalar de vetores pertencentes a uma base ortonormal pode ser calculado a partir apenas das coordenadas desses vetores, ignorando o ângulo, já que ${\Theta}=1$ quando ${\Theta}={\pi}/2$

![[image 6 2.png|image 6 2.png]]

### Propriedades

![[image 7 2.png|image 7 2.png]]

### Desigualdade de Schuarz

$$|{\vec{u}}*{\vec{v}}| ≤ ||{\vec{u}}||*||{\vec{v}}||$$

## Ortonormalização ou Processo de Gram-Schmidtt