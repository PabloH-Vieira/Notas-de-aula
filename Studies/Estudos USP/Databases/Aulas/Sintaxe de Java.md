---
Course:
  - https://www.notion.so/Programa-o-Orientada-Objetos-265fa7f60cd880e59d77df13ebae5811?pvs=21
Last Edited: 2025-08-23T00:29
Related to Semestres:
  - "[[Estudos Complementares]]"
---
Declaramos uma classe, dizendo se ela é pública ou não.

Devemos declarar no escopo da classe todos os seus atributos e métodos, já tipados.

Há como deixar atributos privados, ainda que a classe seja pública.

Para declarar o construtor, usamos uma função cujo tipo é o nome da função, e parâmetros os valores que o usuário passará para os atributos.

É comum utilizarmos a palavra `self` que retorna um ponteiro para o próprio objeto.

Para fazer com que os valores dos atributos possam ser acessados e mudados fora da classe, ainda que esses atributos sejam privados, utilizamos os métodos de `getter` e `setter`

- Podemos fazer isso ao invés de passar como argumento os valores dos atributos.

Para criar uma subclasse, utilizamos a palavra `extends Superclass` na declaração da subclasse

- Para declarar o construtor da subclasse criamos uma função cujo tipo é o nome da subclasse e passamos como parâmetro os atributos que serão passados pelo usuário. Dentro do construtor utilizamos o método `super` passando como argumentos os atributos da superclasse.

- Cada classe deve possuir um arquivo `.java` próprio e separado um do outro, com o mesmo nome da classe.

Podemos criar um método para imprimir uma mensagem. Esse é o `ToString`, que retorna uma `String`.

Para tornar a classe executável, precisamos criar o método `main`, cujo tipo é `static void` e recebe como parâmetro um array de `string`

Para instanciar um objeto criamos uma variável cujo tipo é o nome da classe e como valor chamamos o construtor, passando os valores dos atributos.

```Java
public class Veiculo{
    int AnodeFabricacao;
    private String modelo;
    private String marca;

    Veiculo(int adf, String m, String ma){
        AnodeFabricacao = adf;
        modelo = m;
        marca = ma;
    }
    //Getter
    public int getAnodeFabricacao() {
        return AnodeFabricacao;
    }
    //Setter, que altera o valor do atributo da classe
    public void setAnodeFabricacao(int anodeFabricacao) {
        AnodeFabricacao = anodeFabricacao;
    }
}
```

```Java
public class carro extends Veiculo{
    private int numPassageiros;
    private boolean airbag;

    public String toString(){
            return "O carro foi fabricado em " + getAnodeFabricacao() + " e possui " + numPassageiros + " passageiros.";
    }

    carro (int AnodeFabricacao, String modelo, String marca, int num, boolean airbag){
        super(AnodeFabricacao, modelo, marca);
        numPassageiros = num;
    }

    public static void main(String args[]){
        carro c = new carro(2015, "Fiat", "Palio", 4, true);
        System.out.println(c);
    }
}
```