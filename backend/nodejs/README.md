# NODEJS
<!-- 2023.10.14 -->
- link : [static files in nodejs](https://m.blog.naver.com/PostView.naver?isHttpsRedirect=true&blogId=pjok1122&logNo=221545195520)
- link : [npm 과 yarn](https://cloud-allstudy.tistory.com/958)
- link : [package-lock.json 이 필요한 이유](https://jihyundev.tistory.com/21)
- link : [commonjs 와 es module 의 공존(good practice)](https://toss.tech/article/commonjs-esm-exports-field)
- link : [ECMAScript 쉬운 설명](https://wormwlrm.github.io/2018/10/03/What-is-the-difference-between-javascript-and-ecmascript.html)
- link : [ECMAScript 란?](https://sumini.dev/til/006-ecmascript/)
- link : [error class](https://nodejs.org/api/errors.html)
- link : [assert module](https://www.geeksforgeeks.org/node-js-assert-iferror-function/?ref=lbp)
    - ifError(value) 메소드는 error object 를 리턴하고 value 값을 메시지에 포함한다. value 에 undefined, null 을 넣을 경우 error 를 리턴하지 않는다.
- link : [exports 와 module.exports 의 차이](https://dydals5678.tistory.com/97)
- link : [vm module2(참고용. 많이 어려움)](https://core-research-team.github.io/2023-03-29/Nodejs-VM-Sandbox-Breakout)
- link : [vm module](https://homzzang.com/b/njs-62)
<!-- 2023.10.13 -->
- link : [async_hooks module](https://runebook.dev/ko/docs/node/async_hooks)
- link : [node-gyp 사용 예제](https://m.blog.naver.com/pjt3591oo/220781916699)
    - node-gyp란 노드로 작성된 크로스 플랫폼 CLI. 이것을 통해 노드에서 네이티브 애드온 모듈들을 사용할 수 있다.
- link : [semantic versioning](https://jake-seo-dev.tistory.com/283)
- The crypto module provides cryptographic functionality that includes a set of wrappers for OpenSSL's hash, HMAC, cipher, decipher, sign, and verify functions.
- link : [cluster module 을 통해 멀티코어 사용하기](https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-cluster-%EB%AA%A8%EB%93%88-%EC%BD%94%EC%96%B4%EB%A5%BC-%EC%B6%94%EA%B0%80%EB%A1%9C-%EC%82%AC%EC%9A%A9)
    - cluster module 은 기본적으로 os 모듈과 세트라고 볼 수 있다. os 모듈을 통해 코어 갯수를 확인한 후 cluster worker 를 설정한다.
- link : [import, export](https://inpa.tistory.com/entry/JS-%F0%9F%93%9A-%EB%AA%A8%EB%93%88-%EC%82%AC%EC%9A%A9%ED%95%98%EA%B8%B0-import-export-%EC%A0%95%EB%A6%AC)
- .node extention file
    - a C++ Addon file that is built with node-gyp
<!-- 2023.10.12 -->
- link : [module wraper function](https://velog.io/@vekkary/exports%EC%99%80-module.exports)
- link : [http module 에 대한 설명](https://sjh836.tistory.com/84)
    - 익히 알고 있는 req 는 IncomingMessage 이고, res 는 serverResponse 이다.
- link : [process module](https://nodejs.org/api/process.html)
    - process 모듈은 EventEmitter 를 상속받고 있다.
- NodeJS LTS 버젼은 어떻게 선정되는가?
    - LTS release status is “long-term support”, which typically guarantees that critical bugs will be fixed for a total of 30 months. Production applications should only use Active LTS or Maintenance LTS releases.
- link : [path module](https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-Path-%EB%AA%A8%EB%93%88-%F0%9F%A7%B7-%EA%B2%BD%EB%A1%9C-%EC%A0%9C%EC%96%B4)
- link : [__dirname / __filename / process.cwd() 차이 정리](https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-dirname-filename-processcwd-%EC%B0%A8%EC%9D%B4-%EC%A0%95%EB%A6%AC)
- link : [event module](https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-require-%EB%AA%A8%EB%93%88)
- link : [child_process](https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-childprocess-%EB%AA%A8%EB%93%88)
- link : [Worker_Threads 모듈 (멀티 쓰레드 구현)](https://inpa.tistory.com/entry/NODE-%F0%9F%93%9A-workerthreads-%EB%AA%A8%EB%93%88?category=890802)
- link : [module:repl](https://runebook.dev/ko/docs/node/repl)
<!-- 2023.10.11 -->
- link : [nojavascript 엔진과 브라우저, nodejs의 동작 이해](https://inpa.tistory.com/entry/%F0%9F%94%84-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9D%B4%EB%B2%A4%ED%8A%B8-%EB%A3%A8%ED%94%84-%EA%B5%AC%EC%A1%B0-%EB%8F%99%EC%9E%91-%EC%9B%90%EB%A6%AC)
- link : [동기, 비동기 그리고 블로킹, 논블로킹 완벽 이해](https://inpa.tistory.com/entry/%F0%9F%91%A9%E2%80%8D%F0%9F%92%BB-%EB%8F%99%EA%B8%B0%EB%B9%84%EB%8F%99%EA%B8%B0-%EB%B8%94%EB%A1%9C%ED%82%B9%EB%85%BC%EB%B8%94%EB%A1%9C%ED%82%B9-%EA%B0%9C%EB%85%90-%EC%A0%95%EB%A6%AC)
<!-- 2023.10.10 -->
- link : [util.promisify 라는 것이 있다?](https://helloinyong.tistory.com/94)
- link : [nodejs process 터미널 출력에 대한 흥미로운 options](https://runebook.dev/ko/docs/node/process)
    - `--no-warnings` : 명령줄 옵션을 사용하여 기본 콘솔 출력을 억제할 수 있습니다.
    - `--trace-warnings` : 명령줄 옵션을 사용하면 경고에 대한 기본 콘솔 출력에 경고의 전체 스택 추적이 포함되도록 할 수 있습니다.
    - `--throw-deprecation` : 명령줄 플래그를 사용하여 Node.js를 시작하면 사용자 정의 사용 중단 경고가 예외로 발생합니다.
    - `--trace-deprecation` : 명령줄 플래그를 사용하면 사용자 정의 지원 중단이 스택 추적과 함께 stderr 에 인쇄됩니다.
    - `--no-deprecation` : 명령줄 플래그를 사용하면 사용자 정의 지원 중단에 대한 모든 보고가 억제됩니다.
    - *-deprecation 명령줄 플래그는 'DeprecationWarning' 이름을 사용하는 경고에만 영향을 미칩니다.
- link : [require 에 대한 이해](https://jongmin92.github.io/2017/07/13/Node/require/)
- link : [Console module](https://nodejs.org/api/console.html)
    - `console.time()`, `console.timeEnd()`, `console.timeLog()` 를 이용하면 쉽게 걸린시간 체크를 할 수 있다. 
- link : [built-in module "os"](https://coderrocketfuel.com/article/get-the-number-of-system-cpu-cores-using-node-js)
<!-- 2023.10.09 -->
- link : [nodejs chrome debuging 연결방법](https://blog.outsider.ne.kr/1307)
- link : [Node-API more detail](https://runebook.dev/ko/docs/node/n-api)
- link : [Node-API(N-API)](https://m.blog.naver.com/remocon33/221580633458)
- link : [util.types](https://nodejs.org/api/util.html#utiltypes)
    - javascript 에 built-in 되어 있는 object 들의 타입을 검증할 때 사용할 수 있음(ex. util.types.isDate())
- link : [DNS module 한글 간략 설명](https://homzzang.com/b/njs-42)
- link : [DNS module](https://nodejs.org/api/dns.html)
    - dns.lookup() does not necessarily have anything to do with the DNS protocol. The implementation uses an operating system facility that can associate names with addresses and vice versa. This implementation can have subtle but important consequences on the behavior of any Node.js program.
- link : [스트림 부연설명](https://velog.io/@moongq/Stream-Nodejs)
- link : [Nodejs 스트림의 모든 것](https://fedevelopers.github.io/tech.description/node-js-stream-everything-you-have-to-know/)
- link : [Buffer syntax](https://yceffort.kr/2021/10/understanding-of-nodejs-buffer)
- link : [Buffer 에 대한 개념 자체](https://tk-one.github.io/2018/08/28/nodejs-buffer/)
- link : [Core modules list](https://flaviocopes.com/node-core-modules/)
    - 포함: crypto, events, dgram(udp 관련), http2 등...
    - 미포함: webpack, request, chalk, ftp(파일 전송 프로토콜)
<!-- 2023.10.07 -->
- link : [node-cron 을 이용한 NODEJS 스케줄러 설정](https://miiingo.tistory.com/180)
- link : [Nodejs 란? 특징, 장점, Single Thread](https://m.blog.naver.com/hhw1990/221394005779)