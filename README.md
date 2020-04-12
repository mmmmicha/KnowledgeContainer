# 지식창고

  - <b>$(document).ready() 를 쓰는 이유는?</b>
  
    $(document).ready() 를 쓰는 이유는 jquery를 기본적으로 load 하기 위해서가 아니라 html을 전체적으로 로딩한 후에 javascript 코드를 적용하기 위해서이다.

    즉, <script> 태그를 만나게 되면 렌더링을 멈추고 이를 처리하게 되는데 그래서 렌더링을 다 하고 body 태그 내 마지막에 link 태그를 둠으로써 사용자에게 렌더링요소를 먼저 보여지게 하는 것이다.

    ready를 사용하게 되면 렌더링을 다 마치고 javascript 처리를 시작하기 때문에 body 마지막에 link를 놓을 필요가 없어진다.
    
  - <b>docker란?</b>
  
    1. Container 관리 플랫폼

    2. Container 와 image 가 매우 중요
       image : Container 에 대한 A to Z 를 모두 가지고 있는 파일
       - 이 때문에 다른 라이브러리가 필요없음.

    3. 레이어 저장방식이 유용함
       - 버젼업이 되거나 파일이 추가될 경우 전체 파일을 다시 배포하는 것이 아니라 추가된 파일만 새로운 layer 로 추가되는 형식.
  
