# MYSQL
- link : [int(4) 와 tinyint(4), smallint(4)의 차이점은?](https://kojin777.tistory.com/57)
- link : [MySQL Partition 파티션(2) - 파티션 종류 와 파티션 테이블 생성 과 변경](https://hoing.io/archives/8527)
- link : [MySQL 쓰면서 하지 말아야 할 것 17가지](https://blog.lael.be/post/370)
- link : [Range partition by timestamp](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=sory1008&logNo=221276594829)
- link : [EVENT SCHEDULE](https://pinokio0702.tistory.com/85)

## index
- link : [B-Tree로 인덱스(Index)에 대해 쉽고 완벽하게 이해하기](https://mangkyu.tistory.com/286)
    - 주요
        - `카디널리티`가 높은 컬럼일수록 인덱스를 걸었을 때 성능 개선이 있다.
            - `카디널리티`란 중복되지 않는 정도로 해석할 수 있다.
        - 조회하고자 하는 조건의 데이터가 전체의 25퍼센트를 넘어설 경우 풀스캔을 실행해버릴수도 있다.