---
Course:
  - "[[Cálculo III]]"
Last Edited:
---
É um sistema de vetores, em duas ou três dimensões. São determinados por funções vetoriais.
- Significa que existem vetores em todos os pontos do sistema.
No $\mathbb R$² temos $f(x,y) = P i + Q j$.
No $\mathbb R$² temos $f(x,y,z) = P i + Q j + R k$.
Onde P, Q e R são funções definidas em um região.

Para representar o campo vetorial devemos utilizar pontos, a partir dos quais teremos vetores. Esses vetores devem iniciar no ponto dado.
Ao aplicar o ponto na função, o coeficiente de i será para onde o vetor vai apontar no eixo x. O coeficiente de j será para onde o vetor vai apontar no eixo y.
**Exemplo**
![[Pasted image 20260330135921.png|310]]

## Divergência e curvas de campos vetoriais

Descreve o quão fluído são os vetores de um campo. Analisamos o quanto o fluído ocupa de uma região ao redor de P comparado com o quanto ele vaza da região.
- Quanto mais ele ocupar, ao invés de vazar, dizemos que a divergência será mais negativa.
- Quanto mais ele vazar, mais positiva será a divergência. Chamamos a vizinhança de divergente.
- Se o fluído ocupar um valor da região exatamente igual ao valor com que ele vaza, a divergência será 0 no ponto. Chamamos a vizinhança de incomprimível.

Para calcular a divergência, utilizaremos a definição do campo vetorial junto à ideia de gradiente vetorial:
![[Pasted image 20260330144557.png]]
Esse valor é escalar, isto é, não vetorial.

### Curvas

Mede a tendência do fluído rotacionar na região.
- Essa curva determina de que forma o fluído rotaciona ou se ele sequer rotaciona.
- A curva é positiva quando o sentido da rotação é anti-horário.
- A curva é negativa quando o sentido da rotação é horário.
- Se a curva for nula, o fluído não tem rotação.

Essa rotação acontece em um ponto P.
Para calcular a curva utilizaremos a mesma ideia do campo vetorial e do vetor gradiente, mas dessa vez a operação será de multiplicação vetorial (resolvida por uma matriz).
![[Pasted image 20260330210222.png]]

Graficamente, observamos que uma vizinhança tem divergência quando existe diferença no módulo do vetor verticalmente (acima da região e abaixo da região). Se o módulo for igual, a divergência é 0.
Já a curva existe quando comparamos os vetores horizontalmente e observamos diferenças entre eles. O lado com maior módulo dita o sentido da rotação.

**Exemplo**

![[Pasted image 20260330211916.png]]