# CRYPTO
- link : [Hex To Byte, Byte To Hex](https://m.blog.naver.com/PostView.naver?blogId=phm0515&logNo=20167769706&proxyReferer=https:%2F%2Fwww.google.com%2F)
- link : [base64 인코딩이란?](https://effectivesquid.tistory.com/entry/Base64-%EC%9D%B8%EC%BD%94%EB%94%A9%EC%9D%B4%EB%9E%80)

## jwt
- link : [jwt refreshToken 관리](https://velog.io/@from_numpy/NestJS-How-to-implement-Refresh-Token-with-JWT#-refresh-token%EC%9D%80-%EC%99%9C-%EB%93%B1%EC%9E%A5%ED%95%98%EC%98%80%EB%8A%94%EA%B0%80)
    - link : [jwt refreshToken 관리 2(비슷한 내용)](https://soonyubi.github.io/jwt-refresh-token/)

## Base64 vs safe url Base64
- 끝부분 `=` 는 없애고, `+` => `-` & `/` => `_`
    - url 로 들어갔을 때 치명적일 수 있는 문자들이기 때문.
- 다시 바꿀 땐 역으로. 단, `=` 의 경우 전체 문자의 길이를 4로 나눴을 때 나머지가 나오면 `4-나머지` 만큼 `=` 를 끝에 더한다.
    
## Encrypt
- RSA 암호화
    - 공개키, 개인키 암호화 시스템
- ecdh(≒secp256r1 ≒nistP256)
    - 서로 다른 둘이 각각 key pair(공개, 비밀) 을 만들어서 공개키를 교환한 후 각자의 비밀키와 공개키로 secret key 를 만들었을 때 그 값이 같아야함.
- ECB, CBC