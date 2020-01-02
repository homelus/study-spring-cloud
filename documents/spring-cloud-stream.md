# [Spring Cloud Stream](https://spring.io/projects/spring-cloud-stream)

Spring Cloud Stream 은 공유되는 메시지 시스템에 연결된 고 가용성 이벤드 주도 마이크로서비스들을 구축하기 위한 프레임워크입니다.

프레임워크는 스프링 철학과 예제들(영구적인 pub/sub, 컨슈머 그룹, 상태값 파티션에 대한 지원을 포함하여)에 
친숙한 이미 만들어진 유연한 프로그래밍 모델을 제공합니다.

## Binder Implementations

Spring Cloud Stream 은 다양한 binder 구현체들과 다음의 테이블(GitHub projects)들을 지원합니다.

- [RabbitMQ](https://github.com/spring-cloud/spring-cloud-stream-binder-rabbit)
- [Apache Kafka](https://github.com/spring-cloud/spring-cloud-stream-binder-kafka)
- [KafkaStreams](https://github.com/spring-cloud/spring-cloud-stream-binder-kafka/tree/master/spring-cloud-stream-binder-kafka-streams)
- [Amazon Kinesis](https://github.com/spring-cloud/spring-cloud-stream-binder-aws-kinesis)
- [Google PubSub](https://github.com/spring-cloud/spring-cloud-gcp/tree/master/spring-cloud-gcp-pubsub-stream-binder) (partner maintained)
- [Solace PubSub+](https://github.com/SolaceProducts/spring-cloud-stream-binder-solace) (partner maintained)
- [Azure Event Hubs](https://github.com/microsoft/spring-cloud-azure/tree/master/spring-cloud-azure-stream-binder/spring-cloud-azure-eventhubs-stream-binder) (partner maintained)
- [Apache RocketMQ](https://github.com/alibaba/spring-cloud-alibaba/wiki/RocketMQ-en) (partner maintained)

Spring Cloud Stream 의 핵심구조는 다음과 같습니다.

- Destination Binders: 외부 메시징 시스템과의 통합을 제공할 책임을 가진 컴포넌트
- Destination Bindings: 외부 메시징 시스템과 메시지에 대한 Producer 와 Consumer 를 제공하는 애플리케이션 간의 Bridge
- Message: Destination Binders(및 외부 메시징 시스템과 통하는 다른 Application) 와 통신하기 위해 producers 와 consumers 가 
사용하는 원본 데이터 구조 

