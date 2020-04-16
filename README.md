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
     
