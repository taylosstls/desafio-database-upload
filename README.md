# 🚀 Desafio - Database Upload
**Quinto desafio da Rocketseat utilizando os conceitos de NodeJS junto com Typescript, desenvolvendo a aplicação do banco de dados via TypeORM e envios de arquivos com o Multer**<br>
Os testes devem ser válidos utilizando o comando <code>"yarn test"</code><br>
Para startar a aplicação, devem ser criados 2 bancos de dados <code>"gostack_desafio06"</code> e <code>"gostack_desafio06_tests"</code>, no **prompt/cmd**, utilize o comando <code>"yarn typeorm migration:run"</code> e na sequência <code>"yarn dev:server"</code>.

### O desafio é constituído nas seguintes etapas:
A aplicação deve armazenar transações financeiras de entrada e saída e permitir o cadastro e listagem das transações, além de permitir a criação de novos registros no banco de dados a partir do envio de um <code>arquivo csv</code>.
- <code>**Cadastrar e listar as entradas da API:**</code> Cadastrar uma lista com o id, nome, valor e tipo de entrada (income / outcome) e categoria.
- <code>**Não permitir duplicatas:**</code> Se o tipo de categoria já existir no banco de dados, o campo seja atribuído à transação com o id dessa categoria existente, não permitindo a duplicação de categorias.
- <code>**Rota de DELETE:**</code> Deve ter a possibilidade de deletar a transação e retornar uma resposta HTTP 204 (Status de Ok).
- <code>**Resgatar os valores e balanço de caixa:**</code> Agrupamento de valores em cada tipo de entrada e verificação do saldo.
- <code>**Permissão de transação:**</code> A transação somente pode ser permitida em 2 hipóteses: apenas se o <code>"type"</code> for do tipo _**income**_ ou _**outcome**_; e apenas se o saldo em caixa <code>(income)</code> for maior do que o saque/transação <code>(outcome)</code> deve retornar um erro HTTP 400.
- <code>**Upload de base CSV:**</code> Deve ser permitido a criação dos registros e categorias que estavam presentes no arquivo, e retornar as transactions importadas.
