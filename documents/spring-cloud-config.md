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

