//1
fun main() {
    val palavra = "Universidade"

    for (letra in palavra) {
        if (letra.lowercaseChar() in "aeiou") {
            continue
        }

        print(letra)
    }
}

//2
fun main() {
    var numero = 1

    while (true) {
        if (numero % 7 == 0 && numero % 13 == 0) {
            println(numero)
            break
        }

        numero++
    }
}

//3
fun main() {
    var total = 0

    for (numero in 1..100) {
        if (numero % 10 == 0) {
            continue
        }

        total += numero

        if (total > 500) {
            break
        }
    }

    //4
    fun main() {
    var saldo = 1000.00
    val saque = 150.00

    while (true) {
        if (saldo >= saque) {
            saldo -= saque
            println("Saque realizado: R$ $saque")
            println("Saldo atual: R$ $saldo")
        } else {
            println("Saldo Insuficiente")
            break
        }
    }
}

    println("Total final: $total")

    //5

    fun main() {
    val alvo = 29
    var ehPrimo = true

    for (numero in 2 until alvo) {
        if (alvo % numero == 0) {
            ehPrimo = false
            break
        }
    }

    if (ehPrimo) {
        println("$alvo é um número primo.")
    } else {
        println("$alvo não é um número primo.")
    }
}

//6

fun main() {
    while (true) {
        println("===== MENU =====")
        println("1 - Opção 1")
        println("2 - Opção 2")
        println("3 - Opção 3")
        println("0 - Sair")
        print("Escolha uma opção: ")

        val opcao = readLine()?.toIntOrNull() ?: continue

        when (opcao) {
            1, 2 -> {
                println("Processando...")
            }

            3 -> {
                println("Módulo em manutenção")
                continue
            }

            0 -> {
                println("Encerrando o programa...")
                break
            }

            else -> {
                println("Opção inválida!")
            }
        }
    }
}

//7
fun main() {
    for (numero in 1..50) {
        if (numero % 10 == 7) {
            continue
        }

        println(numero)
    }
}
}

//8

fun main() {
    val senhaCorreta = "1234"

    for (tentativa in 1..5) {
        print("Digite a senha: ")
        val senha = readLine()

        if (senha == senhaCorreta) {
            println("Acesso concedido!")
            break
        } else {
            println("Senha incorreta!")

            if (tentativa == 3) {
                println("Cofre travado administrativamente")
                break
            }
        }
    }
}
