# Test

## supertest

- `Test` 객체에 `field()`메서드를 사용할 때의 유의 사항

  - `field(key, value)` 에서 key를 이미 등록한 값 외에 중복으로 등록할 경우 value값이 자동적으로 배열타입으로 변경되면서 값이 overlap이 아닌 appending이 된다.

    ```ts
    import request from "supertest";

    const result = request
      .post(baseUrl)
      .set(something)
      .field("name", "dog")
      .field("name", "cat");
      /**
       * request body {
       *    name: ["dog", "cat"]
       * }
       * /
    ```

## Jest

### mock

- `jest.mock(path, factory: () => any, option?)`
  - 파일 내 있는 메서드들을 대거 mocking할 때 사용한다.
  ```ts
  // test.ts
  export const add = (a: number, b: number) => a + b;
  // something.spec.ts
  import * as addmodule from "./test";
  const mockAddModule = {
    add: jest.fn(),
  };
  jest.mock("./test", () => mockAddModule);
  mockAddModule.add.mockResolvedValueOnce(null);
  ```
- `jest.spyOn(object, method)`
  - 특정 object내에 존재하는 method가 동작하는 걸 감시할 수 있다.
  - mocking과는 달리 실제로 동작하는 함수(목업에도 spy를 달 수는 있다)를 그저 감시하는 것 뿐이다.
  - 함수가 특정조건에서 call이 되어야하는지 아닌지를 테스트해볼 때 유용하게 사용할 수 있다.
  - 주의사항
    - 하나의 describe 스코프 안에서 it를 여러개 수행하는 데 똑같은 스파이를 지정할 경우 stack을 공유하게 된다.
      - 이에 따라 `spy.mockClear()`를 it의 끝부분에 해주면 해결할 수 있다.
- `jest.fn()`을 통해 비동기 함수를 mocking하는 방법
  ```ts
  jest.fn(() => Promise.resolve({ data: {} }));
  ```

### expect

- describe안에서는 곧바로 `expect`를 사용하여 비교할 수 없다.

## TDD

- TDD vs BDD
