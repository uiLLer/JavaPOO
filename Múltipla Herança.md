Em Java, é importante notar que a [[Herança]] múltipla não é permitida. A herança múltipla ocorre quando uma subclasse herda de duas ou mais superclasses.
Entretanto, é possível criar uma hierarquia de classes utilizando herança, simulando com isso uma herança múltipla. Por exemplo:
```kotlin
public class Conta {
  //codigo da classe omitido
}
```
```java
public class ContaCorrente extends Conta {
  //codigo da classe omitido
}
```
```java
public class ContaCorrentePessoaFisica extends ContaCorrente {
  //codigo da classe omitido
}
```
No código anterior, a classe `ContaCorrentePessoaFisica` está herdando de `ContaCorrente`, que por sua vez herda da classe `Conta`, ou seja, indiretamente a classe `ContaCorrentePessoaFisica` vai herdar de `Conta`, pois sua superclasse herda dela.