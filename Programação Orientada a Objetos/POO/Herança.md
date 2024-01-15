***
A herança em Programação Orientada a Objetos ([[POO]]) é um princípio fundamental que permite a uma [classe](Classes) herdar [atributos](Atributos) e [métodos](Métodos) de outra [classe](Classes). Este conceito é importante para a reutilização de código, a eficiência e a organização hierárquica em programação.
***
## Definição e Usos
***
Herança permite que uma  [classe](Classes) (chamada de [subclasse](Classes#Subclasses) ou  [classe](Classes)  filha) adquira as propriedades e comportamentos de outra [classe](Classes) (conhecida como superclasse ou  [classe](Classes) pai). Isso significa que a [subclasse](Classes#Subclasses) contém os [atributos](Atributos) e [métodos](Métodos) da superclasse, além de seus próprios.
***
- **Reutilização de Código:** `você pode escrever o código comum na superclasse e depois herdar na subclasse`
***
- **Relação "É um":** `Carro é um Veículo.`
***
- **Sobrescrita de [[Métodos]]:** `Uma subclasse pode definir seu próprio comportamento para esses métodos.`
***
- **[[Encapsulamento]] e [[Polimorfismo]]:** `O encapsulamento protege os dados internos de uma classe e o polimorfismo permite que um método tenha várias formas.
***
- **Herança Múltipla e Simples:** `Herança múltipla permite que uma classe herde de várias superclasses, já herança simples permite que uma classe possa herdar de apenas uma superclasse.`
***
- **Hierarquia de [[Classes]]:** `A herança cria uma hierarquia entre classes. Isso pode ser visualizado como uma estrutura de árvore, onde a superclasse está no topo e as subclasses estão abaixo dela.`
***
- **[Abstract Classes](Abstração) e [[Interfaces]]:** `Existem classes abstratas e interfaces que podem ser usadas para definir métodos que devem ser implementados pelas subclasses.`
***
## Exemplo em [[Java]]
***
Nesse exemplo iremos usar a [Classe](Classes) ``Carro`` para demonstrar os [atributos](Atributos) e os [métodos](Métodos)
***
```java
// Classe base Carro já fornecida
public class Carro {
    // ... [atributos e métodos da classe Carro]
    // Como já fornecido anteriormente
}

// Subclasse CarroEletrico que herda de Carro
public class CarroEletrico extends Carro {

    // Atributo adicional específico para CarroEletrico
    int autonomiaBateria;

    // Construtor de CarroEletrico
    public CarroEletrico(String marca, String modelo, String cor, int ano, int autonomiaBateria) {
        // Chama o construtor da classe pai (Carro)
        super(marca, modelo, cor, ano); 
        this.autonomiaBateria = autonomiaBateria;
    }

    // Método específico para CarroEletrico
    public void carregarBateria() {
        System.out.println("Carregando a bateria do carro elétrico!");
    }

    // Sobrescrita do método exibirInformacoes
    @Override
    public void exibirInformacoes() {
        // Chama o método da classe pai
        super.exibirInformacoes();
        System.out.println("Autonomia da Bateria: " + autonomiaBateria + " km");
    }
}

public class Main {
    public static void main(String[] args) {
        // Criando um objeto da classe CarroEletrico
        CarroEletrico meuCarroEletrico = new CarroEletrico("Tesla", "Model S", "Branco", 2022, 500);
        // Chamando métodos do objeto meuCarroEletrico
	    meuCarroEletrico.exibirInformacoes();
	    meuCarroEletrico.ligar();
	    meuCarroEletrico.carregarBateria();

	    // Exemplo de como a herança permite usar métodos da classe pai
	    meuCarroEletrico.setMarca("Nissan");
	    System.out.println("Marca atualizada:"+meuCarroEletrico.getMarca());
}

```