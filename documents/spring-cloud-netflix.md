# Spring Cloud Netflix

Spring Cloud Netflix 는 자동 설정을 통해 Spring Boot 애플리케이션에 대한 Netflix OSS 통합과 
Spring Environment 와 다른 Spring programming idioms 를 제공합니다.
몇몇 간단한 애노테이션들을 사용하면 내부의 공통 패턴을 빠르게 활성화하거나 설정할 수 있으며 
Netflix 구성요소로 대규모 분산시스템을 구축할 수 있습니다.
제공되는 패턴들은 Service Discovery (Eureka), Circuit Breaker (Hystrix), Intelligent Routing (Zull) 과 
Client Side Load Balancing (Ribbon) 에 포함됩니다.

## Features

Spring Cloud Netflix 특징들

- Service Discovery: Eureka 인스턴스를 등록할 수 있고 클라이언트는 Spring 에서 관리하는 bean 들을 사용해 인스턴스를 발견할 수 있습니다.
- Service Discovery: 내장된 Eureka 서버는 선언적인 자바 설정으로 작성할 수 있습니다.
- Circuit Breaker: Hystrix 클라이언트들은 간단한 annotation-driven 메서드 데코레이터로 구축할 수 있습니다.
- Circuit Breaker: 선언적인 자바 설정이 포함된 내장 Hystrix 대시보드
- Declarative REST Client: Feign 은 JAX-RS 또는 Spring MVC 애노테이션으로 꾸며진 인터페이스의 동적인 구현체를 생성합니다.
- Client Side Load Balancer: Ribbon
- External Configuration: 
- Router and Filter: 
