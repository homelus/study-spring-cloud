# [Spring Cloud Netflix](https://spring.io/projects/spring-cloud-netflix)

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
- External Configuration: Spring 설정에서 Archaius 로의 브릿지(SpringBoot 규칙을 사용한 Netflix Component의 기본 구성을 사용할 수 있음)
- Router and Filter: Zull 필터의 자동 등록과 프록시 생성을 위해서 설정보다 간단한 규칙으로 접근한다.

## Getting Started
Spring Cloud Netflix 와 Eureka Core 가 classpath 에 있는 한 `@EnalbeEurekaClient` 를 사용하는 Spring Boot 애플리케이션은 
`http://localhost:8761` 로 설정된 Eureka 서버에 접속하려고 시도할 것 입니다. (기본값 `eureka.client.serviceUrl.defaultZone`)

```java
@SpringBootApplication
@EnableEurekaClient
@RestController
public class Application {

  @RequestMApping("/")
  public String home() {
    return "Hello World";
  }
  
  public static void main(String[] args) {
    SpringApplication.run(Application.class, args);
  }

}
```
