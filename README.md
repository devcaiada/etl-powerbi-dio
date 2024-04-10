# Processando e Transformando Dados com Power BI

Desafio de processamento e tratamento de dados utilizando Power BI e SQL.

**[ O Desafio](https://academiapme-my.sharepoint.com/:w:/g/personal/renato_dio_me/EVxAxO7akV5FoNy3mOk_3QwB3wKeyXMaFUi3ekTLQkY_sA?rtime=DrTvNZ5Y3Eg)**

## Resolução

Foi criada uma instância no **Microsoft Azure**, onde criei um serviço SQL para criar o banco de dados. Ao criar o banco foi necessário a conexão do mesmo junto ao **Power BI**.

Após a criação tive que importar o banco de dados para o Power BI, que exigiu a instalação de um conector MySQL antes da importação. No link "Saiba mais" no próprio Power BI Desktop ele me direcionou para uma página da Oracle.
Tive que criar uma conta na Oracle para poder baixar o conector, por isso deixei o instalador [nesse repositório](https://github.com/devcaiada/etl-powerbi-dio/tree/main/MySQL%20Connector).

## Relatório Empresarial

![report](https://github.com/devcaiada/etl-powerbi-dio/blob/main/git/images/R.png?raw=true)

## Tratamento de Dados

Com o banco já conectado ao Power BI foi necessário tratar algumas informações, como funcionários sem gerentes, valores nulos, mesclar e separar tabelas para facilitar a criação de um relatório claro e coerente.

![tratamento](https://github.com/devcaiada/etl-powerbi-dio/blob/main/git/images/nome%20-%20endereco.png?raw=true)

O endereço dos funcionários estava todo alocado em uma única célula como string. Eu separei todas as informações em colunas exclusivas para facilitar a compreensão. Também juntei as colunas first name e last name para termos uma única coluna nome, facilitando a exibição das legendas nos gráficos.

![dinamico](https://github.com/devcaiada/etl-powerbi-dio/blob/main/git/images/Dinamix.png?raw=true)

Como podemos ver na imagem acima, temos algumas infoomações bem definidas, como a quantidade de funcionários por sexo, a quantidade de funcionários administrados por gerentes, bem como os respectivos salários e a quantidade de unidades por cidade.

## Mesclar e Acrescentar Colunas

O desafio solicita ainda que mesclemos a tabela departamentos com a de localização, para obtermos o número de departamentos por região, conforme exibição no gráfico **Empresas por Cidade**. Nesse caso a mesclagem é essencial, uma vez que a função Acrescentar Coluna apenas iria adicionar as tabelas uma abaixo da outra, sem correlação entre ambas.

![mesclar](https://github.com/devcaiada/etl-powerbi-dio/blob/main/git/images/Mesclar.png?raw=true)

### Mesclar Colunas

Funciona como um join no sql. Ele usa uma coluna em comum para mesclar as informações das tabelas. Muito útil para conflitarmos dados.

### Acrescentar Colunas

Ele acrescenta uma tabela embaixo da outra sem a necessidade de uma coluna em comum. Isso pode dificultar a análise de algumas informações e até embaralhar alguns dados. Sendo útil apenas quando quisermos concatenar dados.

---
