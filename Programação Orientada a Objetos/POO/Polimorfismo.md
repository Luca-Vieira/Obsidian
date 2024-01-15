***
Polimorfismo é um conceito da Programação Orientada a Objetos ([[POO]]) que se refere à capacidade de um [método](Métodos) ou [objeto](Objetos) se comportar de maneiras diferentes, dependendo do contexto ou da [classe](Classes) a que pertence. Existem dois tipos principais de polimorfismo: polimorfismo de tempo de execução (dinâmico) e polimorfismo de tempo de compilação (estático).
***
## Polimorfismo de Tempo de Execução (Dinâmico)
***
Ocorre quando o comportamento exato de um [método](Métodos) só é determinado em tempo de execução. Isso é geralmente alcançado através de sobrescrita de métodos em [subclasses](Classes#Subclasses).
```java
class Animal {
    void emitirSom() {
        System.out.println("Algum som");
    }
}

class Cachorro extends Animal {
    @Override
    void emitirSom() {
        System.out.println("Au au");
    }
}

class Gato extends Animal {
    @Override
    void emitirSom() {
        System.out.println("Miau");
    }
}

// Em outro lugar do código
// O método `emitirSom` tem comportamentos diferentes dependendo do tipo real de `Animal` (Cachorro ou Gato).
Animal meuAnimal = new Cachorro();
meuAnimal.emitirSom(); // Imprime "Au au"
meuAnimal = new Gato();
meuAnimal.emitirSom(); // Imprime "Miau"

```
***
## Polimorfismo de Tempo de Compilação (Estático)
***
Este tipo de polimorfismo é alcançado através do sobrecarregamento de [métodos](Métodos) (overloading), onde o mesmo nome de [método](Métodos) é usado com diferentes parâmetros em uma mesma [classe](Classes).
```java
class Calculadora {
    int soma(int a, int b) {
        return a + b;
    }

    double soma(double a, double b) {
        return a + b;
    }
}

// Em outro lugar do código
Calculadora calc = new Calculadora();
// Usa o método soma(int, int)
System.out.println(calc.soma(5, 3)); 
// Usa o método soma(double, double)
System.out.println(calc.soma(5.0, 3.0));
//O método `soma` é sobrecarregado com diferentes tipos de parâmetros, permitindo comportamentos diferentes dependendo dos tipos dos argumentos passados.
```
***