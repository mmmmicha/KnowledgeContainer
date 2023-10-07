# ETC
- 아직 분류가 제대로 되지 않은 지식들

## Base64 vs safe url Base64
- 끝부분 `=` 는 없애고, `+` => `-` & `/` => `_`
    - url 로 들어갔을 때 치명적일 수 있는 문자들이기 때문.
- 다시 바꿀 땐 역으로. 단, `=` 의 경우 전체 문자의 길이를 4로 나눴을 때 나머지가 나오면 `4-나머지` 만큼 `=` 를 끝에 더한다.
    
## Encrypt
- RSA 암호화
    - 공개키, 개인키 암호화 시스템
- ecdh(≒secp256r1 ≒nistP256)
    - 서로 다른 둘이 각각 key pair(공개, 비밀) 을 만들어서 공개키를 교환한 후 각자의 비밀키와 공개키로 secret key 를 만들었을 때 그 값이 같아야함.
- ECB, CBC
    
## PathVariable 과 QueryStringParameter 의 차이
- Path Variable
    ```
        localhost:8080/delete/123
    ```
    - 경로 상 parameter 를 넘기는 것
    - delete에 주로 쓸 수 있음
- Query String Parameter
    ```
        localhost:8080/put?id=321&name=예제
    ```
    - ? 뒤에 넘기게 되는 parameter를 지칭함
    - 주로 get방식에 쓰인다.
    
## ssh(Secure Shell)
- [ssh란?](https://jootc.com/p/201808031460)
- 보안이 아주 강한 통신 프로토콜
    
## 캐시서버(Cache Server)
- [캐시서버란(나무위키)](https://namu.wiki/w/%EC%BA%90%EC%8B%9C%20%EC%84%9C%EB%B2%84)
- [캐시서버란 무엇인가](http://www.dt.co.kr/contents.html?article_no=20000330101602002)
    
## Git 캐시 삭제 명령어
    git rm -r --cached .
    git add .
    
## 템플릿 엔진(Template Engine)
- [템플릿 엔진이란?](https://gmlwjd9405.github.io/2018/12/21/template-engine.html)
    
## TNS Service(ORACLE)
- [참고링크](http://blog.naver.com/PostView.nhn?blogId=hei4&logNo=220105219049)
- 정리해야함!!
    
## 클라우드 컴퓨팅
- 정의
    - 내 컴퓨터가 아닌 원격의 컴퓨터의 자원을 이용하는 컴퓨팅방식
- 종류
    - SaaS(Software as a Service)
    - Iaas(Instructure as a Service)
    - FaaS(Flatform as a Service)
    - DaaS(Desktop as a Service) : [참조링크](https://www.vmware.com/kr/topics/glossary/content/desktop-as-a-service.html)
    - BaaS(Blockchain as a Service)
    
## 인포테인먼트
- [네비가 아니라 인포테인먼트 시스템입니다.](https://brunch.co.kr/@realhoo/11)
- '정보' 를 뜻하는 `인포메이션(Information)` 과 '즐거움'을 뜻하는 `엔터테인먼트(Entertainment)`의 합성어
    
## 사설 IP, 공인 IP
- [IP주소 구분에 대한 모든 것(강추!!)](http://gotocloud.co.kr/?p=320)
- [사설 IP주소와 VPN](https://velog.io/@noyo0123/VPN%EC%9D%B4%EB%9E%80-czk1z1of8x)
- [포트 포워딩(외부에서 내 컴퓨터 접속하기)](http://webprogramming.co.kr/admins_blog/1397)
    
## 호스트(host)
- 호스트의 기준 : IP 주소
    - IPv4, IPv6
- link : [호스팅 vs 클라우드](https://brunch.co.kr/@gabianow/6#comment)
- link : [호스트이름, 도메인이름](https://dnssec.tistory.com/26)
- 호스팅이란 정보의 집약체인 서버의 전체 혹은 일부를 이용할 수 있도록 임대해 주는 서비스를 말합니다.
- link : [호스팅이란 무엇인가?](http://blog.wishket.com/%ED%98%B8%EC%8A%A4%ED%8C%85%EC%9D%B4%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C-%EA%B7%B8%EB%A6%B0%ED%81%B4%EB%9D%BC%EC%9D%B4%EC%96%B8%ED%8A%B8/)
    
    
## Web
- link : [월드 와이드 웹(www, World Wide Web)](https://ko.wikipedia.org/wiki/%EC%9B%94%EB%93%9C_%EC%99%80%EC%9D%B4%EB%93%9C_%EC%9B%B9)
- 웹은 전자 메일과 같이 인터넷 상에서 동작하는 하나의 서비스일 뿐이다.
    

    
## 블록체인
- [당장 돈 안되는 암호화폐 커스터디 서비스에 나서는 이유는 ?](https://decenter.kr/NewsView/1VPGUEUY5C/GZ02)
- [생활 속 블록체인 사례](https://m.blog.naver.com/softcamp1999/221416980281)
- [블록체인 개념 정리](https://terms.naver.com/entry.nhn?docId=3578241&cid=59088&categoryId=59096)
- [쉽게 알아보는 블록체인의 원리](https://banksalad.com/contents/%EC%89%BD%EA%B2%8C-%EC%84%A4%EB%AA%85%ED%95%98%EB%8A%94-%EB%B8%94%EB%A1%9D%EC%B2%B4%EC%9D%B8-%EB%B8%94%EB%A1%9D%EC%B2%B4%EC%9D%B8%EC%9D%98-%EC%9B%90%EB%A6%AC-%EC%B1%84%EA%B5%B4-%ED%95%B4%EC%8B%9C-%EA%B7%B8%EB%A6%AC%EA%B3%A0-%EC%9E%91%EC%97%85%EC%A6%9D%EB%AA%85-qvCud)
- [적절한 디앱아키텍처가 왜 중요한가](https://skale.network/blog/danil-hyeongsig-vs-meolticein-wae-jeogjeolhan-diaeb-akitegceoga-jungyohanga)
    
## ETC(알쓸신잡)
- [ARM](https://namu.wiki/w/ARM(CPU))
- [AP(Aplication Processor)](https://www.samsungsemiconstory.com/203) : cpu기능 + 다른장치를 제어하는 칩셋 기능
- [PG사업](https://outstanding.kr/paymentgateway20200311)
    - Payment Gateway
    - **결제** 를 담당하는 회사
    - 온라인에서 물건을 파는 가맹점과 지불 수단을 제공하는 금융사를 이어줌
    - 처리한 거래액 중 일정 비율을 수수료로 번다.
- [랙 서버](https://namu.wiki/w/%EB%9E%99%EB%A7%88%EC%9A%B4%ED%8A%B8)
- 인슈어테크(insurTech)
    - **보험(insurance)** + **기술(technology)**의 합성어
    - 기술과 보험업의 융합
    
    - 대표 사례
        - 레모네이드, 美증시 상장
- [펜데믹](https://ko.wikipedia.org/wiki/%EB%B2%94%EC%9C%A0%ED%96%89) : 전염병이나 감염병이 범지구적으로 유행하는 것.
- [뉴딜정책](https://ko.wikipedia.org/wiki/%EB%89%B4%EB%94%9C)
- [핀테크 와 테크핀](https://m.post.naver.com/viewer/postView.nhn?volumeNo=17217422&memberNo=42188607)
- [visa(wiki)](https://ko.wikipedia.org/wiki/%EB%B9%84%EC%9E%90%EC%B9%B4%EB%93%9C)
- [비자(VISA) 발급](https://m.blog.naver.com/PostView.nhn?blogId=hi_calt&logNo=130135979276&proxyReferer=https:%2F%2Fwww.google.com%2F)
- [master card(wiki)](https://ko.wikipedia.org/wiki/%EB%A7%88%EC%8A%A4%ED%84%B0%EC%B9%B4%EB%93%9C)
- [VC(wiki)](https://ko.wikipedia.org/wiki/%EB%B2%A4%EC%B2%98_%EC%BA%90%ED%94%BC%ED%84%B8)
    
## 탈중앙화 신원증명(DID, Decentralized Identifier)
    
## 워크로드(workload)
- link : [워크로드(제타위키)](https://zetawiki.com/wiki/%EC%9B%8C%ED%81%AC%EB%A1%9C%EB%93%9C)

## 아키텍처 패턴
- 레이어 패턴(Layers pattern)
    - 시스템을 계층으로 구분하여 구성하는 방법
    - 마주보는 두 개의 계층만 상호작용이 가능
    - 특정계층만 교체해 시스템을 개선하는 것이 가능
    - ex) OSI 참조 모델
- 클라이언트-서버 패턴(Client-Server pattern)
    - 하나의 서버 컴포넌트와 다수의 클라이언트 컴포넌트로 구성되는 패턴
    - 사용자 -> 클라이언트 -> 서버 -> 클라이언트 -> 사용자
    - 서버는 클라이언트 요청에 대비해 항상 대기상태 유지
    - 클라이언트나 서버는 요청과 응답을 위해 동기화되는 경우를 제외하면 서로 독립적!
- 파이프-필터 패턴(Pipe-Filter Pattern)
    - 데이터 스트림 절차의 각 단계를 필터(Filter) 컴포넌트로 캡슐화하여 파이프(Pipe)를 통해 데이터를 전송하는 패턴
    - 필터 컴포넌트의 재사용성, 확장 용이성
    - 필터 컴포넌트의 재배치로 다양한 구축 가능
    - 데이터변환, 버퍼링, 동기화 등에 사용
    - ex) UNIX 의 쉘(Shell)
- 모델-뷰-컨트롤러 패턴(MVC Pattern : Model-View-Controller Pattern)
    - 서브시스템을 3개의 부분으로 구조화하는 패턴
        - 모델(Model) : 서브시스템의 핵심 기능과 데이터를 보관
        - 뷰(View) : 사용자에게 정보를 표시
        - 컨트롤러(Controller) : 사용자로부터 받은 입력을 처리
    - 서로 영향을 받지않고 개별작업 수행 가능
    - 한 개의 모델에 여러 개의 뷰를 필요로 하는 '대화형 어플리케이션' 에 적합
- 마스터-슬레이브 패턴(Master-Slave Pattern)
    - 마스터 컴포넌트에서 슬레이브 컴포넌트로 작업을 분할한 후, 슬레이브 컴포넌트에서 처리된 결과물을 다시 돌려받는 방식
        - 마스터 컴포넌트 : 모든 작업의 주체
        - 슬레이브 컴포넌트 : 지시에 따라 작업을 수행 후 결과 반환
    - ex) 장애허용시스템, 병렬 컴퓨팅 시스템
- 브로커 패턴(Broker Pattern)
    - 사용자가 브로커 컴포넌트에 요청 시 요청에 맞는 컴포넌트와 사용자를 연결
    - 원격 서비스 호출에 응답하는 컴포넌트들이 여러 개 있을 때 적합한 패턴
    - ex) 분산 환경 시스템
- 피어-투-피어 패턴
    - 피어(Peer)를 하나의 컴포넌트로 간주함
    - 각 피어는 서비스를 호출하는 클라이언트가 될수도, 서비스를 제공하는 서버가 될 수도 있는 패턴
    - 클라이언트와 서버는 전형적인 '멀티스레딩(multi-threading)'방식을 사용
- 이벤트-버스 패턴(Event-Bus Pattern)
    - 소스가 특정 채널에 이벤트 메시지를 발행(publish)하면, 해당 채널을 구독(subscribe)한 리스너들이 메시지를 받아 이벤트를 처리
    - 4가지 주요 컴포넌트
        - 이벤트를 생성하는 소스(Source)
        - 이벤트를 수행하는 리스너(Listener)
        - 이벤트의 통로인 채널(Channel)
        - 채널들을 관리하는 버스(Bus)
- 블랙보드 패턴(BlackBoard Pattern)
    - 모든 컴포넌트들이 공유 데이터 저장소와 블랙보드 컴포넌트에 접근이 가능한 형태
    - 컴포넌트들은 검색을 통해 블랙보드에서 원하는 데이터를 찾을 수 있음
    - 해결책이 명확하지 않은 문제처리에 유용
    - ex) 음성인식, 차량식별, 신호해석 등...
- 인터프리터 패턴(Interpreter Pattern)
    - 프로그램 코드의 각 라인을 수행하는 방법을 지정하고, 기호마다 클래스를 갖도록 구성
    - 특정 언어로 작성된 프로그램 코드를 해석하는 컴포넌트를 설계할 때 사용
                    
## 이상거래 탐지 시스템(FDS, Fraud Detection System)
- link : [이상거래 탐지 시스템](http://blog.daum.net/mc529/1499)

## 검색엔진 최적화(SEO)
- link : [검색엔진(wiki)](https://ko.wikipedia.org/wiki/%EA%B2%80%EC%83%89_%EC%97%94%EC%A7%84)
- link : [검색엔진 최적화(wiki)](https://ko.wikipedia.org/wiki/%EA%B2%80%EC%83%89_%EC%97%94%EC%A7%84_%EC%B5%9C%EC%A0%81%ED%99%94)

## 데이터 통신 지식
- link : [데이터 통신 지식](https://www.sktinsight.com/87770)

## 엣지 클라우드 컴퓨팅(Edge Cloud Computing)
- 클라우드 컴퓨팅(Cloud Computing)
    - 설명
        - 자신의 컴퓨터가 아닌 다른 컴퓨터로 처리하는 기술
        - 통상적으로 요새 유행하는 클라우드는 중앙집중적 클라우드
        - 대표적으로 구글, 아마존 등 무지막지한 데이터센터를 클라우드 서버로 사용
        - 이를 통해 서비스를 제공
    - 장점
        - 자체 용량을 사용하지 않아도 됨
        - 비용이 절약되고, 간편함
    - 단점
        - 보안 문제
        - 처리를 좀더 예민하게 처리해야하는 경우 빠른속도의 한계를 느낄 수 있음
    
- 엣지 컴퓨팅(Edge Computing)
    - 설명
        - IoT 처럼 자체적으로 데이터를 처리하는 기술
        - 자율주행, 인공지능 등 데이터처리의 신속성에 기민한 경우에 효과를 발휘함
    - 장점
        - 데이터 처리가 신속함
        - 보안이 좋음(기술적으로 좋다기보단 자체적으로 데이터를 보관하기 때문에 집중 데이터보관보다 좋다고 할 수 있음)
    - 단점
        - 비용이 많이 들수 있음
        - 자체용량도 많이 필요함
    
- 엣지 클라우드 컴퓨팅(Edge Cloud Computing)
    - 설명
        - 클라우드와 엣지 컴퓨팅을 결합함으로써 효과를 극대화 시킬 수 있음
        - 최근 5G와 연계하여 기술 붐이 일고 있음.
        - 네트워크 말단에 엣지 클라우드를 두어 데이터처리에 매우 신속하며
        - 중앙클라우드엔 데이터를 보관하는 방식으로 간단한 데이터 교환을 사용함
    - 장점
        - 클라우드와 엣지의 장점을 살리면서 단점을 해소할 수 있음
    - 단점
        - 아직 역할 분담이 모호함
        - 비용과 자원의 사용이 아직 모호함            
    
## port 죽이기
    
### WINDOW
- 현존하는 port 확인 
```
    netstat -ano
```

- port 죽이기
```   
    taskkill /f /pid 10908
```
    
### UNIX
- tomcat 죽이기
```
    sudo pkill -9 -f tomcat
```
    
## 클러스터
- link : [클러스터(wiki)](https://ko.wikipedia.org/wiki/%EC%BB%B4%ED%93%A8%ED%84%B0_%ED%81%B4%EB%9F%AC%EC%8A%A4%ED%84%B0)

## ANSI SQL    
- link : [ANSI SQL 이란?](https://lena19760323.tistory.com/60)
  
## MapReduce
- link : [맵/리듀스 (Map/Reduce) 이해하기](https://cskstory.tistory.com/entry/%EB%A7%B5%EB%A6%AC%EB%93%80%EC%8A%A4-MapReduce-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0)
  
## Spark
- link : [[Spark] 스파크 이해하기](https://12bme.tistory.com/305)
  
## SVN commit 방법
- SVN 폴더에 파일을 넣는다.
- 폴더 field 에 마우스 우측클릭 > commit 클릭
- 넣은 파일 check 후 commit 실시
  
## AS-IS vs To-Be
- As-Is : `'이전의'` 라는 사전적 의미. `현행 프로젝트`
- To-Be : `'미래의'` 라는 사전적 의미. `개선` or `이관 프로젝트`
  
## Agile
- `Agility`
- backlog = (pbs+fbs)+wbs --> `Product Owner` 가 갱신함.
- `scrum`
- daily standup
- kanban
- pmi 기법
- 빨간선과 파란선의 경계를 시점과 관점으로 조율하는 것
- 2주단위 `sprint`
- bottom up
- Being, Doing
- Product Owner + Agile Master + Team Member
    
## Calendar class constant ID 
- 0 : Era
- 1 : Year
- 2 : Month
- 3 : Week-of-year
- 4 : Week-of-month
- 5 : Date/day-of-month
- 6 : Day-of-year
- 7 : Day-of-week
- 8 : Day-of-week-in-month
- 9 : Am/Pm selector
- 10 : Hour
  
## Eclipse에서 search 기능
- Search > search > File 또는 java 등등 원하는 category로 찾을 수 있음.
   
## 전자정부 프레임워크

- 대한민국의 공공부문 정보화 사업 시 플랫폼별 표준화된 개발 프레임워크를 말함
- 특징
    - 개방형 표준 준수 : 오픈소스 기반의 범용화되고 공개된 기술의 활용으로 특정 사업자에 대한 종속성 배제
    - 상용 솔루션 연계 : 사용 솔루션과 연계가 가능한 표준을 제시하여 상호운용성 보장
    - 표준화 지향 : 민, 관, 학계로 구성된 자문협의회를 통해 표준화 수행
    - 변화 유연성 : 각 서비스의 모듈화로 교체가 용이하며 인터페이스 기반 연동으로 모듈간 변경 영향 최소화
    - 편리하고 다양한 환경 제공 : 이클립스 기반의 모델링(UML, ERD), 에디팅, 컴파일링, 디버깅 환경 제공

## .properties 확장자
- link : [properties 확장자](https://ko.wikipedia.org/wiki/.properties)
- 용도 : Spring에서 이를 유용하게 사용할 수 있다.