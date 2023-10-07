# JAVA
- link : [자바 정렬 Java Comparable Comparator 확실히 알고 넘어가기](https://cwondev.tistory.com/15)

## Telegram 봇 API
- link : [Java 를 이용해 Telegram 봇에 메세지 보내기](https://kshman94.tistory.com/40)

## 람다 표현식
- 표현식
```
    (매개변수) -> {함수몸체}
```
- Stream 과의 연계
- link : [람다 표현식](https://futurecreator.github.io/2018/08/26/java-8-streams/)

## stream
- Input/Output stream 이 있으며, 단방향이다.
- `바이트기반 스트림(stream)` 과 `문자기반 스트림(Reader/Writer)` 으로 나뉜다.
- 기본적으로 스트림은 `바이트기반`이며, 바이트 기반을 `문자기반`으로 변환할 수 있다(인코딩방식을 적용해서 변환)

## Set
- 자료구조의 일종.
- List 와 달리 index없이 집합의 개념으로 존재하며, 중복을 허용하지 않는다.
- 동기화를 허용하지 않는다.
- 종류
    - HashSet
        - set 중에 등록되는 순서가 가장 빠르다. 순서가 없다.
    - TreeSet
        - 오름차순이 적용된 set 이다.
    - LinkedHashSet
        - add된 순서대로 출력이 나타나는 set 이다.

## hashCode()
- 모든 클래스의 모체가 되는 Object 클래스의 메소드 중 하나.
- 객체의 hashcode를 반환해주는 메소드
- **참고!! hashcode 는 가상메모리의 주소가 아니라, 객체들을 구별하기위한 구별자**
- **객체가 같으면 hashcode 가 같지만, hashcode가 같다고 해서 객체가 같은 것은 아니다.**
- hashcode() return 값을 16진수로 바꾸게 되면 toString() 메소드를 사용했을때 나오는 return 값에서 **클래스명@(`여기`)** 에 해당하는 값과 같다. 

## 객체비교

- 객체의 비교 방법은 여러가지가 있다.
- `==`, `equals()`, `hashcode()`, `instancof()` 등...
- `==` 과 `equals()` 는 아예 같은 instance 일 경우 true, 다른 경우 false
- `hashcode()`, `toString()` 메소드 역시 아예 같은 instance 일 경우 똑같은 값을 return, 다른 경우 다른 값을 return 하는데 아주 적은 확률로 같은 값이 나올 수도 있다. (**중요!! 그렇다고 hashcode가 같다고해서 equals() 와 == 에서 true 가 나오는건 아니다. 내부 해싱알고리즘..**)

## String.equals(null) 과 NULL.equals(String) 의 차이
- 후자의 경우 `NullpointerException` 이 발생한다. 주의할 것.

## Map 과 List 의 차이
- List
    - 장점
        - 데이터 저장속도가 빠름
        - 데이터를 순차적으로 저장함
    - 단점
        - 원하는 index에 삽입/삭제 시 비효율(해당 index 아래의 데이터들을 배열에 copy 후 다시 붙여넣어야 함)
- Map 
    - 장점
        - 특정데이터를 search 하기에 매우 유리(List 보다 삽입/삭제 에서도 빠름)
    - 단점
        - List 보다 데이터 저장속도가 느림

## 변수 정리
- `static변수 == 클래스 변수 == 정적 변수` <--> `non-static변수 == 인스턴스 변수 == 동적 변수`
- `멤버 == 필드 == 전역변수` <--> `지역변수`

## 초기화 블럭
- static 블럭
    - 클래스가 로드될 때 초기화를 실행하고 그 후엔 실행되지 않음.
- 인스턴스 블럭
    - 인스턴스가 생성될 때마다 초기화를 실행함.
- 작동 순서
```
    static 블럭 > 인스턴스 블럭 > 생성자
```