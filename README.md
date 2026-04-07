# Danil Linnik

Java / Spring backend engineer. Проектирую и разрабатываю backend-системы, в которых важны не только бизнес-функции, но и надежность интеграций, безопасность, наблюдаемость, тестируемость и удобство эксплуатации.

## Чем я занимаюсь

- Проектирую сервисные границы, API и взаимодействие между модулями и микросервисами.
- Делаю backend-сервисы не только рабочими, но и удобными в сопровождении: с безопасностью, мониторингом, логированием и устойчивой обработкой сбоев.
- Довожу систему до рабочего окружения: Docker, Kubernetes, Helm, инфраструктурные конфиги, локальный и стендовый запуск.
- Работаю как с классическим синхронным REST, так и с event-driven и reactive подходами.

## Основной стек

- Java 25, Spring Boot 4, Spring MVC, Spring WebFlux
- Spring Security, OAuth2/OIDC, Keycloak
- Spring Data JPA, Hibernate, JDBC, R2DBC, PostgreSQL, Redis, Liquibase
- Kafka, Resilience4j, OpenAPI Generator, Testcontainers
- Docker, Kubernetes, Helm, Prometheus, Grafana, Zipkin, ELK

## Архитектурный подход

- Контрактное взаимодействие между сервисами через OpenAPI и generated clients
- Надежные интеграции через retries, circuit breaker и явную обработку ошибок внешних сервисов
- Компенсационные сценарии для распределенных операций: outbox, saga orchestration, async recovery
- Security-first подход: разграничение прав, JWT/OAuth2, machine-to-machine интеграции, защита UI и API
- Наблюдаемость как часть архитектуры: structured logs, tracing, business metrics, dashboards, alerts
- Осмысленная тестовая стратегия: unit, integration, security и container-based тесты

## Избранные проекты

### [my-bank-app](https://github.com/LinnikDanil/my-bank-app)
Микросервисный banking-проект, который показывает мой подход к проектированию сложных систем целиком, а не только отдельных CRUD-сервисов.

Что внутри:
- отдельные сервисы `account`, `cash`, `transfer`, `notification`, `front` и общая библиотека `common`;
- OAuth2/OIDC через Keycloak для пользовательского и межсервисного взаимодействия;
- saga сценарий перевода денег с компенсацией при сбоях;
- transactional outbox в `transfer` для надежной асинхронной доставки событий и recovery-процессов;
- Kafka, Resilience4j, Prometheus, Grafana, Zipkin, ELK, Helm и Kubernetes.

Отдельно важно:
- в ветке `module_3_sprint_9` проект развивался со `Spring Cloud`, `gateway` и `Consul Discovery / Config`;
- в более поздних ветках архитектура была усилена Kafka-интеграциями, security, observability и k8s-инфраструктурой.

### [my-market-app](https://github.com/LinnikDanil/my-market-app)
Реактивный интернет-магазин на Spring WebFlux, где акцент сделан на web backend, security и интеграцию с платежным сервисом.

Что внутри:
- `market` как реактивная витрина, корзина, заказы, регистрация и авторизация пользователей;
- `payments` как отдельный сервис платежей;
- form login, роли, CSRF, logout-handling и OAuth2 `client_credentials` между сервисами через Keycloak;
- Redis caching, R2DBC + PostgreSQL, OpenAPI-generated client;
- компенсационный flow для заказа: hold платежа, сохранение заказа, confirm/cancel в зависимости от результата.

Этот проект хорошо показывает, что я уверенно работаю не только с привычным Spring MVC, но и с reactive стеком и нефункциональными требованиями вокруг него.

### [my-blog-back-app](https://github.com/LinnikDanil/my-blog-back-app)
Компактный backend-монолит, который хорошо демонстрирует инженерную дисциплину на базовом уровне архитектуры приложения.

Что внутри:
- REST API для постов, комментариев, лайков, изображений и тегов;
- Spring MVC + Spring Data JDBC + PostgreSQL;
- явный SQL-слой, pagination/search, централизованная обработка ошибок, CORS и логирование;
- unit-, controller-, repository- и integration-тесты с Testcontainers.

Этот проект меньше по масштабу, но отлично показывает, что даже без микросервисов я строю код предсказуемо: с понятными слоями, аккуратной работой с БД и нормальной тестовой стратегией.

## Что можно понять по этим проектам

- Я умею самостоятельно проектировать систему от доменной модели до инфраструктуры запуска.
- Мне комфортно и в монолите, и в микросервисной архитектуре, и в реактивных приложениях.
- Я думаю не только про "чтобы работало", но и про эксплуатацию, деградацию, диагностику и развитие системы.

## Contact me
[![Telegram](https://img.shields.io/badge/-Telegram-blue?style=for-the-badge&logo=telegram&logoColor=white)](https://t.me/Danil_Linnik) 
[![LeetCode](https://img.shields.io/badge/LeetCode-000000?style=for-the-badge&logo=LeetCode&logoColor=#d16c06)](https://leetcode.com/LinnikDanil/)

![](https://komarev.com/ghpvc/?username=LinnikDanil)
