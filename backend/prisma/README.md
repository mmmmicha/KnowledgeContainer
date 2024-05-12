# PRISMA
- link : [select vs include in NESTJS Prisma](https://stackoverflow.com/questions/69679956/nestjs-prisma-orm-using-select-versus-include-when-fetching-data-records)

## Connection Pool
- 기본적으로 `new PrismaClient()`를 통해 프리즈마 인스턴스를 만들때마다 커넥션풀이 생성된다.
- 커넥션풀은 상당히 조심히 다뤄야한다. DB마다 정해진 커넥션풀의 물리량이 있고, 이를 모두 특정 서버에서 할당받아 사용할 경우 다른 서버들은 해당 DB와 커넥션을 맺지못한채 기다려야하는 상황이 생긴다.
- 커넥션풀은 커넥션의 생명을 계속 유지하면서 빌려주고 반납받는 식으로 커넥션을 관리한다.
    - TCP 연결을 통해 소켓을 열어두고 세션을 계속 유지하는 것이다.
- Prisma는 쿼리요청이 있을 경우 가용한 커넥션을 커넥션풀내에서 할당한다.
- 커넥션풀내에 있는 모든 커넥션이 할당된 경우엔 다른 쿼리들이 프리즈마 큐에서 커넥션을 할당받길 기다린다. 이때 큐에서 기다리는 waitTime을 설정할 수도 있다.

## query option
- contains
    - like 조건과 같음
- equals
    - 완전 일치
- insensitive
    - 대문자와 소문자구분을 안함. (사용안하면 default로 sensitive해짐)
    ```
    prisma.cat.findMany({
        where: {
            name: {
                contains: "mew",
                mode: "insensitive"
            }
        },
        select: { id: true }
    })
    ```
- OR
    - 반드시 대문자로 해야함
    ```
    prisma.cat.findMany({
        where: {
            OR: {
                name: {
                    ...
                },
                id: {
                    ...
                }
            }
        }
    })
    ```

## 명령어
- npx prisma migrate dev --create-only: draft migration file만 생성 ( 즉, /prisma/migrations/생성시간_이름/migration.sql 생성 )
- npx prisma migrate deploy: DB에 적용 및 _prisma_migrations 업데이트
- npx prisma generate: prisma client 생성 ( 즉, 타입을 만들고 코드에 적용 )
- npx prisma migrate dev: 위 3가지 명령어 순차적으로 실행 ( 즉, .sql 만들고 DB에 적용하고 코드에 적용 )
- prisma db pull
    - 이걸 사용하게 되면 ```schema.prisma```파일이 db 정보로 덮어써지게 된다.(주의요망)
- prisma format
    - prisma.schema 파일 내 형식을 맞춰준다.
    - 1:N 관계에서 1을 나타내는 스키마에 relation을 표시한 후 prisma format을 하면 N을 나타내는 스키마에도 relation이 표시된다.

## prisma select
- `includes` 를 사용하지 않고 `find-` 메서드들을 사용하는 경우 related되어 있는 데이터들은 기본값으로 조회할 수 없다.

## prisma syntax
- prisma.schema.$transaction([func1, func2, func3])
    - const [res1, res2, res3] 이런식으로 위에 대한 결과를 받을 수 있음
- prisma.schema.$transaction(async (tx) => {
    ...
})
    - tx.schema.create 이런식으로 사용할 수 있음. 내부에 await를 사용하면서 코드 구성을 할 수 있다는 게 특징

## schema.prisma
- @@unique()
- @relation()
    - 자식테이블에서 작성한다
    - 그 이후 prisma format 명령어를 콜하게 되면 부모테이블에 프로퍼티가 생긴다
    - ex)
        ```
            model GroupMember [
                id
                groupId
                Group @relation(fields: [groupId], references: [id])
            ]

            // 이 상태에서 prisma format 명령어를 콜하게 되면

            model Group {
                id
                GroupMembers GroupMember[]
            }

            // 부모테이블에 위와 같이 프로퍼티가 생긴다
        ```

## kysely
- link : [(승준님글)kysely란 무엇인가?](https://velog.io/@easdkr/Prisma-%EC%99%80-kysely-%ED%95%A8%EA%BB%98-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0)
    - prisma의 extension라이브러리인데, 기존 prisma의 아래 단점들을 보완하기 위해 제공되기 시작했다.
        - raw 쿼리 작성에 대해 힌트 제공이 없고, raw 쿼리 작성 이후 return type이 unknown으로 제공됨으로 인해 런타임 오류 가능성이 있다.
        - prisma 기본 라이브러리에 lock, join 같은 메이저한 기능 지원이 없다.