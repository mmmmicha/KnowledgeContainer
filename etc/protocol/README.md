# PROTOCOL

## HTTP

- request `body`에 `content-type: application/json`인 경우
  - `date`는 Object는 string으로 알아서 변환된다
  - `number`는 number로 값 전달이 가능하다

### PathVariable 과 QueryStringParameter 의 차이

- Path Variable
  ```
      localhost:8080/delete/123
  ```
  - 경로 상 parameter 를 넘기는 것
  - delete에 주로 쓸 수 있음
  - `required`조건인 값을 사용한다.
- Query String Parameter
  ```
      localhost:8080/put?id=321&name=예제
  ```
  - ? 뒤에 넘기게 되는 parameter를 지칭함
  - 주로 get방식에 쓰인다.
  - `optional`조건인 값을 사용한다.

### Content-Type

- multipart/form-data vs application/json
  - plain object 에 undefined 필드를 담는가 안담는가?

## ZWave

- link : [Z-Wave 란?](https://blog.naver.com/owcred601/220623424615)

## BLE

- link : [Bluetooth Low Energy(BLE) 파헤치기](https://medium.com/@zoyi_product/bluetooth-low-energy-ble-84b03705ffca)
