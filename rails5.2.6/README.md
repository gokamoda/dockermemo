2021.10.02

Docker version : 20.10.8  
Ruby version : 2.5.9  
Rails version : 5.2.2  
mysql : 5.7

step1 : create
docker-compose.yml
Dockerfile
Gemfile
Gemfile.lock

step2 : rails new
command:
docker-compose run web rails new . --force --database=mysql --skip-bundle

step3 : modify config/database.yml

- password:

* password: password

- host: localhost

* host: db

step4 : build
command:
docker-compose build

step5 : db:create
command:
docker-compose run web rails db:create

step6 : up
command:
docker-compose up

access localhost:3000
