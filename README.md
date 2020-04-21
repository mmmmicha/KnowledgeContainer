# 지식창고

  - <b>$(document).ready() 를 쓰는 이유는?</b>
  
    1. $(document).ready() 를 쓰는 이유는 jquery를 기본적으로 load 하기 위해서가 아니라 html을 전체적으로 로딩한 후에 javascript 코드를 적용하기 위해서이다.

    2. 즉, <script> 태그를 만나게 되면 렌더링을 멈추고 이를 처리하게 되는데 그래서 렌더링을 다 하고 body 태그 내 마지막에 link 태그를 둠으로써 사용자에게 렌더링요소를 먼저 보여지게 하는 것이다.

    3. ready를 사용하게 되면 렌더링을 다 마치고 javascript 처리를 시작하기 때문에 body 마지막에 link를 놓을 필요가 없어진다.
    
  - <b>docker란?</b>
  
    1. Container 관리 플랫폼

    2. Container 와 image 가 매우 중요
       image : Container 에 대한 A to Z 를 모두 가지고 있는 파일
       - 이 때문에 다른 라이브러리가 필요없음.

    3. 레이어 저장방식이 유용함
       - 버젼업이 되거나 파일이 추가될 경우 전체 파일을 다시 배포하는 것이 아니라 추가된 파일만 새로운 layer 로 추가되는 형식.
       
  - <b>Calendar class constant ID?</b> 
  
    0 : Era<br>
    1 : Year<br>
    2 : Month<br>
    3 : Week-of-year<br>
    4 : Week-of-month<br>
    5 : Date/day-of-month<br>
    6 : Day-of-year<br>
    7 : Day-of-week<br>
    8 : Day-of-week-in-month<br>
    9 : Am/Pm selector<br>
   10 : Hour
  
 - <b>Eclipse에서 search 기능</b>
 
   Search>search>File 또는 java 등등 원하는 category로 찾을 수 있음.
   
 - <b>Map 과 List 의 차이</b>
 
   1. List
      - 장점 : 데이터 저장속도가 빠름, 데이터를 순차적으로 저장함
      - 단점 : 원하는 index에 삽입/삭제 시 비효율(해당 index 아래의 데이터들을 배열에 copy 후 다시 붙여넣어야 함)
   
   2. Map
      - 장점 : 특정데이터를 search 하기에 매우 유리(List 보다 삽입/삭제 에서도 빠름)
      - 단점 : List 보다 데이터 저장속도가 
  
 - <b>변수 정리</b>
 
   1. static변수 == 클래스 변수 == 정적 변수 <--> non-static변수 == 인스턴스 변수 == 동적 변수
   
   2. 멤버 == 필드 == 전역변수 <--> 지역변수
   
 - <b>DECODE 함수</b>
 
   - DECODE(컬럼, 조건1, 결과1, 조건2, 결과2, 조건3, 결과3..........) 

 - <b>초기화 블럭</b>
 
   1. static 블럭
      - 클래스가 로드될 때 초기화를 실행하고 그 후엔 실행되지 않음.
     
   2. 인스턴스 블럭
      - 인스턴스가 생성될 때마다 초기화를 실행함.
   
   3. 작동 순서
      - static 블럭 > 인스턴스 블럭 > 생성자

 - <b>하둡(Hadoop) 이란?</b>
 
   - 대용량 데이터를 분산처리할 수 있는 자바 기반의 오픈소스 프레임워크이다.
   - 분산파일시스템(HDFS) + 분산처리시스템(MapReduce)
   
   - 주요 특징
     1. 데이터가 있는 곳에서 로직을 처리할 수 있음.
     2. x86 서버에 설치 할 수 있음
     3. 하드웨어 장애를 피할 수 없다는 가정하에 설계됨
     4. 서버(노드)를 추가하면, 선형적인 기능확장을 할 수 있음.
     5. 다수의 클러스트를 하나의 스토리지처럼 사용할 수 있음.
     
 - <b>웹스퀘어5(Websquare5) 란?</b>    

   - 국내 최초의 WYSIWYG 개발 도구가 포함된 HTML5 웹 표준 UI 플랫폼으로 최신의 선진 신기술과 개념, 다양한 구축 경험과 방법론을 집대성하여 HTML5를 완벽히 지원할 수 있는 HTML5 웹표준 UI 플랫폼. 
   - No Active X, No Runtime, Only Standard 를 가능케 함.
   
   - 특징
     1. Open Architecture
     2. HTML5 Standards 적용
     3. Adaptive Web Component 제공
     4. One Source Multi Use 지원
     5. 통합개발도구 지원

 - <b>stream 이란?</b>
 
   - Input/Output stream 이 있으며, 단방향이다.
   - 바이트기반 스트림(stream) 과 문자기반 스트림(Reader/Writer)으로 나뉜다.
   - 기본적으로 스트림은 바이트기반이며, 바이트 기반을 문자기반으로 변환할 수 있다(인코딩방식을 적용해서 변환)
   
 - <b>Set 이란?</b>
 
   - 자료구조의 일종.
   - List 와 달리 index없이 집합의 개념으로 존재하며, 중복을 허용하지 않는다.
   - 동기화를 허용하지 않는다.
   
   - 종류
     - HashSet : set 중에 등록되는 순서가 가장 빠르다. 순서가 없다.
     - TreeSet : 오름차순이 적용된 set 이다.
     - LinkedHashSet : add된 순서대로 출력이 나타나는 set 이다.
     
 - <b>hashCode() 이란?</b>
 
   - 모든 클래스의 모체가 되는 Object 클래스의 메소드 중 하나.
   - 객체의 hashcode를 반환해주는 메소드
     (hashcode 는 가상메모리의 주소가 아니라, 객체들을 구별하기위한 구별자)
   - 중요! 객체가 같으면 hashcode 가 같지만, hashcode가 같다고 해서 객체가 같은 것은 아니다.
   - hashcode() return 값을 16진수로 바꾸게 되면 toString() 메소드를 사용했을때 나오는 return 값에서 "클래스명@(여기)" 에 해당하는 값과 같다. 
   
 - <b>객체비교</b>
 
   - 객체의 비교 방법은 여러가지가 있다.
   - ==, equals(), hashcode(), instancof() 등...
   - == 과 equals() 는 아예 같은 instance 일 경우 true, 다른 경우 false
   - hashcode(), toString() 메소드 역시 아예 같은 instance 일 경우 똑같은 값을 return, 다른 경우 다른 값을 return 하는데 아주 적은 확률로 같은 값이 나올 수도 있다.
   
