# NESTJS
- Exception
    - @nestjs/common 라이브러리에 Exception 리스트를 얻을 수 있음
    - 특별한 경우가 아니면 ```HttpException(message, httpStatus)```를 사용하면 되겠다
- link : [nestjs unittest 작성하기](https://www.youtube.com/watch?v=1Vc6Xw8FMpg)
- link : [nestjs configModule 사용하기](https://velog.io/@kakasoo/Nest%EC%97%90%EC%84%9C-ConfigModule-TypeORM-%EC%93%B0%EA%B8%B0)
- link : [nestjs multer(file upload)](https://lee-eonsang.com/blog/fileupload-with-multer)
    - multer-s3 라이브러리는 es6 구문이 아닌 commonJs 구문으로 사용해야한다.
- link : [nestjs cookies](https://codegear.tistory.com/78)
- link : [nestjs validator](https://codegear.tistory.com/76)
- link : [nestjs roles](https://codegear.tistory.com/74)
    - link : [canActivate 에 대한 이해](https://www.daleseo.com/nestjs-guards/)
        - ```guard``` 를 사용하기 위해서 필요한 interface 이다.
    - link : [reflector 에 대한 이해](https://hwasurr.io/nestjs/caching/)
        - reflector 는 Nestjs에서 제공하는 메타데이터를 다루기 위한 클래스 Reflector의 인스턴스입니다.
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

## testing
- link : [nestjs testing(official)](https://docs.nestjs.com/fundamentals/testing)
### @nestjs/jest
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

## pipe
### class-validator
- class 내부에서 non-null assertion이 사용되는 경우엔 null 체크가 아닌 컴파일러에게 해당 필드가 사용되기 전엔 반드시 defined될 것이라고 얘기하는 역할을 한다고 함. 그렇게 되면 null은 허용하게 되는 것이다.
    - link: [참고자료](https://stackoverflow.com/questions/49699067/property-has-no-initializer-and-is-not-definitely-assigned-in-the-construc)
- link : [response에서 validator를 동작시키는 방법](https://medium.com/@kuba.2001/reponse-validation-in-nestjs-0db70b955a6a)
    - nestjs 내부적으로 intercepting을 하여 response역시 validate를 하는 줄 알았는데 아니었음.
- @Param()으로 받아온 데이터의 경우도 DTO와 같은 클래스를 생성하여 class-validator를 적용한 상태로 타입명시를 하게되면 ValidationPipe의 영향을 받을 수 있음
- usePipes
    - @UsePipes(new ValidationPipe({ whitelist: true, forbidNonWhitelisted: true }))
    - 기본적으로 Nestjs 의 request body 와 dto 의 조합은 dto 에 명시되어 있지 않은 필드들을 거르지 못함. 따라서 위와 같이 처리를 해야 이를 막을 수 있음
    - whitelist: true 옵션이 없이 forbidNonWhitelisted: true 옵션만 있으면 모든 요소들을 통과시키게된다. 제대로 동작하지 않으니 주의해야 함
- 'class-validator', 'class-transformer' 라이브러리 필수
- 주 사용 데코레이터
    - @IsMongoId()
    - @IsNotEmpty()
    - @IsString()
    - @IsEnum()
        - @IsEnum(Enum Class 명, { each: true })
        - 반드시 Enum 에 존재하는 구성요소들만 들어올 수 있음
    - @IsArray()
    - @ArrayNotEmpty()
    - @MinLength(), @MaxLength()
        - String의 길이를 제한할 수 있는 데코레이터
    - @Min(), @Max()
        - 숫자의 크기를 제한할 수 있는 데코레이터
### class-transformer
- `plainToInstacne` vs `instanceToPlain`
    - js는 기본적으로 http api에서 plainToClass를 지원해주지 않는다.(참고로 response body에 담겨서 전달되는 데이터는 클래스가 아니라 그저 리터럴 객체이다)
    - 리터럴 객체를 위한 도메인 타입을 만들어두지 않은 상태에서 리터럴 객체 그 자체로 사용을 하게 되면 책임 소지가 없어진다.
    - 이런 부분에서 유용하게 사용할 수 있는 것이 `plainToInstance`이다. 리터럴 객체를 도메인 모델의 인스턴스로 만들어줌으로써 객체로써의 책임이 생겨난다.
        - ref: https://jojoldu.tistory.com/617
- `@Type()`
    - `@Type(() => Something)` 이런식의 데코레이터를 클래스 멤버변수 위에 붙이게 되면 `new Something(value)`를 하여 return을 한다.
    - null의 경우 그냥 null로 return한다.
- `ParseArrayPipe`는 어떻게 사용하는 게 좋을까?
    - new ParseArrayPipe(options) 방식으로 사용해야 원하는 타입배열로 파싱이 가능하다. 특히 options.item을 Number로, seperator를 ','(아마도 default) 로 하게 되면 number[] 타입으로 파싱이 가능하다.
- link : [ParseDatePipe](https://github.com/nestjs/nest/issues/12848)

## configuration
- link : [nestjs configuration(official)](https://docs.nestjs.com/techniques/configuration)
- configService를 inject하는 과정에서 interface 를 generic 으로 사용할 수 있음
    - 추가적으로 그 interface 의 옵션대로 auto-changing해주는 ```infer```라는 옵션이 있음
    ```
        interface EnvironmentVariables {
        PORT: number;
        TIMEOUT: string;
        }

        // somewhere in the code
        constructor(private configService: ConfigService<EnvironmentVariables>) {
        const port = this.configService.get('PORT', { infer: true });

        // TypeScript Error: this is invalid as the URL property is not defined in EnvironmentVariables
        const url = this.configService.get('URL', { infer: true });
        }
    ```

## rate limiter
- link : [nestjs rate limiter(official)](https://docs.nestjs.com/security/rate-limiting)

## openapi
- link : [nestjs openapi(official)](https://docs.nestjs.com/openapi/introduction)

## microservice
- link : [nestjs microservices(official)](https://docs.nestjs.com/microservices/kafka)

## swagger
- `@Type(() => Something)`을 사용하는 경우 `@ApiProperty({ type: Something })`을 추가해주지 않으면 스웨거에서 해당 타입을 볼 수 없다.
- link : [swagger사용 시 주의사항](https://meongae.tistory.com/99)
    - enum을 사용할 때 @ApiProperty({ enum: })을 사용해야 하는데 잘못해서 @ApiProperty({ type: })을 사용하게 되면 위 에러가 발생할 수 있음


## official site
- link : [excution context(official)](https://docs.nestjs.com/fundamentals/execution-context)
- link : [lifecycle events]()
    - resolve: dependency를 instantiate하는 것
    - initialize vs instantiate
    - lifecycle events들은 request-scoped class에 의해서는 trigger되지 않음

## Module
- 모듈의 역할을 명확히 나눠라
    - `module`들이 모여있는 hub의 역할인지? `provider`들을 제공하는 대표 module의 역할인지?
    - 전자라면 웬만하면 모듈내부에 `imports`만 채울 것
    - 후자라면 `providers`를 우선적으로 채우고, 그 다음 `providers`에 주입한 비즈니스 클래스들에 주입될 다른 providers를 가지고 있는 모듈들을 `imports`하고 모든 종속성 정리가 끝났으면 상황에 맞게 `exports`로 providers를 내보내준다(controllers는 필요할 경우 사용)
- 어느 특정 모듈에서 이미 `providers`에 injection한 비즈니스 클래스들의 경우 `절대로 다른 모듈에 이중으로 injection하지 말 것`
    - 필요할 경우 이미 injection한 module을 imports하여 사용할 것