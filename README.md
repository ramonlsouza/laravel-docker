# Descrição
Setup de um ambiente de desenvolvimento Laravel (PHP) e MySQL utilizando docker.

# Dependências
Um projeto já iniciado com Laravel e as ferramentas docker e docker-compose

# Como utilizar
1. Copiar arquivos para dentro da pasta principal de um projeto Laravel
2. Copiar dump do banco de dados (arquivo com extensão .sql) para docker-compose/mysql/init_db.sql
3. alterar valor de DB_HOST no arquivo .env para DB_HOST=db
4. rodar o seguinte comando no terminal, dentro da pasta do projeto: docker-compose build app
5. iniciar os containers utilizando docker-compose: docker-compose up -d
6. instalar as dependências utilizando composer: docker-compose exec app composer install
7. criar uma nova chave de segurança utilizando artisan: docker-compose exec app php artisan key:generate

Para encerrar os containers, utilize o comando: docker-compose down
