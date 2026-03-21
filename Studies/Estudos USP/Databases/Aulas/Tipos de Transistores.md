---
Course:
  - https://www.notion.so/Eletr-nica-1e2fa7f60cd880e4aabad53a3b5539e4?pvs=21
Last Edited: 2025-08-10T22:02
---
Transistores podem ser usados no lugar de chaves para fechar ou abrir um circuito.

Existem três perninhas, as quais tem funções funções diferentes a depender do tipo de transistor.

![[image 65.png|image 65.png]]

![[image 1 49.png|image 1 49.png]]

# Bipolar

Os transistores são feitos de materiais semicondutores, isto é, que podem funcionar como isolantes ou condutores. O material mais comum é o silício.

- Emissor: liga-se a um lado do circuito principal.

- Base: permite a passagem de corrente no circuito principal.

- Coletor: liga-se ao outro lado do circuito principal.

### Funcionamento e Características

==No caso do transistor bipolar, a corrente flui através do circuito principal somente quando existir uma corrente passando por ele próprio, através da perninha intermediária, a base.==

- Aplica-se em média 0,6V a 0,7V para permitir a corrente passar.
    
    - ==A intensidade da corrente na base influencia na intensidade da corrente no circuito principal, de modo que o transistor bipolar pode funcionar como um controlador de potência.==
        
        - Isso só é possível no tipo bipolar, pois nestes é possível definir uma resistência, enquanto os mosphets já tem um resistor nativo.
            
            ![[image 2 40.png|image 2 40.png]]
            
        
    

- ==A corrente na base é muito menor do que a corrente do circuito principal.==

- A base consume parte da corrente principal.

  

  

Existem dois tipos de transistores bipolares, o NPN e o PNP.

Para resumir, o uso dos transistores bipolares é mais voltado em casos em que é necessário ==**amplificar sinais analógicos**== ==(áudio, sensores, etc.) ou trabalhar com== ==**correntes menores**== ==controladas de forma precisa.==  

## NPN

- Os componentes do circuito estão ligados ao coletor, o qual liga-se ao positivo da fonte de tensão.

- O emissor liga-se ao polo negativo da fonte de tensão. A corrente total passa pelo emissor para regressar a fonte.

![[image 3 33.png|image 3 33.png]]

- O chamado circuito de controle é o responsável por alimentar a base, e esta o circuito principal.

- O circuito de controle funciona ainda que o principal não esteja.

## PNP

- O emissor liga-se ao polo positivo da fonte de tensão. Parte da corrente destina-se a base e a outra ao circuito principal.

- Os componentes continuam ligados no coletor, mas este agora liga-se no polo negativo.

- O circuito de controle funciona ainda que o principal não esteja.

![[image 4 29.png|image 4 29.png]]

---

# Mosfet

É um transistor de efeito de campo (FET), pertencente a essa família de transistores.

MOS (Metal Oxide Semiconductor) refere-se a estrutura da construção do Gate.

Existem dois tipos, o enriquecimentoo e depressão.

Existem três pernas:

- Fonte/Source

- Gate ou Porta

- Dreno/Drain

### Funcionamento

==O princípio de funcionamento do transistor mosfet é a tensão.== Se ela deve ser menor ou maior do que a principal, isso vai depender do tipo, que pode ser NMOS ou PMOS.

- Existe a TH, a tensão threshold, o valor mínimo para que o transistor cumpra seu papel na condução.

- Existe pouquíssimo consumo de corrente no gate.

Para resumir, o uso dos transistores bipolares é mais voltado em casos em que é necessário ==**chavear cargas**== **(sim ou não/0 ou 1)** ==(tipo motores, LEDs de alta potência, fontes de energia), especialmente quando precisa de== ==**velocidade alta**== ==e== ==**baixo consumo**====.==  
  

## Enriquecimento tipo N (NMOS)

![[image 5 21.png|image 5 21.png]]

Para que haja corrente da fonte para o dreno, é necessário que haja uma tensão no gate maior que em source.

## Enriquecimento tipo P (PMOS)

![[image 6 14.png|image 6 14.png]]

Para que haja a condução de corrente de source para dreno (transistor ativo) é necessário que a tensão de gate seja menor que a tensão de source.

- Para que haja corrente, é necessário que a diferença de tensão entre source e gate seja menor que o valor da tensão threshold.