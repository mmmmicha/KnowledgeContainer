# 지식창고

- <b>엣지 클라우드 컴퓨팅(Edge Cloud Computing)</b> 
    >- 클라우드 컴퓨팅(Cloud Computing)
    
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
            
    >- 엣지 컴퓨팅(Edge Computing)
    
        - 설명
            - IoT 처럼 자체적으로 데이터를 처리하는 기술
            - 자율주행, 인공지능 등 데이터처리의 신속성에 기민한 경우에 효과를 발휘함
        - 장점
            - 데이터 처리가 신속함
            - 보안이 좋음(기술적으로 좋다기보단 자체적으로 데이터를 보관하기 때문에 집중 데이터보관보다 좋다고 할 수 있음)
        - 단점
            - 비용이 많이 들수 있음
            - 자체용량도 많이 필요함
            
     >- 엣지 클라우드 컴퓨팅(Edge Cloud Computing)
     
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

- <b>.crf file</b> 
    >- 설명
    
        - Cal3D Binary Materials File
        - XML 형식으로 저장하는 .XRF 형식의 2진버전

- <b>[Java]람다 표현식</b>
    >- 표현식
    
        - (매개변수) -> {함수몸체}
        
    >- Stream 과의 연계
    >- link : https://futurecreator.github.io/2018/08/26/java-8-streams/
        

- <b>Session</b>
    >- HttpSession
    
        - HttpSession session = request.getSession(true) // session 생성
        - 이 session 객체는 서버에 저장됨
        - 서버 Container에 의해 관리되는 servlet들은 이 session을 공유함
        - session lifetime은 web.xml에 지정할 수 있음
        - Object session.getAttribute(키)
            - 명시적 형변환 필요
        - session.setAttribute(키, 값)
        
    >- @SessionAttribute
    
        - 파라미터 scope 에 쓰임
        - @SessionAttribute 값타임 키
        - 명시적 형변환을 필요없게 해줌
        - 사용이 한정적
        
    >- @SessionAttributes
    
        - 클래스명 위에 사용하는 어노테이션
        - 해당 어노테이션이 쓰여있는 클래스 내에서만!! Session 공유가 가능하다(큰 단점일 수 있음)
        - @SessionAttributes("UserNm", "PWD", ...)
        - Model 객체와 연관됨
            - model.setAttribute("UserNm", "정광현") // session 에 저장이 됨.

- <b>port 죽이기</b>
    >- 현존하는 port 확인
       
        - netstat -ano
       
    >- port 죽이기
       
        - taskkill /f /pid 10908

- <b>클러스터란?</b>
    >- link : https://ko.wikipedia.org/wiki/%EC%BB%B4%ED%93%A8%ED%84%B0_%ED%81%B4%EB%9F%AC%EC%8A%A4%ED%84%B0

- <b>ANSI SQL 이란?</b>
    >- link : https://lena19760323.tistory.com/60
  
- <b>MapReduce 란?</b>
    >- link : https://cskstory.tistory.com/entry/%EB%A7%B5%EB%A6%AC%EB%93%80%EC%8A%A4-MapReduce-%EC%9D%B4%ED%95%B4%ED%95%98%EA%B8%B0
  
- <b>Spark 란?</b>
    >- link : https://12bme.tistory.com/305
  
- <b>MongoDB 란?</b>
    > - link : http://bigmatch.i-um.net/2013/12/09/mongodb%EB%A5%BC-%EC%93%B0%EB%A9%B4%EC%84%9C-%EC%95%8C%EA%B2%8C-%EB%90%9C-%EA%B2%83%EB%93%A4/
    
    > 1. 대표적인 NoSQL
    > 2. JSON 을 sql로 파싱하지않고 저장한다.
  
- <b>SVN commit 방법</b>
  
    > 1. SVN 폴더에 파일을 넣는다.
    > 2. 폴더 field 에 마우스 우측클릭 > commit 클릭
    > 3. 넣은 파일 check 후 commit 실시
  
- <b>AS-IS vs To-Be</b>
    
    > - As-Is : '이전의' 라는 사전적 의미. 현행 프로젝트
    > - To-Be : '미래의' 라는 사전적 의미. 개선 or 이관 프로젝트
  
- <b>Agile</b>
    
    > - Agility
    > - backlog = (pbs+fbs)+wbs // Product Owner 가 갱신함.
    > - scrum
    > - daily standup
    > - kanban
    > - pmi 기법
    > - 빨간선과 파란선의 경계를 시점과 관점으로 조율하는 것
    > - 2주단위 sprint
    > - bottom up
    > - Being, Doing
    > - Product Owner + Agile Master + Team Member
  
- <b>merge into란?</b>
  
    > - 해당 테이블에 key가 존재한다면 update, 존재하지 않는다면 insert
    > - Java 자료구조중 getOrDefault() 메소드가 
    > - link : https://m.blog.naver.com/PostView.nhn?blogId=wiseyoun07&logNo=220319875065&proxyReferer=https:%2F%2Fwww.google.com%2F

- <b>index란?</b>
  
    > - 일종의 DB 주소록
    > - link : https://rongscodinghistory.tistory.com/113

- <b>PF Key란?</b>
   
    > - Primary key임과 동시에 Forien Key인 Key를 말함.
    > - 주로 Composite Key(복합키) 로 사용된다.
    > - 독립적으로 사용되는지는 의문이다.
  
- <b>$(document).ready() 를 쓰는 이유는?</b>
  
    > 1. $(document).ready() 를 쓰는 이유는 jquery를 기본적으로 load 하기 위해서가 아니라 html을 전체적으로 로딩한 후에 javascript 코드를 적용하기 위해서이다.
    > 2. 즉, <script> 태그를 만나게 되면 렌더링을 멈추고 이를 처리하게 되는데 그래서 렌더링을 다 하고 body 태그 내 마지막에 link 태그를 둠으로써 사용자에게 렌더링요소를 먼저 보여지게 하는 것이다.
    > 3. ready를 사용하게 되면 렌더링을 다 마치고 javascript 처리를 시작하기 때문에 body 마지막에 link를 놓을 필요가 없어진다.
    
- <b>docker란?</b>
  
    > - wiki : https://ko.wikipedia.org/wiki/%EB%8F%84%EC%BB%A4_(%EC%86%8C%ED%94%84%ED%8A%B8%EC%9B%A8%EC%96%B4)
  
    > 1. Container 관리 플랫폼 
    > 2. Container 와 image 가 매우 중요<br>
         - image : Container 에 대한 A to Z 를 모두 가지고 있는 파일<br>
           - 이 때문에 다른 라이브러리가 필요없음.
    > 3. 레이어 저장방식이 유용함<br>
         - 버젼업이 되거나 파일이 추가될 경우 전체 파일을 다시 배포하는 것이 아니라 추가된 파일만 새로운 layer 로 추가되는 형식.
       
- <b>쿠버네티스(Kubernetes) vs 도커(Docker)</b>
  
    > - keyword : 컨테이너와 오케스트레이션의 이해
    > - link : http://www.itworld.co.kr/news/135282
       
- <b>Calendar class constant ID?</b> 
  
    > 0 : Era<br>
    > 1 : Year<br>
    > 2 : Month<br>
    > 3 : Week-of-year<br>
    > 4 : Week-of-month<br>
    > 5 : Date/day-of-month<br>
    > 6 : Day-of-year<br>
    > 7 : Day-of-week<br>
    > 8 : Day-of-week-in-month<br>
    > 9 : Am/Pm selector<br>
    > 10 : Hour
  
- <b>Eclipse에서 search 기능</b>
 
   > -Search>search>File 또는 java 등등 원하는 category로 찾을 수 있음.
   
- <b>Map 과 List 의 차이</b>
 
   > 1. List
   
       - 장점 : 데이터 저장속도가 빠름, 데이터를 순차적으로 저장함
       - 단점 : 원하는 index에 삽입/삭제 시 비효율(해당 index 아래의 데이터들을 배열에 copy 후 다시 붙여넣어야 함)
   
   > 2. Map
   
       - 장점 : 특정데이터를 search 하기에 매우 유리(List 보다 삽입/삭제 에서도 빠름)
       - 단점 : List 보다 데이터 저장속도가 느림
  
- <b>변수 정리</b>
 
   > 1. static변수 == 클래스 변수 == 정적 변수 <--> non-static변수 == 인스턴스 변수 == 동적 변수
   
   > 2. 멤버 == 필드 == 전역변수 <--> 지역변수
   
- <b>DECODE 함수</b>
 
   > - DECODE(컬럼, 조건1, 결과1, 조건2, 결과2, 조건3, 결과3..........) 

- <b>초기화 블럭</b>
 
   > 1. static 블럭
   
        - 클래스가 로드될 때 초기화를 실행하고 그 후엔 실행되지 않음.
     
   > 2. 인스턴스 블럭
   
        - 인스턴스가 생성될 때마다 초기화를 실행함.
   
   > 3. 작동 순서
   
        - static 블럭 > 인스턴스 블럭 > 생성자

- <b>하둡(Hadoop) 이란?</b>
    
   > wiki : https://ko.wikipedia.org/wiki/%EC%95%84%ED%8C%8C%EC%B9%98_%ED%95%98%EB%91%A1
 
   > - 대용량 데이터를 분산처리할 수 있는 자바 기반의 오픈소스 프레임워크이다.
   > - 분산파일시스템(HDFS) + 분산처리시스템(MapReduce)
   
   > - 주요 특징
   
       1. 데이터가 있는 곳에서 로직을 처리할 수 있음.
       2. x86 서버에 설치 할 수 있음
       3. 하드웨어 장애를 피할 수 없다는 가정하에 설계됨
       4. 서버(노드)를 추가하면, 선형적인 기능확장을 할 수 있음.
       5. 다수의 클러스트를 하나의 스토리지처럼 사용할 수 있음.
     
 
- <b>stream 이란?</b>
 
   > - Input/Output stream 이 있으며, 단방향이다.
   > - 바이트기반 스트림(stream) 과 문자기반 스트림(Reader/Writer)으로 나뉜다.
   > - 기본적으로 스트림은 바이트기반이며, 바이트 기반을 문자기반으로 변환할 수 있다(인코딩방식을 적용해서 변환)
   
 - <b>Set 이란?</b>
 
   > - 자료구조의 일종.
   > - List 와 달리 index없이 집합의 개념으로 존재하며, 중복을 허용하지 않는다.
   > - 동기화를 허용하지 않는다.
   
   > - 종류
   
       - HashSet : set 중에 등록되는 순서가 가장 빠르다. 순서가 없다.
       - TreeSet : 오름차순이 적용된 set 이다.
       - LinkedHashSet : add된 순서대로 출력이 나타나는 set 이다.
     
- <b>hashCode() 이란?</b>
 
   > - 모든 클래스의 모체가 되는 Object 클래스의 메소드 중 하나.
   > - 객체의 hashcode를 반환해주는 메소드
   
       (hashcode 는 가상메모리의 주소가 아니라, 객체들을 구별하기위한 구별자)
   
   > - 중요! 객체가 같으면 hashcode 가 같지만, hashcode가 같다고 해서 객체가 같은 것은 아니다.
   > - hashcode() return 값을 16진수로 바꾸게 되면 toString() 메소드를 사용했을때 나오는 return 값에서 "클래스명@(여기)" 에 해당하는 값과 같다. 
   
- <b>객체비교</b>
 
   > - 객체의 비교 방법은 여러가지가 있다.
   > - ==, equals(), hashcode(), instancof() 등...
   > - == 과 equals() 는 아예 같은 instance 일 경우 true, 다른 경우 false
   > - hashcode(), toString() 메소드 역시 아예 같은 instance 일 경우 똑같은 값을 return, 다른 경우 다른 값을 return 하는데 아주 적은 확률로 같은 값이 나올 수도 있다. (중요!! 그렇다고 hashcode가 같다고해서 equals() 와 == 에서 true 가 나오는건 아니다. 내부 해싱알고리즘..)
   
 - <b>전자정부 프레임워크란?</b>
   
   > - 대한민국의 공공부문 정보화 사업 시 플랫폼별 표준화된 개발 프레임워크를 말함
   > - 특징
     
       1. 개방형 표준 준수 : 오픈소스 기반의 범용화되고 공개된 기술의 활용으로 특정 사업자에 대한 종속성 배제
       2. 상용 솔루션 연계 : 사용 솔루션과 연계가 가능한 표준을 제시하여 상호운용성 보장
       3. 표준화 지향 : 민, 관, 학계로 구성된 자문협의회를 통해 표준화 수행
       4. 변화 유연성 : 각 서비스의 모듈화로 교체가 용이하며 인터페이스 기반 연동으로 모듈간 변경 영향 최소화
       5. 편리하고 다양한 환경 제공 : 이클립스 기반의 모델링(UML, ERD), 에디팅, 컴파일링, 디버깅 환경 제공

- <b>@RestController 란?</b>
   
   > - @Controller 는 view 객체를 리턴할 수 있는 기능을 제공해주지만, @RestController는 문자열과 JSON 등을 전송할 수 있는 기능을 추가제공한다.
   
 - <b>@Service 란?</b>
   
   > - @Service 는 Controller 와 Repository 를 연결해주는 역할로, SpringMVC에 특화된 어노테이션이다.
   
- <b>String.equals(null) 과 NULL.equals(String) 의 차이?</b>
   
   > - 후자의 경우 NullpointerException 이 발생한다. 주의할 것.
   
- <b>.properties 확장자</b>
   
   > - link : https://ko.wikipedia.org/wiki/.properties
   > - 용도 : Spring에서 이를 유용하게 사용할 수 있다.

- <b>Context path, root란?</b>
   > - Context Path : 프로젝트 명을 의미하며 url의 호스트, 포트명 다음에 나온다.<br> 
   > - Context root : Content directory의 경로. 해당 경로에 메타 정보와 웹 정보를 관리하는 META-INF와 WEB-INF 파일이 자동생성되며 JSP파일은 여기 하위에 저장되어야 경로를 찾을 수 있다.
   
