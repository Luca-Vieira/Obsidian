***
Em programação orientada a objetos ([[POO]]), os métodos são como funções que estão associadas a uma [classe](Classes) ou a um [objeto](Objetos). Eles definem o comportamento ou ações que os [objeto](Objetos) dessa [classe](Classes) podem executar. Métodos são essenciais para a interação entre os [objeto](Objetos) e para manipular seus dados ([atributos](Atributos)). Vamos detalhar mais sobre métodos:
***
## Métodos comuns
***
- **Construtor**: inicializa o [objeto](Objetos) com valores específicos para os [atributos](Atributos).
- **Getters**: permitem acessar os valores dos [atributos](Atributos) [privados](Encapsulamento.md) da classe.
- **Setter**: são métodos que permitem modificar os valores dos [atributos](Atributos) [privados](Encapsulamento.md).
***
## Exemplo em [[Java]]
***
Nesse exemplo iremos usar a [Classe](Classes) ``Carro`` para demonstrar os [atributos](Atributos) e os métodos.

```java
	
	
	
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
	//Método para exibir os atributos do carro
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
```
***