# RESOLUÇÃO EXERCÍCIO 05 (COMPLETO)

R= A resolução das questões (Questões 01 a 05 da parte 01, questão 01 da parte 02) referente ao banco estão no código: https://github.com/marciofleitao030609/exercicio05-poo-ifpi-2024.2/blob/main/questao-05-banco

A resolução da questão 01 da parte 02 está no código:

A resolução da questão 02 da parte 02 está no código: 

A resolução da questão 03 da parte 02 está no código: 

# Parte 01
Atualize a implementação das classes apresentadas em sala de acordo com as seguintes abaixo.

1) Classe Cliente
   
Crie uma classe Cliente com os seguintes atributos:
* id: Identificador único do cliente (número).
* nome: Nome completo do cliente (string).
* cpf: CPF único do cliente (string).
* dataNascimento: Data de nascimento do cliente (Date).
* contas: Array de contas associadas ao cliente.

2) Classe Conta

Atualize a classe Conta para incluir os seguintes atributos:

* id: Identificador único da conta (número).
* cliente: Cliente associado à conta.

3) Classe Banco
   
Atualize a classe Banco para incluir os seguintes atributos e métodos:

* clientes: Array de objetos do tipo Cliente, além do array de contas.

Além dos métodos já criados, crie também:

a) Adicionar cliente

* Método: inserirCliente(cliente: Cliente): void
* Insere o cliente passado por parâmetro no array de clientes.

b) Consultar cliente pelo CPF
* Método: consultarCliente(cpf: string): Cliente
* Retorne o cliente correspondente ao CPF;

c) Associar um cliente a uma conta
* Método: associarContaCliente(numeroConta: string, cpfCliente:
string): void
* Procure o cliente e a conta com os dados fornecidos e associe-os, respeitando considernado que o cliente não pode ter a mesma conta adicionada mais de uma vez.

d) Listar contas de um cliente
* Método: listarContasCliente(cpf: string): Conta[]
* Retorne todas as contas associadas ao cliente cujo CPF foi informado.

e) Totalizar saldo por cliente
* Método: totalizarSaldoCliente(cpf: string): number
* Calcule e retorne o saldo total de todas as contas de um cliente.

f) Incluir um cliente
* Método: inserirCliente(cliente: Cliente): void
* Adicione o cliente ao array de clientes, respeitando as seguintes regras:
* Não permitir que um cliente com o mesmo id ou cpf seja cadastrado mais de uma vez.

g) Alterar o método de incluir uma conta
* Método: inserirConta(conta: Conta): void
* Adicione a conta ao array de contas, não permitindo que uma conta com o mesmo id ou numero seja criada.

4) Regras de Negócio

a. Cada cliente pode ter várias contas, mas uma mesma conta não pode ser associada mais de uma vez ao mesmo cliente.

b. Cada conta só pode ser associada a um único cliente.

c. O sistema deve impedir duplicações:

i. Nenhum cliente pode ter o mesmo id ou cpf de outro cliente.

ii. Nenhuma conta pode ter o mesmo id ou numero de outra conta.

5) Realize testes em todos os métodos da classe Banco.

6) Questionamentos:

a. Você concorda que o banco faz o cadastro de duas entidades e ainda faz regras de negócios?

R= 

b. Não seria adequado o banco ter uma class CadastroDeClientes e CadastroDeContas e algumas regras de validação serem feitas no banco e deixar os métodos de consulta e inclusão os mais simples possíveis?

R= 

c. O método associar cliente a uma conta deveria estar em que classe? Banco, CadastroDeContas ou CadastroDeClientes?

R= 


# Parte 02
1. Atualize a implementação da classe Banco com os métodos apresentados em sala de aula:
a. Consultar por índice, excluir, atualizar, sacar, depositar e transferir apresentadas em sala. Nota: o transferir deve ter como parâmetros os dois números de conta, não os objetos e um valor a ser transferido conforme slide "Esqueleto" de um cadastro.

b. Crie um método transferir que recebe um array de contas destino e realiza transferências para cada uma delas;

c. Crie 3 métodos: um que retorne a quantidade de contas, outro que retorne o total de dinheiro depositado em todas as contas. Por fim, crie um método que retorne a média do saldo das contas chamando os dois métodos anteriores.

2. Crie uma implementação que simule um migroblog:
* Crie uma classe Postagem e nela:
   a. Crie os atributos:
      1. id do tipo number, representando o identificador da postagem;
  
      2. texto do tipo string, representando um texto da postagem;
  
      3. quantidadeCurtidas do tipo number;

b. Crie um método chamado curtir que incrementa a quantidade curtidas;

c. Crie um método chamado toString que retorna a concatenação da postagem com a quantidade de curtidas;

* Crie uma classe Microblog e nela:
   a. Crie um array de classes Postagem;
  
   b. Crie um método que inclua uma postagem passada como parâmetro no array de postagens;
  
   c. Crie um método de excluir uma postagem que recebe um id passado por parâmetro. Para isso, efetue uma busca pelo id nas postagens  do array e faça a exclusão de forma análoga à feita na classe Banco;

   d. Crie um método que retorna a postagem mais curtida;

   e. Crie um método curtir em que se passa um id como parâmetro e a classe microblog pesquisa a postagem e chama seu método curtir da própria postagem;

   f. Crie um método toString que retorna a concatenação do “toString” de todas as postagens.

3. Coloque as classes de Banco e Conta em um arquivo chamado banco.ts e faça as exportações necessárias. Crie um arquivo chamado app.ts que tenha leitura de dados e um loop semelhante ao demonstrado abaixo e implemente todas as funcionalidades da classe banco. Além de instalar a biblioteca prompt-sync, instale também a versão tipada dela: npm install @types/prompt-sync
