***
Em programação orientada a objetos ([[POO]]), os atributos de uma [classe](Classes) são elementos que definem as características ou propriedades dos [objeto](Objetos) criados a partir dessa [classe](Classes). Eles são essencialmente variáveis que estão contidas dentro da [classe](Classes) e representam o estado de um [objeto](Objetos).
***
## Exemplo em [[Java]]
***
Nesse exemplo iremos usar a [Classe](Classes) ``Carro`` para demonstrar os atributos e os [métodos](Métodos).
***
```java
public class Carro {

    // Atributos da classe Carro
    String marca;
    String modelo;
    String cor;
    int ano;
    static int numModelos = 10;
    final int 
```
***
### Static
***
É um modificador que indica que um membro (seja método, variável ou bloco de código) pertence à classe em vez de a uma instância específica da classe.
***
### Final
***
É um modificador que, quando aplicado a uma variável, impede que seu valor seja alterado após a inicialização; quando aplicado a uma classe, impede que a classe seja herdada; e quando aplicado a um método, impede que o método seja sobrescrito por subclasses.
***
