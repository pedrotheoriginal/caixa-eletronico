# 🏧 Simulador de Caixa Eletrônico em Python

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
* **Python** (Conceitos aplicados: Funções, Manipulação de Variáveis de Estado, Loops, Condicionais, Tratamento de Exceções e Formatação de Strings).

## 💻 Como executar o projeto na sua máquina

1. Certifique-se de ter o Python instalado no seu computador.
2. Clone este repositório ou baixe o arquivo `.py` do projeto.
3. Abra o terminal na pasta onde o arquivo está salvo.
4. Execute o comando:
   ```bash
   python caixa_eletronico.py
