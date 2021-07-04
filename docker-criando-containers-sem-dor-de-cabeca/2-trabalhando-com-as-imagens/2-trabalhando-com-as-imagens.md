# Docker: Criando containers sem dor de cabeça

## 2. Trabalhando com as imagens

### Anotações

Ver todos os containers ativos:

    docker ps

Ver todos os containers já criados:

    docker ps -a

Executar um comando dentro do container:

    docker run ubuntu echo "Ola Mundo"

Utilizando o terminal do container:

    docker run -it ubuntu

Remover um container:

    docker rm ID_DO_CONTAINER

Iniciar um container:

    docker start ID_DO_CONTAINER

Parar um container:

    docker stop ID_DO_CONTAINER
    docker stop NOME_DO_CONTAINER

Permite remover todos os container inativos de uma só vez:

    docker container prune

Executar o container e não atrelar o seu terminal ao nosso:

    docker run -d dockersamples/static-site

O `-P` vai fazer o docker atribuir uma porta aleatória para ser possivel a comunicação com o container:

    docker run -d -P dockersamples/static-site

O `-p PORTA_MUNDO_EXTERNO:PORTA_CONTAINER` vai fazer o docker atribuir essa porta especifica para o comunicação com o container:

    docker run -d -p 12345:80 dockersamples/static-site

Ver informações das portas do container:

    docker port ID_DO_CONTAINER

Nomear um container:

    docker run -d -P --name meu-site dockersamples/static-site

Atribuir uma variável de ambiente para o container:

    docker run -d -P -e AUTHOR="Weverton Reis" dockersamples/static-site

Consultar os ids dos container que estão sendo excutado no momento:

    docker ps -q

Parando varios container com interpolação de comandos:

    docker stop $(docker ps -q)