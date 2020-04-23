# Data Lakehouse na prática
Repositório com os dados da talk sobre data lakehouse, realizada no dia 22/04, apresentação disponível no link: https://www.youtube.com/watch?v=N8laLqERi8w


## Como "instalar" a demo

Esta demo roda no databricks community edition, que provê um cluster gratuito de Spark para a execução de notebooks, siga os passos abaixo para criar uma conta community e importar os notebooks para o ambiente

* Crie uma conta em https://community.cloud.databricks.com/

* Após a conta criada, faça o login

* Clique no botão Workspace e ele abrirá uma aba a esquerda, na parte superior aperte o botão à direita da palavra "Workspace" e seleciona a opção "import"

* Clique em browse ou arraste o arquivo demo_delta.dbc para a caixa e clique no botão importa

## Como executar a demo

* Caso você já use a versão community, recomendo que seja executado o notebook `cleanup_resources`, para limpar os recursos que são usados pela demo

* Para o notebook `dim_operador`, recomendo que se realize um fork do projeto no Github e mude o caminho do arquivo `operators.csv` para o caminho *raw* do arquivo no fork

* Execute o notebook `dim_operador`,  ele irá criar a dimensão operador. Após a primeira execução altere o arquivo `operators.csv` e rode o notebook `dim_operador` novamente, você verá que a dimensão operador receberá as alterações que foram feitas no arquivo, também será possível utilizar a funcionalidade *Time Travel*, que está logo mais abaixo no mesmo notebook

* Execute o notebook `gera_chamadas`, ele irá começar a produzir dados de chamadas na pasta de entrada

* Execute o notebook `fat_chamada`, este notebook irá criar o fato chamada e irá carregar a tabela em tempo real.

