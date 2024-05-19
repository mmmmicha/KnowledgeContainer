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
