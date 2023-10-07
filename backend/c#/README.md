# C#
- link : [비동기 프로그래밍](https://learn.microsoft.com/ko-kr/dotnet/csharp/asynchronous-programming/async-scenarios)
- link : [lock 블럭](https://www.csharpstudy.com/Threads/lock.aspx)

## GC 가 커버하지 못하는 경우
- 이런 객체들이 존재함 (대표적으로 C#에서 '암호화Object')
- 이런 객체들은 보통 하드웨어 가속을 씀(CPU)
- 반드시 Dispose 를 해줘야함
- using 으로 생명주기를 보장해주는 것이 좋은 방법