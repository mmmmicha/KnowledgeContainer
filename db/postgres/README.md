# POSTGRES

## 구동
- link : [homebrew로 postgres설치 후 접속하기](https://reinvestment.tistory.com/66)
- link : [postgres docker로 구동하기](https://devinlife.com/postgresql/run-postgresql-on-docker/)

## 백업
- link : [데이터 백업 및 복구](https://bhpark.tistory.com/225)

## extension
- link : [extension make시 postgres.h 파일 없어서 나는 에러 해결방법](https://stackoverflow.com/questions/56724622/how-to-fix-postgres-h-file-not-found-problem)
- link : [extension 설치 과정 에러나는 경우 해결 방법](https://effortmakesme.tistory.com/32)
- link : [postgres extension](https://bitnine.tistory.com/536)
    ```
    make USE_PGXS=1
    make USE_PGXS=1 install
    ```

## Function
- ```window function```
    - 대표적으로 `OVER(PARTITION BY something1, ORDER BY something2)`
    - ref : https://postgresql.kr/docs/9.3/tutorial-window.html
- ```NULLIF(value, replaceValue)```
    - value가 null일 경우 replaceValue를 반환한다.
- ```LN()```
    - loge 를 씌운 값을 반환한다.
- ```RANK()```
    - link : [row_num, rank](https://new-hero.tistory.com/22)
- ```NOW()```: 현재 시간을 반환하는 함수(with Timezone)
    - ```NOW() :: timestamp```: without Timezone
- [generate_series()](https://sas-study.tistory.com/380)
- ```COUNT()```에서 ```DISTINCT```를 사용하게 되면 유니크 한 값들로 카운팅을 하게 되기 때문에 기본적인 COUNT()보다는 값이 적게 나온다

## Join
- [Join의 종류](https://ysyblog.tistory.com/141)
    - ```cross join```은 1:N의 베이스 테이블 초기 셋팅에 굉장히 유용하다
    ```
        // 아래와 같이 사용하면 날짜당 모든 카테고리가 1:N으로 셋팅 된다
        WITH date_series AS
        (SELECT DISTINCT
            date_trunc('week', GENERATE_SERIES('2021-01-01'::date, now(), '1 day')::date + 1)::date - 1 AS day)
        select dc.day,
               c.id,
               c.name
        from date_series dc
        cross join "Category" c
    ```

## Type
- `Date` vs `Timestamp`
    - link : [(강추)official doc](https://www.postgresql.org/docs/current/functions-datetime.html)

## Date
- [postgresql date document official](https://www.postgresql.org/docs/current/functions-datetime.html)
    - date_trunc() 설명 잘되어 있음

## CRUD
- Update
    - string을 수정할 시, 세팅할 값을 ```작은따옴표```로 감싸야 한다.(큰따옴표 안됨)

## offset limit
- link : [offset limit ordering bug](https://stackoverflow.com/questions/13580826/postgresql-repeating-rows-from-limit-offset)

## ALTER
- link : [TRUNCATE ... RESTART IDENTITY](https://www.postgresql.org/docs/current/sql-truncate.html)
    - 요약
        - `시퀀스`를 초기화해준다.