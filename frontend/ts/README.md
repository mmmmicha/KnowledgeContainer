# TS(typescript)

- link : [type extend](https://pro-growth.tistory.com/entry/Typescript%ED%83%80%EC%9E%85%EB%B3%80%EC%88%98%EC%97%90-%EB%8B%B4%EA%B8%B0type-alias-%ED%83%80%EC%9E%85-extend%ED%95%98%EA%B8%B0)
- link : [!. 단언연산자](https://inpa.tistory.com/entry/TS-%F0%9F%93%98-%ED%83%80%EC%9E%85%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EB%8A%90%EB%82%8C%ED%91%9C-Non-null-%EB%8B%A8%EC%96%B8-%EC%97%B0%EC%82%B0%EC%9E%90)

## 덕타이핑

## 제네릭함수

- 함수에 제네릭 함수를 유용하게 사용할 수 있는 방법을 제시한다.
- `extends`를 사용하는 방법을 `제네릭 제약 조건` 이라는 명칭으로 사용한다.

  - case1) `extends`를 사용하여 범용적으로 타이핑을 할 수 있다. `덕타이핑`이라는 기술을 이용하여 적용한 예시이다.

    ```ts
    type Cats = {
      id: string;
      name: string;
      age: number;
      kind: string;
    };

    const updateCatInfo = <T extends { id: string; name: string }>(cat: T) => {
      console.log(`cat: ${cat}`);
    };

    console.log(
      updateCatInfo({
        id: 1,
        name: "가필드",
        age: 3,
        kind: "something",
      })
    );
    ```

## void

- `void`는 js에는 없고 ts에서만 사용할 수 있는 타입이다.
  - 기본적으로 js에서 undefined값들을 리턴하던 함수들의 경우를 ts에선 해당 리턴타입을 void로 나타낸다.
- `() => void`
  ```ts
  const a: () => void = () => 3; // 문제 없음
  const b = (): void => {
    return 3;
  }; // 문제 있음
  ```
  - `a`의 특징은 자바스크립트에서 많이 사용되는 콜백함수와 연관이 있는데, 콜백함수들은 단순히 실행이 목적이고 리턴값은 중요하지 않다. 예를 들어 `forEach(callback)`의 경우 `forEach(callback: () => void)` 이런식으로 메개변수의 타입을 갖게 되면 리턴타입이 어떠하든지 모든 함수들을 허용할 수 있다. 이런 부분에서 유용하게 사용이 가능하다.
  - `b`의 특징은 함수의 선언시 타입 에러 발생을 통해 목적과 맞지 않는 코딩을 방지해준다. 리턴타입을 `void`로 설정했다는 말은 말그대로 리턴에 값을 주지 않겠다는 의미인데, 값을 줬을 때 에러를 발생시키는 것이다.
  - 결론적으로 a, b의 두 가지 특징을 통해 void라는 타입을 유연하게 사용할 수 있다.
