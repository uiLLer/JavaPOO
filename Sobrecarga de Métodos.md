Quando nós utilizamos como parâmetro de um [[Método]], um atributo de um [[Tipos Primitivos]]/[[Classe]] e podemos receber mais de um tipo e apresentamos a mesma funcionalidade. Podemos reescrever o mesmo método mudando o parâmetro, assim caracterizando a sobrecarga de métodos. exemplificando:

```java
// CalculadoraDeTempo.java

package br.com.alura.screenmatch.calculos;

import br.com.alura.screenmatch.modelos.Filme;
import br.com.alura.screenmatch.modelos.Serie;

public class CalculadoraDeTempo {
    private int tempoTotal = 0;

    public int getTempoTotal() {
        return this.tempoTotal;
    }

    public void inclui(Filme f) {
        this.tempoTotal += f.getDuracaoEmMinutos();
    }
	//Realizando a sobrecarga
    public void inclui(Serie s) {
        this.tempoTotal += s.getDuracaoEmMinutos();
    }
}
```

Nota-se que foi feito a reescrita do Método inclui, fazendo a troca do parâmetro `f` da classe `Filme`, pelo parâmetro `s` da classe `Serie`.

No entanto, essa não é a melhor forma de implementação desse conceito, porque foge do nossa melhor forma de desenhar nossas classes. Nota-se que as classes `Filme` e `Serie` são filhas da classe `Titulo` (no nosso exemplo), ou seja, se recebermos a classe `TItulo`, quer dizer que também recebemos `Filme` e `Serie`. Já que ambas são `Titulo`também por causa da herança.
exemplificando:
```java
// ...

public void inclui(Titulo t) {
    this.tempoTotal += t.getDuracaoEmMinutos();
}

// ...
```
Deve ser feito a correção dos imports(o atalho shitf + alt + O ajuda nesse caso no Intellij) e o método inclui apresentará a mesma funcionalidade do exemplo anterior, utilizando-se de uma menor quantidade de linhas e declarações; 