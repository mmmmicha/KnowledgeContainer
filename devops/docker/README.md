# DOCKER
- link : [docker network 설정하기2](https://www.daleseo.com/docker-networks/)
- link : [도커(Docker) 입문편 | 컨테이너 기초부터 서버 배포까지](https://www.44bits.io/ko/post/easy-deploy-with-docker)
- link : [springbootApp docker로 배포하기 및 mysql 연동](https://galid1.tistory.com/726)
- link : [docker network 설정하기](https://galid1.tistory.com/723)
- link : [도커(wiki)](https://ko.wikipedia.org/wiki/%EB%8F%84%EC%BB%A4_(%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4))
- `Container` 관리 플랫폼 
- Container 와 `image` 가 매우 중요
    - image : Container 에 대한 A to Z 를 모두 가지고 있는 파일
        - 이 때문에 다른 라이브러리가 필요없음.
- `레이어 저장방식`이 유용함
    - 버젼업이 되거나 파일이 추가될 경우 전체 파일을 다시 배포하는 것이 아니라 추가된 파일만 새로운 layer 로 추가되는 형식.

## exec
- 컨테이너 접근 후 사용할 수 있는 패키지 인스톨러
    - apt, apt-get
- 위 인스톨러들을 이용하여 각종 패키지를 설치가 되지 않는 경우 아래 명령어를 반드시 실행
    ```
    apt-get update
    ```

## volume
- link : [docker volume 사용법](https://0902.tistory.com/6)

## 쿠버네티스(Kubernetes) vs 도커(Docker)
- keyword : `컨테이너`와 `오케스트레이션`의 이해
- link : [쿠버네티스 vs. 도커 : 컨테이너와 오케스트레이션의 이해](http://www.itworld.co.kr/news/135282)