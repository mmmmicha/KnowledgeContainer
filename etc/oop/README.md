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

    - 상위 객체는 언제든 하위 객체로 치환될 수 있어야 한다.
    - 핵심은 상위 객체가 선언해둔 메서드들의 책임이 하위 객체에서 변경되면 안된다는 것이다.
    - 가령 부모 객체에서 선언된 메서드가 멤버 변수의 조합을 리턴하도록 설계됐는데 자식 객체에서 이를 오버라이드하면서 에러를 던지게 만든다면 이는 LSP를 위반하는 것이다.

      ```ts
      class Cat {
        public speak() {
          console.log("meow");
        }
      }

      class BlackCat extends Cat {
        public speak() {
          console.log("black meow");
        }
      }

      class Fish extends Cat {
        public speak() {
          throw new Error("Error!!");
        }
      }

      // const cat: Cat = new Cat();
      // cat.speak(); // 기대한대로 동작 O
      // const cat: Cat = new BlackCat();
      // cat.speak(); // 기대한대로 동작 O
      const cat: Cat = new Fish();
      cat.speak(); // 기대한대로 동작 X
      ```

- ISP(Interface-Segregation Principle)

  - 인터페이스 분리 원칙

    - 클라이언트들이 사용하지 않는 메서드들에 의존하게 만들어서는 안된다.
    - 원형의 역할을 할 인터페이스는 책임을 분명히 하여 최소단위로 설계되어야 한다.
    - 가령 수륙양용차는 보트의 성격과 차의 성격을 둘 다 지니게 되는데 이는 보트 인터페이스와 차 인터페이스를 둘 다 구현하면 될 일이다. 이 둘의 성격을 굳이 수륙양용차라는 인터페이스에 섞어놓는다면 이를 구현하는 차량 또는 보트 객체들이 `불필요한 메서드에 의존`하게 될 가능성이 높아진다.

      ```ts
      interface CarBoat {
        // Car의 특징
        public drive();
        public turnLeft();
        public turnRight();

        // Boat의 특징
        public steer();
        public steerLeft();
        public steerRight();
      }

      class Genesis implements CarBoat {
        // Car의 특징
        public drive();
        public turnLeft();
        public turnRight();

        // 불필요하나 구현해야함
        // Boat의 특징
        // public steer();
        // public steerLeft();
        // public steerRight();
      }
      ```

- DIP(Dependency-Inversion Principle)

  - 의존 역전 원칙

    - 직접 의존관계에 있는 두 객체 사이에 `추상화 레이어`를 추가함으로써 두 객체의 의존 병향이 모두 추상화 레이어를 향하도록 만든다.

      ```ts
      // soldier가 sword를 직접 의존하고 있는 상황
      class Sword {}
      class Soldier {
        private weapon: Sword;
        public constructor(weapon: Sword) {
          this.weapon = weapon;
        }
      }

      // soldier가 추상화된 weapon을 직접 의존하고 sword도 weapon을 의존하게되면서 의존 방향이 역전
      interface Weapon {}
      class Sword implements Weapon {}
      class Soldier {
        private weapon: Weapon;
        public constructor(weapon: Weapon) {
          this.weapon = weapon;
        }
      }
      ```
