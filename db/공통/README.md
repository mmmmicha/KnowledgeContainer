# 공통

## article
- [NULL을 지양해야하는 이유와 대처방안](https://jungeunpyun.tistory.com/60)

## 강의(쉬운코딩)
- [파티셔닝, 샤딩, 레플리케이션](https://youtu.be/P7LqaEO-nGU?si=puL8SZdTfjV-W7r9)
    - `파티셔닝`: 물리적 서버 한 곳에 테이블을 vertical 또는 horizontal 방식으로 쪼개는 것
    - `샤딩`: horizontal 파티셔닝을 한 테이블들을 여러 물리적 서버에 분산하여 저장하는 것
    - `레플리케이션`: 원본 데이터베이스의 복제본들을 여러 물리적 서버에 분산하여 저장하는 것
        - `master`, `slave`의 구조로 나눠서 master는 write/read 역할 모두를, slave는 read의 역할을 지니게끔 설정이 가능함
            - 이에 따라 read에 대한 요청이 write에 대한 요청보다 월등히 많은 보통의 서버들은 read에 집중된 역할을 지니게끔하는 레플리카를 여러개 두어 효율을 높일 수 있음
            - `master`가 죽을 경우 `slave`가 역할을 위임받아 failover가 가능함
- [DB index](https://www.youtube.com/watch?v=IMDH4iAQ6zM)
    - `B-tree 인덱스`
        - 해당 인덱스 테이블에서의 서칭은 `바이너리서치`를 이용한다. O(logn)의 시간복잡도를 갖는다.
        - 보편적으로 사용되는 인덱스이다.
        - 복수개의 키를 인덱스로 설정할 경우 먼저번키의 한정하여 인덱스를 사용할 수 있다.
        - 단점으로는
            - 1. 복수개의 키를 인덱스로 설정할 때, 두번째 키는 인덱스로 사용할 수 없다.(오히려 시간 효율이 떨어질 수도 있음)
    - `Hash 인덱스`
        - 해당 인덱스는 `해시테이블`의 방식을 사용하는 데 O(1)의 시간복잡도를 갖는다.
        - 단점으로는
            - 1. 범위 조회에 인덱싱 적용 안됨
            - 2. 복수개의 키를 인덱스로 설정할 경우 반드시 그 두개의 조합을 이용해야만 인덱싱이 됨(한개라도 빠지면 인덱싱이 안됨)
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