O modificador de acesso **private** é o mais restritivo de todos. Uma classe, atributo ou método declarado como private só pode ser acessado dentro da própria classe. Ou seja, ele possui visibilidade restrita e não pode ser utilizado por outras classes. Por exemplo:
```cpp
public class Conta {

  private double saldo;

  private void sacar(double valor) {
    // lógica de saque...
  }
}
```
```typescript
public class Principal {

    public static void main(String[] args) {
        Conta c1 = new Conta();
        c1.saldo = 300;
        c1.sacar(100);
    }

}
```
No código anterior, vai ocorrer erro de compilação na classe `Principal`, pois o atributo `saldo` e o método `sacar` foram declarados como private, não podendo com isso serem acessados de fora da própria classe `Conta`.
