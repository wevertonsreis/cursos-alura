# Docker: Criando containers sem dor de cabeça

## 3. Usando volumes

### Anotações

Criando um container com um volume:

    docker run -v "/var/www" ubuntu

Criando um container com um volume definindo a pasta na maquina:
(O `-it` trata-se da execução do container em modo interativo)

    docker run -it -v "C:\Users\Weverton\Desktop:/var/www" ubuntu

Inspecionando o container:

    docker inspect ID_DO_CONTAINER

Criando um container com uma imagem do node

    docker run node

Criando um container com uma imagem do node e executando um comando

    docker run node npm -version

Criando um container com uma imagem node e um volume para colocar o código fonte a ser executado

    docker run -v "C:\Users\Weverton\Desktop\volume-exemplo:/var/www" node npm start

Criando um container com uma imagem node e um volume para colocar o código fonte a ser executado e definindo o (Working Directory) com o comando `-w` 

    docker run -v "C:\Users\Weverton\Desktop\volume-exemplo:/var/www" -w "/var/www" node npm start

Definindo a porta

    docker run -p 8080:3000 -v "C:\Users\Weverton\Desktop\volume-exemplo:/var/www" -w "/var/www" node npm start

