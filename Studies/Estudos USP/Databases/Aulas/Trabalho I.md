	Recomendável no Linux (WSL).
Revisar alocação dinâmica e manipulação de arquivos.

~~~ c
fopen();
fclose();

fread (buffer, sizeof(), qntd, file *);
fwrite (buffer, sizeof(), qntd, file *);

ftell (file *); //informa a posição do ponteiro
fseek (file *, qntd, flag); //posiciona o ponteiro do arquivo

~~~

`fseek` é útil para posicionar o ponteiro do arquivo.
- `0, seek_set` posiciona o ponteiro no início do arquivo

Além disso:
- abrir o arquivo no modo correto (texto para o arquivo .csv e binário para o restante).
- problema do *padding* (compilador preenche bytes não utilizados de variáveis de tamanho diferentes, de modo que todos tenham o mesmo tamanho): não ler o struct em apenas um `fread`. Ao invés disso, ler campo a campo com um `fread`.
- `fread` retorna 0 quando chega no fim do arquivo. Utilizar isso para terminar a leitura.


Outro requisito do trabalho é a modularização: com arquivos e funções separadas.

##### Cabeçalho
- status: indica o estado do arquivo. Definir como "consistente" (1) apenas ao final de uma função. Se houver algum erro durante esse processo, será possível identificar isso através do status.
- não basta definir o `nroEstacoes` a partir dos nomes das estações, pois existem nomes repetidos (com id's diferentes)
![[Pasted image 20260325150722.png]]

##### Registro de dados
É um registro de 80 bytes com tamanho fixo.
![[Pasted image 20260325151117.png]]

#### Resumo das Funcionalidades
###### 1. Leitura de CSV

###### 2. Exibição dos dados e registros de um arquivo

###### 3. Busca de campos em um arquivo

###### 4. Remoção de registros em um arquivo

###### 5. Inserção de novos registros em um arquivo

###### 6. Atualização dos registros de um arquivo

##### Vídeo
Sete minutos de vídeo explicando a implementação de cada uma das funcionalidades.

***
#### Observações:
- usar o debugger `gdb` para compilar
- extensão hex editor para auxiliar na leitura/escrita de arquivos binários.
- `valgrind /programTrab` para verificar possíveis leaks. 
- strsep (da biblioteca gnu, basta copiar o código da função ao invés de importá-la) ou strtok (da biblioteca padrão)
- remoções de estações marcam o registro da própria estação como "removida", mas também marca o campo de outras estações que fazem par com ela.