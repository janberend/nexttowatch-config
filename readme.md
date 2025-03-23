# 📦 nexttowatch-config

Configuratiebestand voor de `NextToWatch` microservices.

## Structuur

Elke `.yml` file is gelinkt aan een Spring Boot microservice via de `spring.application.name`:

- `api-gateway.yml` → api-gateway
- `discovery-server.yml` → discovery-server
- `config-server.yml` → config-server

## Gebruik

Zorg dat je `config-server` verwijst naar deze Git-repo in `application.yml`:

```yaml
spring:
  cloud:
    config:
      server:
        git:
          uri: https://github.com/janberend/nexttowatch-config
          clone-on-start: true
          default-label: main
