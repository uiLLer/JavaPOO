Em Java, interfaces são uma forma de definir uma regra que as [[Classe]]s devem seguir. Ou seja, uma interface define quais [[Método]]s precisamos adotar na nossa classe implementada

Interfaces permitem que diferentes classes possam ser tratadas de maneira padronizada, via [[Polimorfismo]], tornando assim o código fácil de estender com novos comportamentos.

Para a criação de uma interface no Java, segue a mesma regras de criação de uma classe, trocando as palavras-chave `class` por `interface`.
exemplo de interface:
```Java
public interface Valido {

    boolean estaNaValidade();

}
```

Para implementar as regras de uma interface, utilizamos o mesmo conceito de [[Herança]], só que ao invés de utilizar a palavra-chave `extends`, utilizamos `implements`

```java
public class Documento implements Valido {

    private String Nome;
    private boolean anoVencimento;

    @Override
    public boolean estaNaValidade() {
        return this.anoVencimento >= 2024;
    }

    //getters e setters
}
```
Nota-se que conseguimos incorporar o método da nossa interface `Valido` e nisso devemos adicionar uma função para esse método, utilizando-se da [[Sobrescrita]].