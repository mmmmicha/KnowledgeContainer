# KAFKA

- kafkajs의 데이터처리는 어떤 레이어로 구성될까?
    - 우연히 로컬 서버 테스트 중 35만건의 데이터가 카프카 버퍼 메모리에 쌓여있다가 카프카를 동작시키니 전부 consuming됨(당시만해도 kafka를 도커로 올리지도 않았었고 consuming하는 서버도 로컬로 올린적이 없었음)
    - 추측으로는 `producer` > `producer쪽 버퍼` > `kafka queue` > `consumer쪽 버퍼` > `consumer` 이렇게 구성되지 않을까?

- link : [transactional outbox pattern](https://velog.io/@eastperson/Transaction-Outbox-Pattern-%EC%95%8C%EC%95%84%EB%B3%B4%EA%B8%B0)

## Debezium
- link : [Debezium Postgresql Source Connector 를 활용한 CDC](https://velog.io/@jihwankim94/Kafka-Debezium-Postgresql-Source-Connector-%EB%A5%BC-%ED%99%9C%EC%9A%A9%ED%95%9C-CDC)