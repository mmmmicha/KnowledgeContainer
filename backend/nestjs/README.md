# NESTJS
<!-- 2023.10.19 -->
- link : [nestjs 컨트롤러](https://codegear.tistory.com/58)
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