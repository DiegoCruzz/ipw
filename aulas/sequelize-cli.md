# Roteiro de aula
## Criando o projeto
Para criar o seu projeto e conseguir usar o Sequelize como ORM para se comunicar com o banco de dados, você precisará usar o pacote `sequelize-cli` da seguinte forma.

1. Crie um novo diretório com o nome do seu projeto e inicialize um novo projeto Node usando o comando `npm init`.
2. Instale os pacotes `sequelize-cli` e `sequelize` com o comando `npm i sequelize sequelize-cli`.

Neste momento, você terá a seguinte estrutura de diretórios:
<pre>
projeto
 |- node_modules (pacotes instalados pelo NPM)
 |- package-lock.json
 |- package.json
</pre>

3. Agora você poderá rodar o comando `sequelize init` para inicializar o seu projeto. Você instalou o `sequelize-cli` localmente. Logo, precisará executar o seu binário (executável) para prosseguir. Os binários de pacotes Node.js ficam localizados no diretório `node_modules/.bin`. Para executar no Windows, digite no terminal `node_modules\.bin\sequelize init` e aperte Enter.

Foram criados alguns diretórios e agora você terá a seguinte árvore de diretórios:
<pre>
projeto
 |- config
 |- migrations
 |- models
 |- node_modules
 |- seeders
 |- package-lock.json
 |- package.json
</pre>

4. Neste momento, você precisará configurar o acesso ao banco de dados. Usaremos o banco de dados PostgreSQL. Certifique-se de ter seguido os passos listados [aqui](https://github.com/antoniojnr/ipw/blob/master/aulas/postgresql.md)
5. Com o usuário e base de dados criados, iremos inserir as configurações no arquivo `config/config.json`. O valor inserido em `username` é `ipw`, conforme definido nos passos de configuração; o valor de `password` é a senha que você inseriu para o usuário e o `database` é `ipw`. Descubra o IP da máquina usando `ip addr`. O IP deverá ser inserido em `hostname`. Finalmente, o `dialect` é `postgres`. Por enquanto, preencha apenas as configurações do ambiente `development`.

Suas configurações devem ficar como as listadas a seguir:
<pre>
"development": {
  "username": "ipw",
  "password": "[SUA SENHA]",
  "database": "ipw",
  "host": "[SEU IP]",
  "dialect": "postgres"
}
</pre>