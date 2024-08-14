# Alura Food - Microsserviços com RabbitMQ

O Projeto Alura Food foi desenvolvido como parte da trilha "Microsserviços na prática: mensageria com RabbitMQ" da Alura. Este projeto tem como objetivo demonstrar a implementação de comunicação assíncrona entre microsserviços utilizando o RabbitMQ.

# Sobre

Neste curso, continuamos o desenvolvimento do projeto Alura Food, iniciado em treinamentos anteriores que focaram na comunicação síncrona usando o Spring Cloud OpenFeign. Aqui, exploramos as limitações dessa abordagem e como o RabbitMQ pode superar os desafios de comunicação em sistemas distribuídos.

# Tecnologias utilizadas

- Java 17
- Spring Boot 3
- Spring Cloud
- Spring Cloud OpenFeign
- RabbitMQ
- Docker

# Estrutura do Projeto

Este projeto está dividido em vários módulos, cada um representando um microsserviço específico:

    1. API Gateway
        O API Gateway serve como ponto de entrada para todas as requisições ao sistema. Ele roteia as requisições para os microsserviços apropriados e é configurado para descobrir automaticamente os serviços registrados no Eureka Server.
    2. Server Discovery
        O Server Discovery é responsável pelo registro e descoberta de microsserviços. Utilizando o Eureka Server, ele permite que os microsserviços se registrem e sejam descobertos dinamicamente pelo Gateway e por outros serviços.
    3. Pedidos
        O Microsserviço de Pedidos gerencia os pedidos realizados pelos clientes. Ele expõe uma API REST para criação, consulta e atualização de pedidos e inclui a integração com RabbitMQ para enviar detalhes do pedido a outros serviços.
    4. Pagamento
        O Microsserviço de Pagamento processa os pagamentos e envia mensagens para o microsserviço de Pedidos. A comunicação assíncrona entre esses serviços é gerenciada pelo RabbitMQ.
    5. Avaliacao
        O Microsserviço de Avaliação consome mensagens do RabbitMQ, processa os dados e realiza as avaliações correspondentes.