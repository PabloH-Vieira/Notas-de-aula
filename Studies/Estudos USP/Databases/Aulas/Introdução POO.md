---
Course:
  - "[[Programação Orientada a Objetos]]"
Last Edited: 2026-03-05T16:46
---
Ao criar um arquivo, o nome dele deve ser o mesmo da classe principal dentro daquele arquivo.
É importante que as classes que se relacionem estejam no mesmo diretório para que a JVM encontre-as.
Isso é importante, pois existem comandos do Java Compiler e do Executável que necessitam da especificação da pasta de classes.
Variáveis e métodos tem controles de acessos.
Em geral, as variáveis são privadas -- isso significa que outras classes não podem alterar o valor das variáveis. Para isso utilizamos os métodos da classe, pois nesse controle de acesso apenas elementos da própria classe podem alterar o valor.
O construtor tem o mesmo nome da classe. Uma classe pode ter mais de um tipo de construtor. Podemos, por exemplo, definir valores iniciais, ou definir parâmetros para o usuário passar ao instanciar o objeto.
~~~ java
public class Cadeira{
	private String posicao;
	private boolean ocupado;
	
	public Cadeira(){
	}
	
	public Cadeira (String pos, boolean oc){
		posicao = pos;
		ocupado = oc;
	}
}
~~~

Como convenção, nome de classe inicia com letra maiúscula. Se houver dois nomes, cada um inicia dessa maneira.
Para nomes de variáveis e métodos, caso haja apenas uma palavra, todas as letras são minúsculas. Para variáveis com mais de uma palavra, a primeira é totalmente minúscula, e as próximas iniciam com maiúscula.

O casting é obrigatório caso seja necessário a atribuição de valores entre variáveis de tipos diferentes.

Existe um for para arrays, sendo a sintaxe `for (int k : v)`
A string é um objeto em Java, ou seja, possui sua própria classe. Não podemos realizar operações como comparação diretamente com a variável. Ao invés disso, devemos usar métodos específicos da classe.

É possível associar um rótulo a loops, de modo que podemos usar um break para loops mais externos.
Existe o try e o catch para tratar erros no código. Qualquer erro dentro do try leva diretamente para o bloco do catch.
- Se for tratada, a execução continua normalmente. No entanto, caso não estiver, a execução é interrompida.
- Existe a propagação de exceções, pois a exceção pode ser tratada dentro de um aninhamento de funções.
- É possível criar diversos catches dentro de um mesmo try.

