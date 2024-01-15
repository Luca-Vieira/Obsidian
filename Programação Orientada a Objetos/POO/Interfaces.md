***
Interfaces, em Programação Orientada a Objetos ([[POO]]), são estruturas que definem um "contrato" que as [classes](Classes) devem seguir. Uma interface declara métodos, mas não os implementa. As [classes](Classes) que implementam uma interface devem fornecer uma implementação concreta para todos os [métodos](Métodos) declarados na interface.
***
## Exemplo em [[Java]]
***
```java
// Definição da interface
interface Animal {
    void emitirSom();
}

// Classe que implementa a interface
class Cachorro implements Animal {
    public void emitirSom() {
        System.out.println("Au au!");
    }
}

class Gato implements Animal {
    public void emitirSom() {
        System.out.println("Miau!");
    }
}

// Em outro lugar do código
public class Main {
    public static void main(String[] args) {
        Animal meuCachorro = new Cachorro();
        Animal meuGato = new Gato();

        meuCachorro.emitirSom(); // Imprime "Au au!"
        meuGato.emitirSom(); // Imprime "Miau!"
    }
}
```
***
Neste exemplo, `Animal` é uma interface que declara um [método](Métodos) `emitirSom`. As [classes](Classes) `Cachorro` e `Gato` implementam a interface `Animal`, o que significa que ambas as [classes](Classes) devem fornecer uma implementação específica para o  [método](Métodos) `emitirSom`. Isso garante que qualquer [classe](Classes) que implemente `Animal` terá um [método](Métodos) `emitirSom`, promovendo a consistência e a previsibilidade no código.
***
## Usos
***
- Definir um conjunto de [métodos](Métodos) que várias [classes](Classes) podem compartilhar.
- Promover a separação entre o que um [objeto](Objetos) faz e como ele faz.
- Facilitar a implementação de funcionalidades em diferentes [classe](Classes) sem se preocupar com a estrutura interna de cada uma.
- Permitir a programação voltada para interfaces, o que pode aumentar a flexibilidade e a capacidade de manutenção do código.
***
