# Test
## Jest
## mock
- `jest.spyOn(object, method)`
    - 특정 object내에 존재하는 method가 동작하는 걸 감시할 수 있다.
    - mocking과는 달리 실제로 동작하는 함수(목업에도 spy를 달 수는 있다)를 그저 감시하는 것 뿐이다.
    - 함수가 특정조건에서 call이 되어야하는지 아닌지를 테스트해볼 때 유용하게 사용할 수 있다.
- `jest.fn()`을 통해 비동기 함수를 mocking하는 방법
    ```ts
    jest.fn(() => Promise.resolve({ data: {} }))
    ```
## expect
- describe안에서는 곧바로 `expect`를 사용하여 비교할 수 없다.

## TDD
- TDD vs BDD


