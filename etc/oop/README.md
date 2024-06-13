# OOP(Object Oriented Programming)

- link : [Growing Application - 2nd. 애플리케이션 아키텍처와 객체지향](https://www.youtube.com/watch?v=26S4VFUWlJM)
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

## SOLID Principle

- SRP(Single-Responsibility Principle)
  - 단일 책임 원칙
    - 객체는 단일 책임을 지녀야만 한다.
    - 객체가 변경될 이유는 단 한가지 때문이어야만 한다.
- OCP(Open-Closed Principle)

  - 개방 폐쇄 원칙

    - 객체는 확장에는 열려있고 수정에는 닫혀있어야 한다.
      - 즉, 확장을 위한 수정이 필요하지 않아야 한다.

    ```ts
    // 위반 케이스
    class Animal {
      public speak(type: string) {
        if (type === "cat") {
          return "mew";
        } else if (type === "dog") {
          return "walwal";
        } else {
          throw new Error("Invalid type");
        }
      }
    }

    // 올바른 케이스
    // 확장에 따라 수정할 필요 x
    interface Animal {
      public speak();
    }
    // 확장
    class Cat implements Animal {
      public speak() {
        return "mew";
      }
    }
    // 확장
    class Dog implements Animal {
      public speak() {
        return "walwal";
      }
    }
    ```

- LSP(Liskov-Substitution Principle)
  - 리스코프 치환 원칙
    - 자세히 공부 더 필요
- ISP(Interface-Segregation Principle)
  - 인터페이스 분리 원칙
    - 자세히 공부 더 필요
- DIP(Dependency-Inversion Principle)
  - 의존 역전 원칙
    - 정리 추가적으로 필요
