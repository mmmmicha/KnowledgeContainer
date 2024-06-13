# DESIGN PATTERN

## RESTFul
- link : [REST API 제대로 알고 사용하기](https://meetup.nhncloud.com/posts/92)
- link : [REST API의 이해와 설계 - API 보안](https://bcho.tistory.com/955)
- link : [(번역) RESTful API Designing guidelines — The best practices](https://wayhome25.github.io/etc/2017/11/26/restful-api-designing-guidelines/)
- link : [REST란? REST API 디자인 가이드](https://covenant.tistory.com/241)

### PathVariable 과 QueryStringParameter 의 차이
- Path Variable
    ```
        localhost:8080/delete/123
    ```
    - 경로 상 parameter 를 넘기는 것
    - delete에 주로 쓸 수 있음
    - ```required```조건인 값을 사용한다.
- Query String Parameter
    ```
        localhost:8080/put?id=321&name=예제
    ```
    - ? 뒤에 넘기게 되는 parameter를 지칭함
    - 주로 get방식에 쓰인다.
    - ```optional```조건인 값을 사용한다.

## 스트래티지
- link : [스트래티지 패턴이란](https://gmlwjd9405.github.io/2018/07/06/strategy-pattern.html)

## 템플릿 메서드
- link : [템플릿 메서드 패턴으로 모순 없는 상태 보장하기](https://engineering.linecorp.com/ko/blog/templete-method-pattern)

## 싱글톤
- link : [싱글톤(Singleton) 패턴 [생성 패턴]](https://effortguy.tistory.com/183)

## 빌더
- link : [빌더패턴 완벽 마스터하기](https://inpa.tistory.com/entry/GOF-%F0%9F%92%A0-%EB%B9%8C%EB%8D%94Builder-%ED%8C%A8%ED%84%B4-%EB%81%9D%ED%8C%90%EC%99%95-%EC%A0%95%EB%A6%AC)

