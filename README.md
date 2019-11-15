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
git 저장소에서 지원하는 중앙에 집중된 외부의 설정 관리
설정 관련 자원은 Spring 의 `Environment` 와 연결되지만 원하는 경우 Spring 이외의 응요 프로그램에서 사용할 수 있습니다.

### Spring Cloud Netflix
다양한 Netflix OSS(Open Source Software) components 를 통합한다. (Eureka, Hystrix, Zuul,  Archaius, etc..)

### Spring Cloud Bus
서비스 와 서비스 인스턴스를 분산 메시징에서 함께 연결하기 위한 이벤트 버스
클러스터에서 상태 변화를 전파하기 유용하다. (예: 환경 변경 이벤트)

### Spring Cloud Cloudfoundry
Pivotal Cloud Foundry 와 함게 애플리케이션을 통합한다.
service discovery 구현체를 제공하고 자원을 보호하는 SSO 와 OAuth2 를 구현하기 쉽게 만들어 준다.

### Spring Cloud Open Service Broker
Open Service Broker API 를 구현하는 service broker 를 만들기 위한 시작 지점을 제공한다.

### Spring Cloud Cluster
Zookeeper, Redis, Hazelcast, Consul 을 위한 추상화 및 구현체에 대한 리더십 선출 및 공용 상태 기반 패턴

### Spring Cloud Consul
Hashicorp Consul 을 이용한 Service discovery 와 환경 관리

### Spring Cloud Security
load-balanced OAuth2 rest client 지원과 Zuul proxy 에서 authentication header 중계를 제공한다.

### Spring Cloud Sleuth
Spring Cloud 애플리케이션에서 Zipkin, HTrace, log-based 추적(ELK) 과 호환되는 분산된 추적 장치이다.

### Spring Cloud Data Flow
새로운 런타임에서 마이크로서비스 애플리케이션을 구성할 수 있는 cloud-native 통합 서비스이다.
사용하기 쉬운 DSL, 드래그드랍 GUI 와 REST API 모두 마이크로서비스 기반의 데이터 파이프라인의 전체적인 통합을 간편화한다.

### Spring Cloud Stream
외부의 시스템들과 연결할 수 있도록 빠르게 애플리케이션을 빌드하기 위한 가벼운 이벤트 기반의 마이크로서비스 프레임워크 

### Spring Cloud Stream App Starters
Spring Cloud Stream App Starterts 는 다른 시스템들과 통합을 제공해주는 Spring Boot 기반의 Spring Integeration 애플리케이션이다.

### Spring Cloud Task
빠르게 유한한 양의 데이터 처리를 수행하는 애플리케이션을 빌드하기 위한 수명이 짧은 마이크로서비스 프레임워크이다.

### Spring Cloud Task App Starters
Spring Cloud Task App Starters 는 영구적으로 실행되지 않으며 한정된 데이터를 처리 후 종료하거나 중지하는 Spring Boot 응용 프로그램입니다.

### Spring Cloud Zookeeper
Apache Zookeeper 에서 서비스검색과 설정 관리를 담당합니다.

### Spring Cloud AWS

### Spring Cloud Connectors

### Spring Cloud Starters

### Spring Cloud CLI

### Spring Cloud Contract

### Spring Cloud Gateway

### Spring Cloud OpenFeign

### Spring Cloud Pipelines

### Spring Cloud Function
