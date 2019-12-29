# [Spring Cloud Bus](https://spring.io/projects/spring-cloud-bus)

Spring Cloud Bus 는 분산시스템의 노드들을 가벼운 메시지 브로커와 함께 연결합니다.
이것은 상태의 변화(예: 설정 변경) 혹은 기타 관리 명령들을 모두에게 전달하는데 사용할 수 있습니다.
현재 유일한 구현체는 전송방법으로 AMQP 브로커를 사용하지만 동일한 기본 기능들(전송에 따르는 더많은 다른것들)은 다른 전송 방법으로 가능합니다.

## Getting Started
Spring Cloud Bus AMQP 와 RabbitMQ 가 클래스패스에 있는 한 Spring Boot 애플리케이션은 `localhost:5672`
(spring.rabbitmq.addresses 기본값) 로 Rabbit MQ 서버에 연결을 시도합니다.

```java
@Configuration
@EnableAutoConfiguration
@RestController
public class Application {
  
  @RequestMappihg("/")
  public String home() {
    return "Hello World";
  }
  
  public static void main(String[] args) {
    SpringApplication.run(Application.class, args);
  }
  
}
```
