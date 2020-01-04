# [Spring Cloud Data Flow](https://spring.io/projects/spring-cloud-dataflow)

Cloud Foundry 와 Kubernetes를 위한 배치 처리와 스트리밍 기반의 마이크로서비스

Spring Cloud Data Flow 는 스트리밍과 일괄처리 데이터 파이프라인을 위한 복잡한 토폴로지를 만드는 툴을 제공한다.
데이터 파이프라인은 [Spring Boot](https://spring.io/projects/spring-boot) 애플리케이션으로 구성되며 [Spring Cloud Stream](https://spring.io/projects/spring-cloud-stream) 혹은
[Spring Cloud Task](https://cloud.spring.io/spring-cloud-task/) 마이크로서비스 프레임워크를 사용해 구축되었다.

Spring Cloud Data Flow 는 ETL 에서 부터 import/export, 이벤트 스트리밍, 예측 분선 등의 다양한 데이터 처리들을 지원한다.

## Features
Spring Cloud Data Flow 서버는 Cloud Foundry나 Kubernetes 와 같은 최신 플랫폼에서 Spring Cloud Stream 혹은 Spring Cloud Task 애플리케이션으로 만들어진 데이터 파이프라인을 배포하기 위해 [Spring Cloud Deployer](https://github.com/spring-cloud/spring-cloud-deployer/) 를 사용한다.





