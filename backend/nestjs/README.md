# NESTJS
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