# [study-spring-cloud](https://spring.io/projects/spring-cloud#overview)

스프링 클라우드는 분산 시스템에서 일반적인 패턴을 빠르게 빌드하기 위해 개발자에게 툴을 제공한다.
(configuration management, service discovery, circuit brakers, intelligent routing, micro-proxy, control bus, one-time tokens, 
global locks, leadership election, distributed sessions, cluster state)

분산 시스템간의 협력은 반복되는 패턴을 만들어 내고 Spring Cloud 를 사용하는 개발자들은 이러한 패턴들을 구현한 서비스나 애플리케이션을
빠르게 만들수 있다.
개발자들의 컴퓨터, bare metal data centers, Cloud Foundry 같은 관리되는 플랫폼들을 포함해 어떠한 분산 환경에서도 잘 동작할 것이다.

## Features

Spring Cloud 는 일반적인 사용 사레에 적합한 뛰어난 경험을 제공하고 다른 것들을 다룰 수 있는 확장성있는 메커니즘에 중점을 둡니다.

- Distributed/versioned configuration
- Service registration and discovery
- Routing
- Service-to-service calls
- Load balancing
- Circuit Breaker
- Global locks
- Leadership election and cluster state
- Distributed messaging

Spring Cloud 는 매우 선언적으로 접근하고 때떄로 많은 features 들을 단지 classpath 혹은 annotation 을 변경함으로 사용할 수 있습니다.
다음은 client 를 발견하는 예제 애플리케이션입니다.

```java
@SpringBootApplication
@EnableDiscoveryClient
public class Application {
  public static void main(String[] args) {
    SpringApplication.run(Application.class, args); 
  }
}
```

## Main Projects

### Spring Cloud Config

### Spring Cloud Netflix

### Spring Cloud Bus

### Spring Cloud Cloudfoundry

### Spring Cloud Open Service Broker

### Spring Cloud Cluster

### Spring Cloud Consul

### Spring Cloud Security

### Spring Cloud Sleuth

### Spring Cloud Data Flow

### Spring Cloud Stream

### Spring Cloud Stream App Starters

### Spring Cloud Task

### Spring Cloud Task App Starters

### Spring Cloud Zookeeper

### Spring Cloud AWS

### Spring Cloud Connectors

### Spring Cloud Starters

### Spring Cloud CLI

### Spring Cloud Contract

### Spring Cloud Gateway

### Spring Cloud OpenFeign

### Spring Cloud Pipelines

### Spring Cloud Function
