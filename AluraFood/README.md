# AluraFood - Microsserviço de Pagamentos

Este projeto faz parte de um curso focado na construção de microsserviços com Java e Spring. O objetivo foi criar um microsserviço de pagamentos para uma plataforma fictícia de pedidos de comida chamada AluraFood.

Principais Funcionalidades

- Arquitetura de Microsserviços: O projeto foi desenvolvido como microsserviços, lidando com pagamentos de forma independente dentro da plataforma AluraFood.
- Banco de Dados MySQL: O microsserviço se conecta a um banco de dados MySQL isolado, com migrações gerenciadas e versionadas utilizando o Flyway.
- Service Discovery: O Eureka é utilizado para a descoberta de serviços, permitindo que os microsserviços se registrem e descubram uns aos outros pelo nome.
- API Gateway: As requisições são centralizadas e roteadas através de um API Gateway, o que é crucial para gerenciar microsserviços em um sistema distribuído.
- Comunicação Síncrona: O OpenFeign é utilizado para habilitar a comunicação síncrona entre o serviço de pagamentos e outros microsserviços, como o serviço de pedidos.
- Padrões de Resiliência: O padrão circuit breaker, implementado com o Resilience4j, garante que o sistema permaneça estável e responsivo mesmo quando certos serviços não estão disponíveis. Métodos de fallback são fornecidos para lidar com falhas.

## Tecnologias Utilizadas

- Java 17
- Spring Boot 3
- Spring Cloud Netflix Eureka
- Spring Cloud OpenFeign
- Spring Cloud Gateway
- Resilience4j
- MySQL
- Flyway
- Postman (para testes de API)
