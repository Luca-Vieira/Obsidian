***
Na programação orientada a objetos ([[POO]]), os [atributos](Atributos) de visibilidade (também conhecidos como modificadores de acesso) são usados para definir como os membros de uma classe (como [atributos](Atributos) e [métodos](Métodos)) podem ser acessados e modificados. Eles são fundamentais para o conceito de encapsulamento, ajudando a proteger os dados e a manter a integridade do [objeto](Objetos). O encapsulamento em [[POO]] é uma técnica que envolve o agrupamento seguro de dados ([atributos](Atributos)) e código ([métodos](Métodos)) dentro de uma [classe](Classes) e a restrição do acesso direto a esses componentes, promovendo uma [interface](Interfaces) pública clara e segura. Isso permite um controle mais rigoroso sobre como os dados são acessados e modificados, protegendo-os contra alterações indevidas e garantindo um maior grau de segurança e integridade do código.
***
## Definições
***
- **Public**: Quando um membro é declarado como `public`, ele pode ser acessado de qualquer outra [classe](Classes). Isso significa que não há restrições de acesso a esses membros.
```java
public class ExemploPublic {
    public int numeroPublico;

    public void metodoPublico() {
        // Código aqui
    }
}
```
***
- **Private**: Membros marcados como `private` são acessíveis apenas dentro da própria [classe](Classes) em que estão declarados. Isso é usado para ocultar os detalhes internos da implementação da [classe](Classes) e é uma prática comum para proteger o estado interno do objeto.
```java
public class ExemploPrivate {
    private int numeroPrivado;

    private void metodoPrivado() {
        // Código aqui
    }
}
```
***
- **Protected**: Um membro declarado como `protected` pode ser acessado dentro de sua própria [classe](Classes), em [classes](Classes) localizadas no mesmo pacote, e também em subclasses. Isso é útil quando você quer permitir que uma [classe](Classes) herdada acesse o membro, mas protegê-lo de um acesso mais amplo.
```java
public class ExemploProtected {
    protected int numeroProtegido;

    protected void metodoProtegido() {
        // Código aqui
    }
}
```
***
- **Default (Package-Private)**: Quando nenhum modificador de acesso é especificado, o membro tem visibilidade de pacote (`default`). Isso significa que ele só pode ser acessado dentro de outras [classes](Classes) no mesmo pacote. Esse nível de visibilidade é menos comum, mas pode ser útil em certas situações para agrupar [classes](Classes) relacionadas dentro do mesmo pacote.
```java
class ExemploDefault {
    int numeroDefault;

    void metodoDefault() {
        // Código aqui
    }
}
```
***
| Visibilidade | Classe | Pacote | Subclasse | Todos | 
|--------------|--------|---------|------------|--------|
| Public          | [ X ]    | [ X ]      | [ X ]          | [ X ]    | 
| Protected    | [ X ]    | [ X ]      | [ X ]          |           | 
| Default        | [ X ]    | [ X ]      |                 |           | 
| Private         | [ X ]    |             |                 |           | 
***


