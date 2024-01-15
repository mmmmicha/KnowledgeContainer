# GIT
- link : [이상적인 commit 단위는 무엇일까](https://youtu.be/f7RMOeApPh8?t=229)
- link : [fork 해온 repository 잔디 심는 방법 : repository 복사해오기 duplicate the repository](https://soranhan.tistory.com/11)
- link : [조직을 벗어나더라도 잔디를 유지하는 방법](https://github.com/isaacs/github/issues/1138)
    - 반드시 리포지토리에 starring을 해둘 것!
- link : [잔디심기 누락 현상 해결](https://kdjun97.github.io/git-github/plant-grass/)
- link : [깃허브 사용법(입문)](https://homeproject.tistory.com/9)
- link : [Git의 동작 원리](https://ndb796.tistory.com/187)

## Fetch
- link : [git pull vs fetch](https://www.freecodecamp.org/korean/news/git-fetch-vs-pull/)

## Merge
- link : [Merge vs Squash and Merge vs Rebase and Merge](https://im-developer.tistory.com/182)
- cli
    - ```git merge 대상브랜치```
        - 외국은 항상 자기중심이다. 현재 체크아웃한 브랜치에 병합할 대상브랜치로 생각하자

## Rebase
- link : [Rebase -i 사용하기(feat.SourceTree)](https://jojoldu.tistory.com/613)
- link : [Rebase 교과서](https://git-scm.com/book/ko/v2/Git-%EB%B8%8C%EB%9E%9C%EC%B9%98-Rebase-%ED%95%98%EA%B8%B0)

## Git Authentication
- link : [깃 토큰 이용한 권한사용](https://whoyoung90.tistory.com/25)

## Git 명령어
- 캐시 삭제
    git rm -r --cached .
    git add .
- push -f 로 없어진 commit 살리기
    - git reflog
    - 위 명령어를 통해 원하는 커밋을 checkout 받을 수 있음
    - 이 커밋과 현재 문제가 생긴 브랜치를 git diff로 비교하여 알맞은 커밋인지 확인함
    - 알맞은 커밋이면 git push -f 로 푸시를 함

## Github Blog
- link : [prose.io tutorial](https://pchengi2.github.io/using-prose.io-for-posting/)
- link : [markdown -> html online](https://markdowntohtml.com/)
- link : [깃 블로그 css 깨질 떄](https://iamheesoo.github.io/blog//gitblog-css-problem)
- link : [깃 블로그 쉽게 만들기 및 관리하기](https://velog.io/@pyk0844/%EA%B9%83-%EB%B8%94%EB%A1%9C%EA%B7%B8-%EB%A7%8C%EB%93%A4%EA%B8%B0%EC%89%BD%EA%B2%8C-%EA%B4%80%EB%A6%AC-%ED%95%98%EA%B8%B0)

## Github README
- link : [깃허브 뱃지로 이쁘게 꾸미기](https://cocoon1787.tistory.com/689)
    - link : [simple icons](https://simpleicons.org/?q=linked)

## Github Action
- link : [Github Actions 적용기](https://tech.kakaoenterprise.com/180)

## Github Environment
- link : [GitHub Actions 워크플로우의 승인 기능 사용하기](https://blog.outsider.ne.kr/1556)