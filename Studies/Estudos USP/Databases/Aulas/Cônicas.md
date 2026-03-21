---
Course:
  - https://www.notion.so/Geometria-Anal-tica-1adfa7f60cd88003b8d3d42ba3b0669b?pvs=21
Last Edited: 2025-08-12T21:33
---
### Elementos

- A1, A2: pontos no eixo X, chamados vértices;

- B1, B2: pontos no eixo Y, chamados vértices.

- F1, F2: focos;

- c: distância do foco para a origem.

- a: distância de A1 ou A2 para a origem.

- b: distância de B1 ou B2 para a origem.

## Elipse

A equação reduzida é dada por:

$$\frac{(x-m)^2}{a^2}+\frac{(y-n)^2}{b^2}$$

Aparecendo mais comumente como $\frac{x^2}{a^2}+\frac{y^2}{b^2}=1$ quando a origem é (0,0).

Excentricidade é dada por e=c/a.

Existe uma propriedade muito característica:

$$a^2=b^2+c^2$$

A circunferência é um caso específico de elipse, na qual a distância a é igual a distância b.

![[image 24.png|image 24.png]]

Os focos também podem estar no eixo y, invertendo a forma da elipse e a fórmula: temos _x_ sobre _b_ e _y_ sobre _a._

---

## Hipérbole

![[image 1 14.png|image 1 14.png]]

A equação reduzida é dada por:

$$\frac{(x-m)^2}{a^2}-\frac{(y-n)^2}{b^2}$$

![[image 2 11.png|image 2 11.png]]

A hipérbole possui o seguinte aspecto, com as retas conhecidas como assíntotas sendo tangentes às hipérboles e dadas pelas fórmulas:

$y = -\frac{b}{a}*x$

$y = +\frac{b}{a}*x$

A relação importante para a hipérbole é a seguinte:

$$c^2=a^2+b^2$$

Existe o caso em que os sinais estão invertidos na equação reduzida, com x positivo e y negativo.

$$-\frac{(x)^2}{a^2}+\frac{(y)^2}{b^2}$$

e nesse caso invertemos a fórmula das assíntotas.

---

## Parábola

Determinamos um plano $\pi$, um ponto F e uma reta _r._ A parábola será o conjunto dos pontos equidistantes de F e _r._

![[image 3 6.png|image 3 6.png]]

- r: reta diretriz, igual a -p.

- 2p: parâmetro, distância do ponto F (foco) até a reta.

- V: fixado no eixo _x_ e com distância _p_ do ponto F e _p_ da reta _r._

- eixo de simetria: eixo que passa pelo foco e é perpendicular à reta _r._

A equação reduzida chega na forma:

$$y²=4px$$

- p: coordenada do foco no eixo _x._

Para o caso da parábola em pé, utilizamos a equação da parábola usual:

![[image 4 6.png|image 4 6.png]]

![[image 5 6.png|image 5 6.png]]

Outras formas da parábola

![[image 6 5.png|image 6 5.png]]

![[image 7 5.png|image 7 5.png]]

---

## Cônicas

A cônica é descrita pela fórmula:

$$G(x,y)=Ax^2+Bxy+Cy^2+Dx+Ey+F=0$$

As cônicas podem ser formadas por diferentes combinações:

1. **Conjunto Vazio.**
    
    1. $x²+y²+1=0$
    

1. **1 ponto.**
    
    1. $x²+y²=0$
    

1. **1 reta**
    
    1. $(x+y)²=0$
    

1. **Reunião de 2 retas**
    
    1. (x+y)(x+y+1)
    

1. **Reunião de 2 retas concorrentes**
    
    1. (x+y)(x-y)=0
    

1. **Elipse.**

1. **Hipérbole.**

1. **Parábola.**

1. **Circunferência.**

### Formas de simplificar a expressão que define a cônica

1. **Eliminar termos de 1º grau por translação**
    
    - Mudamos a origem encontrando um ponto dado por (h, k) que transforma aquela equação em $\overline{A}u²+\overline{B}uv+\overline{C}v+\overline{F}=0$, sendo esse ponto único chamado de centro da cônica/de simetria.
        
        - Eliminamos as variáveis D e E, igualando-as a zero.
        
        - Chegamos na equação abaixo após aplicar os valores de x ($x=h+w$) e de y($k+v$). Os termos de primeiro grau, D e F, podem ser igualados a 0, o que nos leva ao valor de _h_ e _k._
        
        - Percebe-se que os coeficientes de segundo grau, _A, B e C,_ permanecem inalterados.
        
        ![[image 8 3.png|image 8 3.png]]
        
        - Na nova equação encontrada, teremos _u_ no lugar de _x_ e _v_ no lugar de _y._
        
    
    - Para determinar se existe esse ponto, fazemos uma determinante |$\frac{B}{2C}$$\frac{2A}{B}$|=$B²-4AC$, devendo haver apenas uma solução.
        
        - se esse determinante for diferente de 0, ele tem uma única solução.
        
        - se esse determinante for igual a 0, há infinitas soluções ou não há soluções.
        
        ![[image 9 3.png|image 9 3.png]]
        
    
      
    

1. Eliminar termo misto de 2º grau por rotação
    
    - Chegamos à fórmula $A'u²+C'v²+D'x+E'v+F'=0$, com B=0 e novas variáveis iguais a u e v. Para tal, realizamos uma rotação do sistema por um ângulo.
    
    - Relações entre os termos e o ângulo:
    
    ![[image 10 3.png|image 10 3.png]]
    
    - Para tal, temos a relação: se $a≠c$ → $tg2{\Theta}=\frac{B}{A-C}$, e se $a=c$ → $cos2{\Theta}=0$ e nesse caso o ângulo é igual a 45º ou 135º.
    
    - Relação importante entre A’ e C’.
    
    ![[image 11 2.png|image 11 2.png]]
    

  

Em equações mais complexas, devemos primeiro reduzir por translação e depois por redução.