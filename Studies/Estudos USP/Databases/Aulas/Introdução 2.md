---
Course:
Last Edited: 2026-03-03T14:34
---
A memória secundária é o disco, enquanto a primária trata-se da RAM. Uma tarefa a ser processada sai da memória secundária, vai para a primária e então para a CPU.

  

Página de disco: unidade de transferência de bytes entre a RAM e o disco. O tamanho usual é de 4kb.

A análise de complexidade se dá em razão de acessos e leituras à disco.

A quantidade de páginas de disco em um arquivo é dada pelo tamanho do arquivo dividido por 4kb. Em decorrência disso, uma página de disco contém dados de apenas um arquivo.

- A segunda afirmativa passa do conceito de complexidade a partir do número de acessos à disco. Se um arquivo depende de vários acessos a disco, então a memória será muito mais acessada, por vários arquivos de uma vez.

  

A estrutura do disco é separada por páginas de disco, trilhas, setores e cilindros.

O disco é dividido em páginas de disco de 4kb cada. Um arquivo pode conter bytes em páginas de disco que não são necessariamente sequenciais. No entanto, quando uma cópia dessa página é realizada com o intuito de inserir os dados na RAM, as páginas copiadas são alocadas em endereços sequenciais.

### Algoritmo de acesso à disco e cópia na RAM

```Plain
se a página de disco está em RAM
	então responde sem acessar o disco
	senão
		se não existe espaço disponível na RAM
			então aplica uma política de substituição para definir uma página a ser retirada
			se a pagina foi alterada \#devemos salvar a versão alterada no disco, sobrescrevendo
				entao escreve a página que está em RAM no disco
		
		acessa a pagina em disco e transfere para a RAM
			 
```

_Buffer pool_ é uma técnica que reúne esse algoritmo junto da política de substituição.