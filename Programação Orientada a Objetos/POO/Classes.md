***
As classes são um conceito central na [programação orientada a objetos](POO). Elas funcionam como um "molde" ou "blueprint" para criar [objetos](Objetos). Uma classe define as propriedades ([atributos](Atributos)) e os comportamentos ([métodos](Métodos)) que os [objetos](Objetos) criados a partir dela terão.
***
## Exemplo em [[Java]]
***
Nesse exemplo iremos usar a Classe ``Carro`` para demonstrar os [atributos](Atributos) e os [métodos](Métodos)

```java
public class Carro {

    // Atributos da classe Carro
    String marca;
    String modelo;
    String cor;
    int ano;

    // Setter para o atributo marca
    public void setMarca(String marca) {
        this.marca = marca;
    }

	// Getter para o atributo marca
    public String getMarca() {
        return marca;
    }
    
    // Construtor da classe Carro
    public Carro(String marca, String modelo, String cor, int ano) {
        this.marca = marca;
        this.modelo = modelo;
        this.cor = cor;
        this.ano = ano;
    }

    // Método para exibir informações do carro
    public void exibirInformacoes() {
        System.out.println("Marca: " + marca);
        System.out.println("Modelo: " + modelo);
        System.out.println("Cor: " + cor);
        System.out.println("Ano: " + ano);
    }

    // Método para ligar o carro
    public void ligar() {
        System.out.println("O carro está ligado!");
    }
}

public class Main {
    public static void main(String[] args) {
        // Criando um objeto da classe Carro
        Carro meuCarro = new Carro("Toyota", "Corolla", "Preto", 2021);

        // Chamando métodos do objeto meuCarro
        meuCarro.exibirInformacoes();
        meuCarro.ligar();

		 // Exibindo os valores iniciais
        System.out.println("Marca inicial: " + meuCarro.getMarca());

		// Modificando alguns atributos usando setters
        meuCarro.setMarca("Honda");
	
		// Exibindo os valores atualizados
		System.out.println("Marca atualizada: " + meuCarro.getMarca());
	}
}
```
***


