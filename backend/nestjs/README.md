# NESTJS
- Exception
    - @nestjs/common 라이브러리에 Exception 리스트를 얻을 수 있음
    - 특별한 경우가 아니면 ```HttpException(message, httpStatus)```를 사용하면 되겠다
<!-- 2023.11.01 -->
- link : [nestjs unittest 작성하기](https://www.youtube.com/watch?v=1Vc6Xw8FMpg)
<!-- 2023.10.24 -->
- link : [nestjs configModule 사용하기](https://velog.io/@kakasoo/Nest%EC%97%90%EC%84%9C-ConfigModule-TypeORM-%EC%93%B0%EA%B8%B0)
- link : [nestjs multer(file upload)](https://lee-eonsang.com/blog/fileupload-with-multer)
    - multer-s3 라이브러리는 es6 구문이 아닌 commonJs 구문으로 사용해야한다.
<!-- 2023.10.22 -->
- link : [nestjs cookies](https://codegear.tistory.com/78)
- link : [nestjs validator](https://codegear.tistory.com/76)
- link : [nestjs roles](https://codegear.tistory.com/74)
    - link : [canActivate 에 대한 이해](https://www.daleseo.com/nestjs-guards/)
        - ```guard``` 를 사용하기 위해서 필요한 interface 이다.
    - link : [reflector 에 대한 이해](https://hwasurr.io/nestjs/caching/)
        - reflector 는 Nestjs에서 제공하는 메타데이터를 다루기 위한 클래스 Reflector의 인스턴스입니다.
<!-- 2023.10.21 -->
- link : [nestjs jwt passport](https://codegear.tistory.com/73)
    - 적용
        1. security > passport.jwt.strategy.ts 생성
        2. auth.service.ts > tokenValidateUser method 추가
        3. auth.module.ts > imports 엔 PassportModule, providers 엔 JwtStrategy 추가
        4. security > auth.guard.ts 생성
        5. 4번에 만들어진 authGuard 클래스를 provider 로 사용하고 싶은 controller method 에 사용
            - @UseGuards(AuthGuard)
- link : [construct 에 간혹 super 를 쓰는 이유](https://velog.io/@rand_guy/TILClass%EC%97%90%EC%84%9C-Constructor%EC%99%80-Super%EB%A5%BC-%EC%93%B0%EB%8A%94-%EC%9D%B4%EC%9C%A0)
- link : [nestjs jwt](https://codegear.tistory.com/72)
    - ```@nestjs/jwt``` npm 사용
    - injection 으로 private ```jwtService``` 를 사용
- link : [nestjs 비밀번호암호화(bcrypt)](https://codegear.tistory.com/71)
- link : [nestjs login](https://codegear.tistory.com/70)
<!-- 2023.10.20 -->
- link : [nestjs auth 적용하기](https://codegear.tistory.com/68)
    - link : [@EntityRepository deprecated 에 따른 해법](https://velog.io/@sheoae12/NestJS-Custom-Repository-%EB%A7%8C%EB%93%A4%EA%B8%B0)
        - @EntityRespository 를 사용할 경우 sample.module.ts 내 ```providers``` 에 SampleRepository 를 기입하지 않아도 되지만, 새로운 방법에서는 SampleRepository 에 @Injectable 을 적용하기 때문에 꼭 기입해줘야 한다.
- link : [nestjs typeorm 적용하기](https://codegear.tistory.com/67)
    - link : [typeorm 이용해서 string 'null' 이 아닌 null 넣는 방법](https://stackoverflow.com/questions/64635617/how-to-set-a-nullable-database-field-to-null-with-typeorm)
    - 주의 synchronize: true는 운영에서는 사용하지 마세요. 
    - 적용순서
        1. app.module 에 mysql 정보 등록
        2. entity 생성
        3. 생성한 entity 를 app.module 내 mysql 정보 내에 등록
        4. 해당 entity 에 해당하는 module.ts 에 imports 및 exports 로 typeorm 등록
        5. service 에 constructor 로 repository 생성한 후 사용
<!-- 2023.10.19 -->
- link : [nestjs 미들웨어](https://codegear.tistory.com/63)
    - 미들웨어는 라우터 핸들러 이전에 호출되는 함수
    - ```@Injectable``` 데코레이터를 사용합니다
    - ```NestMiddleware``` 인터페이스를 implements 해서 사용합니다
    - Module의 class 내부에 ```configure``` 를 사용하여 선언합니다. 이때 ```NestModule``` 인터페이스를 implements 합니다
- link : [nestjs 서비스](https://codegear.tistory.com/59)
    - service 는 ```provider``` 에 해당되며, provider는 종속성에 의해 Inject(주입)할 수 있습니다. 즉, provider 객체의 생성 및 연결은 nest runtime 시스템에 위임될 수 있습니다.
    - ```@Injectable()``` 데코레이터는 이 class가 Nest IoC 컨테이너에서 관리하는 class 임을 선언하는 것입니다.
    - CatsService는 ```constructor``` 를 통해 주입됩니다. ```private``` 을 사용하면 선언과 초기화가 동시에 이루어 집니다.
- link : [nestjs 컨트롤러](https://codegear.tistory.com/58)
    - NestJS는 Express를 사용하고 있으므로 인해 Request 객체를 사용할 수 있습니다.
        - 핸들러 parameter에 ```@Req()``` 데코레이터를 사용하면 됩니다.
- spring 에서는 ```@``` 을 ```어노테이션```이라고 하지만, nestjs 에서는 ```데코레이터```라고 함
- link : [nestjs 소스 자동 생성기](https://codegear.tistory.com/57)
    - 모듈 자동 생성하기
        ```
        nest g module 모듈명
        ```
    - 컨트롤러 자동 생성하기
        ```
        nest g controller 컨트롤러명
        ```
    - 서비스 자동 생성하기
        ```
        nest g service 서비스명
        ```
- link : [nestjs 구조 이해하기](https://codegear.tistory.com/56)
    - nestjs 는 모듈의 집합체임
        - module = controller(controller) + provider(service)
- link : [nestjs 설치 및 생성](https://codegear.tistory.com/54)
    - 설치
        ```
        (sudo) npm i -g @nestjs/cli
        ```
    - 프로젝트 생성
        ```
        (sudo) nest new project-name
        ```
- link : [nestjs 란?](https://codegear.tistory.com/53)
    - Node.js의 높은 자유도로 인해 Architecture 구성이 어렵고 효과적이지 못했습니다. 이를 해결하기 위해 Angular의 아키텍처 사상을 기반으로 Nest가 만들어졌습니다.

## mongoose
- link : [createdAt, updatedAt](https://khajehossini.medium.com/nestjs-createdat-and-updatedat-in-schema-d1ad6cf525e0)
- link : [nestjs mongoose](https://www.youtube.com/watch?v=ulfU5vY6I78)
    - link : [nestjs mongoose official site](https://docs.nestjs.com/techniques/mongodb#async-configuration)

## @nestjs/jest
- npm run test src 를 통해 전체 spec 코드 테스트가 가능함
- *.spec.ts 파일 작성할 때 유의사항
    - 기존 베이스가 되는 파일이든 위 spec.ts 파일이든 모듈을 import 할때는 항상 상대경로를 이용해야한다.
- jest 코드 작성 순서
    1. 필요 변수들 선언
        - ex) dto, Id, ...
    2. 필요 모델 생성
        - ex) const userModel = module.get(getModelToken(User.name))
    3. 필요 mock 함수 생성
        - ex) userModel.find = jest.fn().mockResolvedValue(mockUser)
    4. result
        - ex) const result = await service.find(Id)
    5. expect
        - ex) expect(result).toEqual(mockUser)
        - ex) expect(userModel.find).toBeCalledWith(Id)
- jest.fn()
    - .mockResolvedValueOnce()
        - 구현해야 하는 service 함수 내 mocking 의 대상이 되는 함수가 여러번 불려야 하는데 심지어 값이 다를 경우 유용하게 사용할 수 있음.
        - piping 해서 여러개를 붙일 수 있음
            - ex) fn().mockResolvedValueOnce().mockResolvedValueOnce()...
    - .mockReturnValue()
        ```
            pageModel.find = jest.fn().mockReturnValue({
                lean: jest.fn().mockResolvedValue([mockSubPage]),
            });
        ```
        - 위 예시처럼, '.find()' 를 통해 리턴되는 객체에 대한 파이핑을 설정할 수 있음
- expect
    - toBeInstanceOf()
        - exception 을 비교할 때 유용하게 사용할 수 있음
            ```
            try {
                await service.deleteOne(subId, differentUserId);
            } catch (error) {
                expect(error).toBeInstanceOf(UnauthorizedException);
            }
            ```
    - toBeLessThanOrEqual()
        - new Date() 와 같이 실시간으로 바뀌는 데이터를 비교할 때 유용하다
        - 단, int / bigInt 만 parameter 로 사용할 수 있다
            ```
            expect(result.deletedAt.getTime()).toBeLessThanOrEqual(new Date().getTime());
            ```
    - toStrictEqual()
        - 정의상으론 sorting 된 배열을 비교할 때 사용한다고 하는데 잘 모르겠음
            ```
            const sortedFilteredNewsList = filteredNewsList.sort(function(a:any, b:any) { return b.createdAt - a.createdAt });
        expect(result).toStrictEqual(sortedFilteredNewsList);
            ```

## validator
- usePipes
    - @UsePipes(new ValidationPipe({ whitelist: true, forbidNonWhitelisted: true }))
    - 기본적으로 Nestjs 의 request body 와 dto 의 조합은 dto 에 명시되어 있지 않은 필드들을 거르지 못함. 따라서 위와 같이 처리를 해야 이를 막을 수 있음
- 'class-validator', 'class-transformer' 라이브러리 필수
- 주 사용 데코레이터
    - @IsNotEmpty()
    - @IsString()
    - @IsEnum()
        - @IsEnum(Enum Class 명, { each: true })
        - 반드시 Enum 에 존재하는 구성요소들만 들어올 수 있음
    - @IsArray()
    - @ArrayNotEmpty()
    - @MinLength()
    - @MaxLength()