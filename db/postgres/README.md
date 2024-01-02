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
- ```NOW()```: 현재 시간을 반환하는 함수(with Timezone)
    - ```NOW() :: timestamp```: without Timezone

## CRUD
- Update
    - string을 수정할 시, 세팅할 값을 ```작은따옴표```로 감싸야 한다.(큰따옴표 안됨)