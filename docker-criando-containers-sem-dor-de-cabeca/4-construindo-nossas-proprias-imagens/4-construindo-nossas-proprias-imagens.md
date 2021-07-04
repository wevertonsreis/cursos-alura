# Docker: Criando containers sem dor de cabeça

## 3. Construindo nossas próprias imagens

### Anotações

Definindo a imagem base para a nossa, utilizando a ultima versão disponivel:

    FROM node:latest

Cria uma imagem a partir de um Dockerfile:

    docker build -f Dockerfile

Constrói e nomeia uma imagem não-oficial informando o caminho para o Dockerfile:

    docker build -f CAMINHO_DOCKERFILE/Dockerfile -t NOME_USUARIO/NOME_IMAGEM

Inicia o processo de login no Docker Hub:

    docker login 

Envia a imagem criada para o Docker Hub:

    docker push NOME_USUARIO/NOME_IMAGEM

Baixa a imagem desejada do Docker Hub:

    docker pull NOME_USUARIO/NOME_IMAGEM 