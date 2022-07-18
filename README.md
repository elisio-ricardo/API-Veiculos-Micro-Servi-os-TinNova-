# API-Veiculos-Micro-Serviços-TinNova
API de veiculos criada em Java com arquitetura de Micro Serviços

Onde Sua principal função é gerar um CRUD de veiculos e fazer filtros dos veiculos, como quantidade por marca, quantidade por decada,
filtro por marca, ano e cor.

Foi Desenvolvida em Micro-serviços  a arquitetura mais utilizada atualmente.

# Ordem de inicialização de Serviços

1° startar o serviços naming-service
2° startar o serviços apigateway
3° startar o serviços teste-api-veiculos

# Banco de Dados

Foi utilizado o banco de dados em Memoria h2

http://localhost:8080/h2-console
 
 username: sa
 
 password: password

# Documentação Swagger

http://localhost:8080/swagger-ui/index.html

# Rotas para teste no postman ou similar

## Rota para o Eureka

Abre a pagina de status do Eureka

localhost:8761

## Rota para post/getAll
localhost:8765/veiculo

## Rota para getAll com os filtros

Esses parametros são opcionais, porem o filtro só é feito quando enviar todos os tres, se faltar algum sera feito um getAll sem filtro.

localhost:8765/veiculo?marca={marca}&ano={ano}&cor={cor}

## Rota para getFindById / delete / put / patch 
localhost:8765/veiculo/{id}

## Rota para executar o filtro de quantidade não vendida
localhost:8765/veiculo/naovendido


## Rota para executar o filtro de quantidade de veiculos por cada fabricante
localhost:8765/veiculo/marca


## Rota para executar o filtro de quantidade de veiculos por cada decada
localhost:8765/veiculo/decada

## Rota para executar o filtro de quantidade de veiculos adicionada no ultima semana
localhost:8765/veiculo/ultimasemana




