---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-09-23T23:08
---
O tratamento de exceções é utilizado para os casos onde um programa passa por várias verificações antes de, de fato, executar as suas operações.

Em linguagens mais convencionais, esse processo é oneroso e passa pela escrita de várias verificações, e o código em si acaba misturado às verificações. Mas em linguagens orientadas a objeto existe uma maior facilidade.

- É o famoso `try{}catch(){}`.

![[image 134.png|image 134.png]]

Separamos claramente o código operacional do código de tratamento de exceções.

![[image 1 102.png|image 1 102.png]]

- Java já tem um tipo nativo para ler arquivos, mas ele necessita de um tratamento de exceções, para o caso de o nome do arquivo inserido não existir.

- Perceba que o `catch` recebe como parâmetro uma variável do tipo `Exception` .

  

Além das exceções já existentes e que são diagnosticadas pelo compilador, podemos definir as nossas próprias exceções. Para tal, existem três formas:

- Definição através de uma subclasse de `Exception` e chamando no código principal através do `throw new nameOfException()`
    
    - a definição do caso acontece diretamente no código.
    

- Indicando que um método lança uma exceção, direta (método `throws Exception`)e indiretamente (chama outra método que lança uma exceção).

![[image 2 81.png|image 2 81.png]]

![[1bb6bd90-9d4c-47d4-82ea-7dee72e07695.png]]

![[image 3 69.png|image 3 69.png]]