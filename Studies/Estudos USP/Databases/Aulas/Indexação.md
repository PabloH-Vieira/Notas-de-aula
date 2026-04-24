---
Course:
  - "[[Organização de Arquivos]]"
Last Edited:
---
Tem a forma de uma struct, com métodos e valores.
A poda diz respeito a ignorar sub-árvores em um arquivo. Quanto mais otimizada a estrutura de indexação, mais podas há.
Um índice simples é composto por uma chave de busca (um campo de um registro, por exemplo) e um campo de referência (RRN para registros de tamanho fixo ou byte offset para tamanho variável).
No índice os campos e registros de tamanho fixo (as chaves de busca) devem obrigatoriamente estar ordenados. Essa característica permite acessar os registros que podem estar desorganizados no arquivo.
- Isso tem como objetivo realizar buscas binárias.

A indexação na busca é utilizada quando o número de retornos é baixo. Para ilustrar, sistemas de Bancos de Dados da Oracle utilizam a indexação quando retorna-se 10% ou menos do total de registros. Caso essa porcentagem seja maior, utiliza-se a busca sequencial.

O passo-a-passo de uma busca é:
- Busca binária pelo índice, acessa o RRN
- Acesso direto ao arquivo através do RRN

Quando removemos um registro que estava indexado, ele deve ser removido totalmente da estrutura de índice. No entanto, isso não é feito diretamente no arquivo.
Antes de realizar inserções ou remoções na memória secundária, isto é, no arquivo com os registros ou no index, guardamos as alterações na memória primária. 
- O primeiro passo é fazer o **carregamento** das informações do índice para a RAM.
- Os valores de campos para novas inserções são descritos na RAM.
- Puxamos o conteúdo dos campos do cabeçalho do arquivo.
- Realiza-se as operações necessárias no arquivo principal.
- Atualiza-se o conteúdo do índice ainda na memória secundária.
- Realize a **reescrita** do índice com o conteúdo recém atualizado.

A manipulação dos dados realizada na memória secundária pode utilizar de estruturas de dados que maximizem o desempenho.