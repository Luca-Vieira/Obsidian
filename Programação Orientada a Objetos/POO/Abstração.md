***
A abstração, no contexto da programação orientada a objetos ([[POO]]), é um princípio fundamental que envolve o foco nas características essenciais de um [objeto](Objetos), ignorando detalhes menos importantes ou irrelevantes para o contexto atual. Ela permite aos programadores criar modelos simplificados de entidades mais complexas do mundo real, concentrando-se apenas nos aspectos que são cruciais para a implementação de um determinado sistema ou aplicação. Vamos detalhar mais sobre a abstração:
***
1. **Essência sobre Detalhes**: Abstração significa representar entidades complexas de maneira simples. Em [[POO]], isso é feito através de [classes](Classes) que capturam características e comportamentos essenciais de um [objeto](Objetos), sem se ater a detalhes que não são necessários no contexto do programa.
***
2. **Modelagem do Mundo Real**: Abstração ajuda na modelagem de objetos do mundo real no software. Por exemplo, se você está criando um programa de simulação de veículos, sua [classe](Classes) `Carro` pode ter [atributos](Atributos) como `marca`, `modelo`, `velocidade` e [métodos](Métodos) como `acelerar()` ou `frear()`, sem necessariamente incluir detalhes menos relevantes para a simulação, como a cor do interior do carro.
***
3. **[[Classes]] e [[Interfaces]]**: Em [[POO]], as abstrações são frequentemente implementadas usando [classes](Classes) e [interfaces](Interfaces). As [interfaces](Interfaces), em particular, são uma forma pura de abstração, pois definem um contrato que outras [classes](Classes) podem implementar, sem fornecer a implementação dos [métodos](Métodos).
***
4. **Reutilização e Escalabilidade**: A abstração também promove a reutilização do código. Ao abstrair e encapsular características comuns em uma [classe](Classes) base ou [interface](Interfaces), é possível estender essas abstrações em [subclasses](Classes#Subclasses)) ou [classes](Classes) que implementam [interfaces](Interfaces), reutilizando funcionalidades e facilitando a manutenção e expansão do sistema.
***
5. **Redução de Complexidade**: Um dos principais benefícios da abstração é a redução da complexidade. Ao se concentrar apenas nos aspectos relevantes, a abstração torna o design e a compreensão do software mais gerenciáveis.
***
## Exemplo em [[Java]] de uma Abstract Class
***
Vamos criar uma [classe](Classes) abstrata chamada `Animal` e uma [subclasse](Classes#Subclasses) concreta chamada `Cachorro`. A [classe](Classes) `Animal` terá um [método](Métodos) abstrato `emitirSom`, que será implementado de forma específica na [subclasse](Classes#Subclasses) `Cachorro`.
***
```java
// Classe abstrata Animal. Esta classe é abstrata e contém um método abstrato `emitirSom`. Como é abstrata, não é possível criar instâncias diretas de `Animal`.
public abstract class Animal {
    
    // Método abstrato emitirSom
    public abstract void emitirSom();
}

// Classe concreta Cachorro que herda de Animal. Esta classe herda de `Animal` e fornece uma implementação específica para o método abstrato `emitirSom`.
public class Cachorro extends Animal {

    // Implementação do método emitirSom para Cachorro
    @Override
    public void emitirSom() {
        System.out.println("Au au!");
    }
}

public class Main {
    public static void main(String[] args) {
        // Criando um objeto da classe Cachorro
        Cachorro meuCachorro = new Cachorro();

        // Chamando o método emitirSom
        meuCachorro.emitirSom(); // Imprime: Au au!
    }
}

```
***
Este exemplo ilustra o conceito básico de [classes](Classes) abstratas em [[Java]] e como elas podem ser usadas para definir um contrato (na forma de [métodos](Métodos) abstratos que as [subclasses](Classes#Subclasses) devem cumprir. Cada [subclasse](Classes#Subclasses) que herda da [classe](Classes) abstrata deve fornecer sua própria implementação para os [métodos](Métodos) abstratos.
***
