# [Spring Cloud Config](https://spring.io/projects/spring-cloud-config)

Spring Cloud Config 는 분산시스템에서 외부 설정을 위해 서버와 클라이언트에 대한 지원을 제공한다.
Config Server 를 사용하면 모든 환경에서 외부 설정값들을 관리할 수 있는 중앙 저장소를 가지게 됩니다.
클라이언트와 서버의 개념은 Spring 의 `Environment` 와 `PropertySource` 추상화에 동일하게 맵핑되므로
Spring 애플리케이션에 매우 적합하지만 모든 언어로 사용되는 모든 애플리케이션에 이용할 수 있습니다.
애플리케이션은 배포 파이프라인을 통해 개발에서 테스트 및 프로덕션으로 이동함에 따라 환경간의 구성을 관리하고
애플리케이션이 마이그레이션할 때 실행에 필요한 모든것을 갖출 수 있습니다.
서버의 백엔드 저장소의 기본 구현은 git 을 사용하므로 광범위한 컨텐츠를 관리하는 툴에 접근할 수 있고 
쉽게 지정된 환경 설정된 버전을 지원할 수 있습니다.
스프링 구성과 관련된 구현체와 플러그인을 쉽게 추가하고 대체할 수 있습니다.

## Features

Spring Cloud Config Server features
- HTTP, 외부 설정을 위한 resource 기반의 API(이름-값 쌍 또는 YAML)
- 설정 값을 암/복호화한다(대칭/비대칭)
- **@EnableConfigServer** 를 이용해 스프링부트 애플리케이션에 쉽게 내장 가능함

Config Client features(for Spring applications)
- Config Server 와 묶이며 원격 property sources 와 Spring `Environment` 를 초기화한다.
- 설정 값을 암/복호화한다(대칭/비대칭)

## Getting Started
Spring Boot Actuator 와 Spring Client Config 가 classpath에 있다면 Spring Boot Application 은 (`spring.cloud.config.uri` 설정된 기본값 혹은)
`http://localhost:8888` 의 설정 서버로 연결을 시도합니다.
기본값을 변경하고 싶다면 `bootstrap.[yml | properties]` 에 있는 `spring.cloud.config.uri` 또는 시스템 설정, 환경 변수를 통해 설정할 수 있습니다.

```java
@Configuration
@EnableAutoConfiguration
@RestController
public class Application {

  @Value("{config.name}")
  String name = "World;
  
  @RequestMapping("/")
  public String home() {
    return "Hello " + name;
  }

  public static void main(String[] args) {
    SpringApplication.run(Application.class, args);
  }

}
```

샘플 코드에 있는 `config.name` 값(또는 일반적인 스프링 부트 방법으로 설정하는 다른 값)은 로컬 환경 혹은 원격 Config Server 에서 가져올 수 있다.
