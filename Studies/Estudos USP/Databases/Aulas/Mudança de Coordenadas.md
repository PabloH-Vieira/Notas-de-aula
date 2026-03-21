---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
Todos os sistemas de coordenadas possuem um ponto de origem e uma base (isto é, três vetores).

Um mesmo ponto pode ter diferentes coordenadas tridimensionais para diferentes sistemas de coordenadas de um mesmo espaço.

![[image 22.png|image 22.png]]

![[image 1 12.png|image 1 12.png]]

Também definimos a origem de cada um dos sistemas de coordenadas. Esse ponto de origem possui coordenadas (0, 0, 0) com relação ao seu sistema de coordenadas, mas outros valores com relação a um outro sistema de coordenadas.

![[image 2 9.png|image 2 9.png]]

- Perceba que O’ é a origem de $\Sigma2$, e por isso tem as coordenadas (0, 0, 0) com relação a $\Sigma2$. No entanto, essas coordenadas são outras com relação a $\Sigma1$, determinados por (_h, k, m_).

### Como fazer a mudança de coordenadas

Existe um roteiro pré-determinado para realizar a mudança de coordenadas.

![[image 3 4.png|image 3 4.png]]

- X, Y, Z são as coordenadas do ponto X no sistema $\Sigma1$

- h, k, m são as coordenadas da origem de $\Sigma2$ em função do $\Sigma1$.

- os valores _a11, a22, a33_ são os valores da matriz mudança de base do ponto X subtraído da origem O’ de $\Sigma1$ para $\Sigma2$.
    
    ![[image 4 4.png|image 4 4.png]]
    

- _u, v, w_ são as coordenadas originais do ponto no sistema de coordenadas $\Sigma2$

---

### Observação

No caso específico onde os sistemas de coordenadas são iguais, e por consequência, as origens também, as equações de mudança de coordenadas ficam muito mais simples, pois os coeficientes da matriz de mudança seguem uma matriz identidade.

![[image 5 4.png|image 5 4.png]]

---

# Plano de Duas Dimensões

Há duas dimensões para tudo.

![[image 6 4.png|image 6 4.png]]

---

Para os conteúdos a seguir, iremos supor que todos os sistemas de coordenadas serão ortogonais, isto é, a base do sistema é ortonormal. Além disso, o plano tem duas dimensões

## Translação

Nesse caso, a matriz de mudança é identidade, ou seja, as bases são iguais.

Para a translação, iremos mudar as coordenadas da origem.

![[image 7 4.png|image 7 4.png]]

- Mudamos as coordenadas da origem do sistema $\Sigma1$, antes iguais a (0,0) para $\Sigma2$, iguais a (u, v)

## Rotação

Mudamos as coordenadas da base, enquanto a origem se mantém.

Tomamos um ângulo $\Theta$ que transforma o sistema $\Sigma1$ (O, $\vec{e1}$, $\vec{e2}$) em $\Sigma2$ (O, $\vec{f1}$, $\vec{f2}$).

![[image 8 2.png|image 8 2.png]]

De forma que o ponto X é dado por (_x, y_) no sistema $\Sigma1$ e (_u, v_) no sistema $\Sigma2$.

Outra forma de expressar isso é isolando u e v.

![[image 9 2.png|image 9 2.png]]

- Lembrando que _u, v_ são as novas coordenadas do sistema de coordenadas após a rotação, enquanto _x, y_ são as antigas.

### Tabela para memorização de mudança de coordenadas na rotação

![[image 10 2.png|image 10 2.png]]