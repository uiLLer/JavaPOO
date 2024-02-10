O modificador de acesso **public** é o mais permissivo de todos. Uma classe, atributo ou método declarado como public pode ser acessado por qualquer classe em qualquer pacote. Ou seja, ele possui visibilidade pública e pode ser utilizado livremente. Por exemplo:
```cpp
public class Conta {

  public double saldo;

  public void sacar(double valor) {
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