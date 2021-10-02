2021.10.02

Docker version : 20.10.8  
Ruby version : 3.0.2  
Rails version : 6.1.4  
mysql : 8.0

step1 : create

> docker-compose.yml  
> Dockerfile  
> Gemfile  
> Gemfile.lock

step2 : rails new

> command:
>
> > `docker-compose run web rails new . --force --database=mysql`

step3 : modify config/database.yml

> \- password:  
> \+ password: password
>
> \- host: localhost  
> \+ host: db

step4 : (may be needed)

> command:
>
> > `cd ./`

step5 : build

> command:
>
> > `docker-compose build`

step6 : db:create

> command:
>
> > `docker-compose run web rails db:create`

step7 : up

> command:
>
> > `docker-compose up`

access localhost:3000
