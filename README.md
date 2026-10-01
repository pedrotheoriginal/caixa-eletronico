# Simulador de Caixa Eletrônico em Python 🏧

Projeto desenvolvido para praticar o gerenciamento de estado (variáveis), loops de repetição (`while`), estruturas condicionais (`if/elif/else`), menus interativos e tratamento de erros (`try/except`) em Python.

## 💳 Sobre o Projeto

Este é um sistema simulador de um caixa eletrônico bancário. O programa apresenta um menu interativo onde o usuário pode consultar seu saldo atual, realizar saques (com validação de saldo disponível e valores válidos), efetuar depósitos e encerrar a sessão com segurança.

## 🚀 Funcionalidades

* **Consulta de Saldo:** Exibe o saldo atualizado da conta em tempo real com formatação monetária (R$).
* **Operação de Saque:** Verifica se o valor solicitado é menor ou igual ao saldo disponível e impede saques com valores negativos ou zerados.
* **Operação de Depósito:** Permite adicionar fundos à conta com validação de valores positivos.
* **Tratamento de Erros:** Protege o sistema contra entradas inválidas (caso o usuário digite texto em vez de números) sem quebrar a aplicação.
* **Menu Contínuo:** Mantém o sistema rodando em loop até que o usuário escolha explicitamente a opção de sair.

## 🛠️ Tecnologias Utilizadas
* **Python 3.x** (Conceitos aplicados: Funções, Manipulação de Variáveis de Estado, Loops, Condicionais, Tratamento de Exceções e Formatação de Strings).

## 💻 Exemplo de Código em Destaque

Uma amostra da função principal que gerencia o estado do saldo fora do loop e processa as transações com segurança:

```python
def caixa_eletronico():
    saldo = 1000.0  # O saldo fica FORA do loop para não resetar a cada rodada!

    while True:
        print("\n--- Bem-vindo ao Caixa Eletrônico! ---")
        print("1. Ver saldo")
        print("2. Sacar dinheiro")
        print("3. Depositar dinheiro")
        print("4. Sair")
        
        opcao = input("Escolha uma opção: ").strip()

        if opcao == "1":
            print(f"\nSeu saldo atual é: R$ {saldo:.2f}")

        elif opcao == "2":
            try:
                valor_saque = float(input("\nDigite o valor que deseja sacar: R$ "))
                if valor_saque <= 0:
                    print("Valor inválido para saque.")
                elif valor_saque <= saldo:
                    saldo -= valor_saque
                    print(f"Saque realizado com sucesso! Novo saldo: R$ {saldo:.2f}")
                else:
                    print("Saldo insuficiente para realizar o saque.")
            except ValueError:
                print("Por favor, digite apenas números válidos.")

        elif opcao == "4":
            print("\nObrigado por usar o Caixa Eletrônico. Até logo!")
            break

        else:
            print("\nOpção inválida. Por favor, escolha uma opção entre 1 e 4.")
