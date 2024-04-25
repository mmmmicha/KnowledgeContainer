# PRISMA
- link : [select vs include in NESTJS Prisma](https://stackoverflow.com/questions/69679956/nestjs-prisma-orm-using-select-versus-include-when-fetching-data-records)

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
