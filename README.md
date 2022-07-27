## Build e execução do projeto

docker-compose up

## Build do projeto quando não houver docker-compose (executar toda vez que houver mudanças nos parâmetros do docker)

docker build -t nome-do-projeto .

## Executando o projeto quando não houver docker-compose (Criando a imagem)

docker run -p 3000:3000 nome-do-projeto

## Volumes: Serve para sincronizar arquivos e pasta do host (máquina) com o contêiner que está executando a aplicação (quando não houver docker-compose)

docker run -it -p 3000:3000 -v ${pwd}:/home/node/app nome-do-projeto

## Entrypoint personalizado: Executar apenas uma vez na linha de comando para evitar acesso negado

chmod +x .docker/entrypoint.sh

# Entrar no container

docker-compose exec app bash
