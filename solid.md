# SOLID

## S - Single Responsability

O princípio de responsabilidade única


## O - Open / Closed

O princípio do aberto e fechado

Os objetos devem estar abertos para extensão porém fechados para modificação

- Criação de uma interface para fazer o controle (ABSTRAÇÃO)

class Remuneracao {
    fun remuneracao();
}

class contratoClt : Remuneracao {
    override fun Remuneracao()
}

class folhaDePagamento {
    private saldo;
    fun calcular(contrato: Remuneracao) {
        // ....
    }
}

## L - LISKOV Substitution

O princípio de Liskov

Uma classe derivada desse ser substituivel por sua classe base

class A() {
    fun getNome() {
        println("Meu nome é A);
    }
}

class B() : A {
    override fun getNome() {
        println("Meu nome é B);
    }
}

class Main() {
    objetoA = new A();
    objetoB = new B();

    fun imprimirNomes(objeto: OBJETO) {
        objeto.getNome();
    }

    imprimirNome(objeto1); // Meu nome é A
    imprimirNome(objeto2); // Meu nome é B

}

## I - Interface Segregation

O princípio de segregação de interface

abstract class Aves() {
    fun setLocalizacao(longitude: Int, latidude: Int)
    fun renderizar()
}

// Criamos uma nova interface para validar as aves que conseguem voar das que não conseguem

class AvesqueVoam() : Aves {
    override fun setLocalizacao(longitude: Int, latidude: Int)
    override fun renderizar()
    fun setAltitude(altitude: Int) 
}

class Papagaio() : AvesqueVoam {
    override fun setLocalizacao(longitude: Int, latidude: Int)
    override fun renderizar()
    override fun setAltitude(altitude: Int) 
}

class Pinguim() : Aves() {
    override fun setLocalizacao(longitude: Int, latidude: Int)
    override fun renderizar()
}

## D - Dependency Inversion

O princípio de inversao de dependência

- Devemos depender de ABSTRAÇÕES e não de Implementações

- Módulos de alto nível não devem depender de módulos de baixo nível

- Abstração não deve depender de detalhes

- Detalhes deve depender de abstrações

