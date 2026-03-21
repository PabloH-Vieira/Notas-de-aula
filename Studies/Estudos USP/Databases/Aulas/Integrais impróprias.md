---
Course:
  - https://www.notion.so/C-lculo-II-24efa7f60cd880b0b8e2ea5108f9eeb0?pvs=21
Last Edited: 2025-10-10T09:04
---
Uma das integrais impróprias é aquela onde um dos limites de integração é $\infin$. Nesse caso, substituímos por uma variável qualquer e realizamos todas as operações quando essa variável tende a $\infin$.

![[image 94.png|image 94.png]]

Dizemos que uma integral ==**converge**== se o seu resultado é um ==**valor finito**==.

Dizemos que uma integral ==di====**verge**== se o seu resultado é um ==**valor infinito, isto é**== ==$+\infin \space -\infin$====.==

## Teste para Comparação

Dada duas funções f(x) e g(x) integráveis no intervalo [a,t], para todo t>a, e para todo x ≥ 0, e as duas funções estritamente crescentes, na forma 0 ≤ f(x) ≤ g(x)

### Teste de Convergência

> **Se a integral da função "maior" (g(x)) converge, então a integral da sua função "menor" (f(x)) também converge.**

- **Lógica:** Se a área sob a curva maior é finita, a área sob a curva menor também tem que ser finita.

- **Fórmula:** Se 0≤f(x)≤g(x) e ∫g(x)dx converge, então ∫f(x)dx converge.

### Teste de Divergência

> **Se a sua função f(x) for maior ou igual a uma outra função g(x) em um certo intervalo, e a integral da função "menor" (g(x)) diverge, então a integral da sua função "maior" (f(x)) também diverge.**

- **Lógica:** Se a área sob a curva menor é infinita, a área sob a curva maior também tem que ser infinita.

- **Fórmula:** Se f(x)≥g(x)≥0 e ∫g(x)dx diverge, então ∫f(x)dx diverge.