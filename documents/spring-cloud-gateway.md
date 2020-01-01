# [Spring Cloud Gateway](https://spring.io/projects/spring-cloud-gateway)

이 프로젝트는 Spring MVC 위에서 API 게이트웨이를 구축하기 위한 라이브러리를 제공합니다.
Spring Cloud Gateway 는 간단하지만 효과적인 방법으로 API 를 라우팅하고 보안, 모니터링, 통계, 장애대응과 같은 횡단 관심사를 제공하는 것을
목표로 합니다.

## Features

Spring Cloud Gateway features:

- Spring Framework 5 와 Project Reactor, Spring Boot 2.0 으로 구축됩니다.
- 모든 요청들을 경로들과 매칭할 수 있습니다.
- Predicates 와 filters 는 라우팅하기 위해 명시됩니다.
- Hystrix Circuit Breaker 와 통합됩니다.
- Spring Cloud DiscoveryClient 와 통합됩니다.
- Predicates 와 Filters 를 쓰기가 쉽다.
- 요청 속도를 제한할 수 있다.
- 경로를 재작성할 수 있다.

## Getting Started

```java
@SpringBootApplication
public class DemogatewayApplication {
  @Bean
  public RouteLocator customRouteLocator(RouteLocatorBuilder builder) {
    return builder.routes()
      .route("path_route", r -> r.path("/get")
          .uri("http://httpbin.org"))
      .route("path_route", r -> r.host("*.myhost.org")
          .uri("http://httpbin.org"))
      .route("rewrite_route", r ->  r.host("*.rewrite.org")
          .filters(f -> f.rewritePath("/foo/(?<segment>.*)",  "/${segment}"))
          .uri("http://httpbin.org"))
      .route("hystrix_route", r -> r.host("*.hystrix.org")
          .filters(f -> f.hystrix(c -> c.setName("slowcmd")))
          .uri("http://httpbin.org"))
      .route("hystrix_fallback_route", r -> r.host("*.hystrixfallback.org")
          .filters(f -> f.hystrix(c -> c.setName("slowcmd").setFallbackUri("forward:/hystrixfallback")))
          .uri("http://httpbin.org"))
      .route("limit_route", r -> r.host("*.limited.org").and().path("/anything/**")
          .filters(f -> f.requestRateLimiter(c -> c.setRateLimiter(redisRateLimiter())))
          .uri("http://httpbin.org"))
      .build();
  }
}
```
gateway를 작동시키려면 `spring-cloud-starter-gateway` 종속성을 하면 됩니다.


