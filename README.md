# Sistema Bancário em Python

## Descrição

Este é um sistema bancário simples desenvolvido em Python. O sistema permite realizar operações básicas como **depositar**, **sacar**, **exibir extrato**, **criar usuário** e **abrir conta**. Recentemente, o código foi refatorado para utilizar o conceito de **classes** para uma melhor organização e estruturação.

## Funcionalidades

- Depósito em conta
- Saque com limite diário
- Exibição de extrato bancário
- Criação de novos usuários
- Criação de contas bancárias
- Listagem de contas criadas

## Melhorias Implementadas

### 1. **Uso de Classes**
Anteriormente, o sistema utilizava apenas funções isoladas. Agora, a lógica do sistema foi encapsulada dentro de uma **classe** chamada `Banco`. Isso traz as seguintes vantagens:

- **Organização**: O código está mais modular e fácil de manter, com todos os métodos e atributos relacionados às operações bancárias agrupados.
- **Reuso**: Facilita a criação de instâncias do sistema para cenários de testes ou extensões do código.
- **Escalabilidade**: Torna mais fácil adicionar novas funcionalidades no futuro, como empréstimos ou investimentos.

### 2. **Encapsulamento de Dados**
Variáveis como saldo, extrato, limite de saques, usuários e contas foram movidas para atributos da classe `Banco`. Isso permite que o estado da aplicação seja mantido dentro de um objeto, evitando a necessidade de passar múltiplas variáveis entre funções.

### 3. **Métodos da Classe**
Os métodos que representam as funcionalidades do sistema foram convertidos em **métodos da classe** `Banco`. Isso torna o código mais intuitivo, pois as operações agora fazem parte da entidade "Banco", ao invés de serem funções soltas no escopo global.

- `depositar(self, valor)`
- `sacar(self, valor)`
- `exibir_extrato(self)`
- `criar_usuario(self)`
- `criar_conta(self)`
- `listar_contas(self)`

### 4. **Separação de Responsabilidades**
Cada funcionalidade do sistema foi mantida em métodos distintos, respeitando o princípio de **responsabilidade única**. Isso melhora a legibilidade e facilita testes e depurações.

### 5. **Facilidade de Execução**
A refatoração permite que o sistema seja instanciado e executado de forma simples, criando uma instância do objeto `Banco` e chamando o método `executar()` para iniciar o menu de operações.

### 6. **Código Mais Limpo**
O uso de classes e métodos auxiliares, como `filtrar_usuario`, ajuda a deixar o código mais conciso e claro, tornando mais fácil entender cada parte do sistema.
