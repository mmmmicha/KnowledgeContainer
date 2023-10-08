# SPRING
- link : [스프링 AOP](https://sg-choi.tistory.com/290)
- link : [스프링 AOP 총정리](https://engkimbs.tistory.com/746)
- link : [(Spring Boot)입문 - 스프링 빈과 컨테이너, 그리고 의존 관계(feat. IoC, DI)](https://bnzn2426.tistory.com/124)
- link : [스프링 빈과 Thread-safe](https://ehdvudee.tistory.com/18)
- link : [@Controller 와 @RestController 의 차이](https://dncjf64.tistory.com/288)

## Context path, root
- Context Path
    - 프로젝트 명을 의미하며 url의 호스트, 포트명 다음에 나온다.
- Context root
    - Content directory의 경로. 해당 경로에 메타 정보와 웹 정보를 관리하는 META-INF와 WEB-INF 파일이 자동생성되며 JSP파일은 여기 하위에 저장되어야 경로를 찾을 수 있다.


## @RestController
- @Controller 는 view 객체를 리턴할 수 있는 기능을 제공해주지만, @RestController는 문자열과 JSON 등을 전송할 수 있는 기능을 추가제공한다.

## @Service
- @Service 는 Controller 와 Repository 를 연결해주는 역할로, SpringMVC에 특화된 어노테이션이다.
- @Service는 명시적 어노테이션이다.

## Session
    
- HttpSession
    - HttpSession session = request.getSession(true) // session 생성
    - 이 session 객체는 서버에 저장됨
    - 서버 Container에 의해 관리되는 servlet들은 이 session을 공유함
    - session lifetime은 web.xml에 지정할 수 있음
    - Object session.getAttribute(키)
        - 명시적 형변환 필요
    - session.setAttribute(키, 값)


- @SessionAttribute
    - 파라미터 scope 에 쓰임
    - @SessionAttribute 값타임 키
    - 명시적 형변환을 필요없게 해줌
    - 사용이 한정적

- @SessionAttributes
    - 클래스명 위에 사용하는 어노테이션
    - 해당 어노테이션이 쓰여있는 클래스 내에서만!! Session 공유가 가능하다(큰 단점일 수 있음)
    - @SessionAttributes("UserNm", "PWD", ...)
    - Model 객체와 연관됨
        - model.setAttribute("UserNm", "정광현") --> session 에 저장이 됨.