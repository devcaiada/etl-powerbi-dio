# Processando e Transformando Dados com Power BI

Desafio de processamento e tratamento de dados utilizando Power BI e SQL.


**[ O Desafio](https://academiapme-my.sharepoint.com/:w:/g/personal/renato_dio_me/EVxAxO7akV5FoNy3mOk_3QwB3wKeyXMaFUi3ekTLQkY_sA?rtime=DrTvNZ5Y3Eg)**

Foi criada uma instância no **Microsoft Azure**, onde criei um serviço SQL para criar o banco de dados. Ao criar o banco foi necessário a conexão do mesmo junto ao **Power BI**.

Após a criação tive que importar o banco de dados para o Power BI, que exigiu a instalação de um conector MySQL antes da importação. No link "Saiba mais" no próprio Power BI Desktop ele me direcionou para uma página da Oracle.
Tive que criar uma conta na Oracle para poder baixar o conector, por isso deixei o instalador [nesse repositório](https://github.com/devcaiada/etl-powerbi-dio/tree/main/MySQL%20Connector).

![report](https://github.com/devcaiada/etl-powerbi-dio/blob/main/git/images/Report.png?raw=true)

Mesclar
Funciona como um join no sql. Ele usa uma coluna em comum para mesclar as tabelas.

Acrescentar
Ele acrescenta uma tabela na outra sem a necessidade de uma coluna em comum.
