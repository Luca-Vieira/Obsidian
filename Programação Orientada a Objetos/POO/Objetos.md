***
Em programação orientada a objetos ([[POO]]), um "objeto" é uma instância concreta de uma [classe](Classes). Uma [classe](Classes) funciona como um modelo ou um esboço, enquanto um objeto é uma entidade real construída com base nesse modelo. Cada objeto tem suas próprias características e comportamentos, definidos pelos [atributos](Atributos) e [métodos](Métodos) da [classe](Classes) da qual ele é instanciado.
***
## Exemplo em [[Java]]
***
Nesse exemplo iremos usar a [Classe](Classes) ``Carro`` para demonstrar os [atributos](Atributos) e os [métodos](Métodos)

```java
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
```

- **Instância de `Carro`**: `meuCarro` é um objeto da [classe](Classes) `Carro`. Ele é criado usando o [construtor](Métodos) `Carro(String marca, String modelo, String cor, int ano)` e inicializado com os [valores](Atributos) "Toyota", "Corolla", "Preto", e 2021.
- **Estado do Objeto**: O estado de `meuCarro` é definido pelos valores de seus [atributos](Atributos) (`marca`, `modelo`, `cor`, `ano`). Este estado pode ser lido (e potencialmente modificado) através dos [métodos getters e setters](Métodos).
- **Comportamento**: O objeto `meuCarro` tem comportamentos definidos pelos [métodos](Métodos) da [classe](Classes) `Carro`. Por exemplo, se houvesse um [método](Métodos) `ligarMotor()`, você poderia chamá-lo em `meuCarro` para simular o ato de ligar o motor do carro.
- **Identidade**: O objeto `meuCarro` tem uma identidade única no programa. Mesmo se criarmos outro objeto `Carro` com os mesmos valores de [atributos](Atributos), ele será um objeto diferente.
***