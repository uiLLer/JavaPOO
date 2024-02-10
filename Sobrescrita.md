Quando nós tratamos do conceito de [[Herança]], ás vezes queremos herdar [[Método]] de mesmo nome, mas com retornos diferentes. Nisso podemos aplicar uma sobrescrita, ou seja, mudar o retorno de um método na classe filha herdada da classe mãe/pai.
Utilizamos dos termos `@Override` antes de redeclarar o método, ex:

Antes:
```java
// Serie.java
// ...

@Override
public int getDuracaoEmMinutos() {
    return super.getDuracaoEmMinutos();
}

// ...
```

Depois: 
```java
// Serie.java
// ...

@Override
public int getDuracaoEmMinutos() {
    return temporadas * episodiosPorTemporada * minutosPorEpisodio;
}

// ...
```

O termo `super.` refere-se a um atributo/método da classe mãe, da classe "superior".
Vale notar que a anotação `@Override` era opcional. De fato, podemos removê-la da classe `Serie`, executar o projeto novamente e não haverá diferença no resultado.
Então, qual é a vantagem de escrevermos o `@override`? Se eventualmente o método for modificado na superclasse, a IDE exibirá um alerta se a classe que sobrescreve esse método deixar de funcionar.