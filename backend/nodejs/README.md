# NODEJS
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