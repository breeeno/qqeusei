## Heroku

Heroku, um serviço feito para hospedar sites feitos em diversas tecnologias, que permite a hospedagem de sites gratuitamente

------

Relativamente fácil de usar, tudo começa com a instalação da [linha de comando](https://devcenter.heroku.com/articles/heroku-cli#install-the-heroku-cli).

Após instalar o CLI e criar a conta no serviço, você deve navegar até o diretório do seu projeto e usar o comando ``heroku apps:create NOME DA SUA APP``

Dessa maneira, o CLI irá dar inicio na sua aplicação, também é interessante ressaltar a utilidade do ``Procfile``

Esse arquivo é o arquivo responsável por mandar os comandos necessários no deploy da sua app. 
Em um projeto em Django por exemplo, talvez se faça necessário a realização de migrações para o banco de dados, então dentro do arquivo você usaria o comando ``release:python manage.py migrate``

Caso seja necessário mais que um comando, você pode usar ```&&``` entre o nome dos comandos para que ele os execute simultamente no servidor do heroku.

Também é necessário a configuração de keys e tokens da sua aplicação, que são dados sensíveis que não devem ser deixados no código fonte da sua aplicação. Nesse caso se faz necessário o uso do comando ``heroku config:set NOME_DA_CHAVE=VALOR_DA_CHAVE``

Com isso dito, você possivelmente já conseguiria fazer deploy da sua app, inclusive é válido ressaltar que você também pode realizar várias operações no Heroku pela página da sua app.