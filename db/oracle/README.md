# ORACLE DB

## ANSI SQL    
- link : [ANSI SQL 이란?](https://lena19760323.tistory.com/60)

## TNS Service(ORACLE)
- link : [오라클 TOAD(토드) TNS, SID 연결 설정](http://blog.naver.com/PostView.nhn?blogId=hei4&logNo=220105219049)

## merge into(오라클)
- 해당 테이블에 key가 존재한다면 `update`, 존재하지 않는다면 `insert`
- Java Map 중 `getOrDefault()` 메소드가 이와 비슷하다고 생각
- link : [[오라클] MERGE INTO 구문 정리](https://m.blog.naver.com/PostView.nhn?blogId=wiseyoun07&logNo=220319875065&proxyReferer=https:%2F%2Fwww.google.com%2F)

## index
- 일종의 DB 주소록
- index도 결국은 테이블이다.
- link : [ORACLE 인덱스(Index) 개념/종류/주의사항/활용,관리](https://rongscodinghistory.tistory.com/113)

## PF Key
- Primary key임과 `동시에` Forien Key인 Key를 말함.
- 주로 `Composite Key(복합키)` 로 사용된다.
- 독립적으로 사용되는지는 의문이다.

## DECODE 함수 
```
    DECODE(컬럼, 조건1, 결과1, 조건2, 결과2, 조건3, 결과3..........) 
```