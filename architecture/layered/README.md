## 레이어드 아키텍쳐
- `service`와 `entity`의 경계는 어떻게 구분하는게 효과적인가?
    - 김영한님의 좋은 답글을 기록해둔다.
    ```
    도메인이 비즈니스 로직의 주도권을 가지고 개발하는 것을 도메인 주도 설계라 합니다. 이렇게 해두면 서비스의 많은 로직이 엔티티로 이동하고, 서비스는 엔티티를 호출하는 정도의 얇은 비즈니스 로직을 가지게 됩니다.

    이렇게 하면 information expert pattern을 지키면서 개발할 수 있습니다.

    (information expert pattern는 검색해보시면 도움이 되실거에요^^)

    반대로 엔티티는 단순히 getter, setter만 제공하고, 서비스에 비즈니스 로직이 모두 있어도 됩니다.

    이렇게 되면 서비스 로직이 커지고, 엔티티는 단순히 데이터를 전달하는 역할만 담당하게 됩니다.

    전자는 엔티티를 객체로 사용하는 것이고, 후자는 엔티티를 자료 구조로 사용하는 방식이지요.

    그러면 항상 전자가 정답인가? 라고 하면 그렇지는 않습니다. 둘다 장단점이 있기 때문에, 상황에 맞는 적절한 방법을 선택하는 것이 중요합니다.

    관련해서 클린코드 6. 객체와 자료구조에 둘의 차이가 자세히 설명되어 있으니 한번 읽어보시길 추천드립니다.

    감사합니다.
    ```

- [기초 아티클](https://hudi.blog/layered-architecture/)
- `4-tier layer`를 많이 사용하는 편이다.
    - `presentation`: view, controller
    - `business`: service, domain model
    - `persistence`: repository, dao
    - `database`: database