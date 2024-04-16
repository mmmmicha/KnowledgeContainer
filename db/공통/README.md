# 공통

## article
- [NULL을 지양해야하는 이유와 대처방안](https://jungeunpyun.tistory.com/60)

## 강의(쉬운코딩)
- MVCC
    - 요점
        - mysql 과 postgresql의 경우 isolation level에 따른 MVCC 동작이 다르다
            - `repeatable read` level
                - mysql은 `for share(read lock)`, `for update(write lock)`을 사용하여 lock의 주도권을 각각의 트랜잭션이 기다리면서 로직을 마무리 한다.
                - postgresql은 자동적으로 `for share` 이나 `for update`가 적용이 되는 대신 postgresql의 특성상 같은 데이터에 대해 여러 트랜잭션이 접근할 경우 가장 먼저 접근한 트랜잭션만 성공시키고 그 외 트랜잭션들은 롤백시켜버리기 때문에 데이터에 대한 접근 재시도를 할 수 있는 로직이 추가적으로 필요하다.
    - [MVCC 2부](https://youtu.be/-kJ3fxqFmqA?si=Z6Z2wnQ_MI6WIrad)
    - [MVCC 1부](https://youtu.be/wiVvVanI3p4?si=39w1SwrI3Z2C31ir)
- [concurrency control 기법 : LOCK & 2PL](https://youtu.be/0PScmeO3Fig?si=5wZV21jb-vci44tb)
- [isolation level](https://youtu.be/bLLarZTrebU?si=4sbsW6roVaTHilcG)
- [(2부) concurrency control 기초 : recoverability](https://youtu.be/89TZbhmo8zk?si=lvtmZ9dDm0Vul2Va)
- [(1부) concurrency control 기초 : serializability](https://youtu.be/DwRN24nWbEc?si=gEwvC2X4JiMPmuij)
- [트랜잭션 기본, ACID](https://youtu.be/sLJ8ypeHGlM?si=VOD4g0IyhKigSdgJ)