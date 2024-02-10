No Java, a herança é realizada através da palavra-chave **extends**. A [[Classe]] que herda é chamada de **subclasse**, e a classe que é herdada é chamada de **superclasse**. A subclasse pode acessar todos os atributos e métodos públicos e protegidos da superclasse, além de poder sobrescrever os métodos da superclasse para criar comportamentos específicos
exemplificando: 
```java
// src > br.com.alura.screenmatch.modelos > Serie.java

package br.com.alura.screenmatch.modelos;

public class Serie extends Titulo {
    private int temporadas;
    private boolean ativa;
    private int episodiosPorTemporada;
    private int minutosPorEpisodio;
}
```
Nossa classe `Serie` está herdando todos os atributos e métodos da classe `Titulo`, com isso formando um novo padrão de construção das nossas classes. Um conceito que aplicaremos normalmente no desenvolvimento Java.