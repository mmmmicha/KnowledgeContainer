# OOP(Object Oriented Programming)
- link : [(명작)Anti-OOP : if 를 피하고 싶어서](https://redutan.github.io/2016/03/31/anti-oop-if)

- 부모 객체로서 `interface` vs `abstract class`
    - interface
        - 멤버 변수들을 있는 그대로 상속받아 사용해야 한다.
        - 메서드를 구현할 때는 파라미터와 리턴 타입까지는 정해둔채로 내부 로직을 자유자재로 구현할 수 있다.
    - abstract class
        - 멤버 변수들뿐만 아니라 구현되어있는 메서드들의 경우엔 그대로 상속받아 사용해야 한다.
        - `abstract` 라는 제어자를 메서드 앞에 붙임으로써 구현없이 선언만 한 상태로 남겨둘 수도 있다. 자식 객체는 이를 구현해야할 의무가 있다.
- `abstract class`에 대해 implements vs extends
    - ref: https://juunone.netlify.app/typescript/extends/