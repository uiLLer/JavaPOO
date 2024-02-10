“this”, traduzindo para o português (Isto/este/esta), é usado para fazer referência aos atributos da classe, especialmente em [[Método]] que têm parâmetros com o mesmo nome do atributo da classe em que estamos trabalhando. 
por ex:
```typescript
public class Lampada {
    private boolean ligada;
    private String modelo;

    public void acendeLampada(boolean ligada) {
       this.ligada = ligada;
    }
}
```
Podemos concluir então que “this” se refere ao objeto atual e não ao parâmetro do método. É comum usarmos o `this` para eliminar essa confusão entre os atributos e parâmetros, sendo que ele não é uma exclusividade do Java, pois outras linguagens de programação orientadas a objetos também possuem esse recurso.