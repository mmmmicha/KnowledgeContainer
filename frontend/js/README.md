# JS(javascript)

- link : [bind()](https://ko.javascript.info/bind)
- link : [reduce()](https://miiingo.tistory.com/365)
<!-- 2023.10.18 -->
- link : [promise.all() vs promise.allSettled()](https://inpa.tistory.com/entry/JS-%F0%9F%93%9A-%EB%8D%94%EC%9D%B4%EC%83%81-Promiseall-%EC%93%B0%EC%A7%80%EB%A7%90%EA%B3%A0-PromiseallSettled-%EC%82%AC%EC%9A%A9%ED%95%98%EC%9E%90)
- link : [classes](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Classes)
- link : [prototype chains](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Inheritance_and_the_prototype_chain)
- link : [anonymous functions](https://www.javascripttutorial.net/javascript-anonymous-functions/)
- link : [for vs foreach](https://stackoverflow.com/questions/43031988/javascript-efficiency-for-vs-foreach)
<!-- 2023.10.09 -->
- link : [javascript engine 동작의 완전 이해](https://www.youtube.com/watch?v=8aGhZQkoFbQ)
<!-- 2023.10.07 -->
- link : [null 병합 연산자 '??' 와 OR 연산자 '||' 의 차이](https://bbaktaeho-95.tistory.com/48)

- link : [Why You Should Think Twice Before Using console.log, and Tips for Avoiding Performance Pitfalls](https://medium.com/@xiaweiliang94/why-you-should-think-twice-before-using-console-log-and-tips-for-avoiding-performance-pitfalls-1228efc27360)
    - 정리하자면, console.log() 에 사용되는 argument를 string으로 serialization하는 과정에서 메모리소요가 커져서 퍼포먼스에 영향을 끼치는게 저명하다.

<!-- 우선 기록해둠. 좀 더 좋은 레퍼런스 찾아야함 -->
- link : [sort() 내장 함수는 어떤 알고리즘으로 동작하는가?](https://choyeon-dev.tistory.com/entry/JavaScript%EC%9D%98-sort%EB%8A%94-%EC%96%B4%EB%96%A4-%EC%A0%95%EB%A0%AC-%EC%95%8C%EA%B3%A0%EB%A6%AC%EC%A6%98%EC%9D%84-%EC%82%AC%EC%9A%A9%ED%95%A0%EA%B9%8C)

## Array
- Filter(callbackFn) 에 return 값으로 비교문이 아닌 대입문을 실수로 넣었는데 동작했던 건에 대하여..
- ```array.flat```을 사용하면 2차원배열을 1차원배열로 플랫화할 수 있다.
- link : [flatMap](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Array/flatMap)
- Array.prototype.push(...Array)
    위 방법을 사용하면 Array의 아이템들이 플랫하게 전부 푸쉬됨

## Set
- link : [Set to Array](https://hianna.tistory.com/421)

## Web api
- link : [event.preventDefault()](https://week-book.tistory.com/entry/%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-preventDefault-%EC%A0%95%EB%A6%AC)
- link : [Window.localStorage](https://developer.mozilla.org/ko/docs/Web/API/Window/localStorage)
- link : [location](https://developer.mozilla.org/en-US/docs/Web/API/Location)

## 클로저
- link : [클로저](https://developer.mozilla.org/ko/docs/Web/JavaScript/Closures)

## setTimeout
- link : [setTimeout을 Promise로 감싼다면?](https://footprint-of-nawin.tistory.com/97)

## spread 문법
- const { type: a, ...b } = someObject;
    - someObject내 있었던 type이라는 필드는 a가 aliasing함
    - b는 type을 제외한 someObject의 모든 필드를 b라는 오브젝트에 담게 됨

## TO DO
- weakMap이 뭔데?