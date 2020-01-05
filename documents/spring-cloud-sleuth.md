# [Spring Cloud Sleuth](https://spring.io/projects/spring-cloud-sleuth)

Spring Cloud Sleuth 는 Dapper, Zipkin, HTrace 의 힘을 빌려 Spring Cloud 를 위한 분산된 추적 솔루션을 구현한다. 
많은 사용자에게 Sleuth 는 보이지 않아야 하고 외부 시스템과의 모든 상호작용 은 자동적으로 측정되어야 합니다.
데이터를 로그에서 간단히 보관하거나 원격 수집 서비스로 전송하여 데이터를 가지고 있을 수 있습니다.

## Features

Span 은 기본적인 작업 단위 입니다.
예를 들어, RPTC에 응답을 보내는 것처럼 RPC 로 전송하는 것은 새로운 span 입니다.
