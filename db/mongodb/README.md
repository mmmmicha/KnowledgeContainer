# MONGODB

## Mongoose
- new mongoose.Types.ObjectId.IsValid()
    - 내부 로직을 정확히 볼 필요가 있음. 단순히 글자수만 맞췄을 때 validation 을 통과하는 현상 발견함.
- __v field 는 왜 필요한가?
    ```
        __v 필드는 MongoDB에서 Mongoose와 같은 ODM(Object-Document Mapping) 라이브러리와 함께 사용될 때 자주 나타나는 필드입니다. 이 필드는 문서의 버전을 나타내며 다음과 같은 이유로 필요합니다s:

        Concurrency Control: 여러 사용자 또는 서비스가 동시에 동일한 문서를 업데이트하려고 할 때, __v 필드를 사용하여 각 업데이트가 해당 문서의 최신 버전인지 확인할 수 있습니다. 이를 통해 동시성 제어 및 데이터 충돌을 방지할 수 있습니다.

        버전 관리: __v 필드는 문서의 업데이트 이력을 추적하는 데 사용됩니다. 언제 문서가 마지막으로 변경되었는지 추적하거나 사용자가 문서를 변경하는 동안 발생한 수정 사항을 추적하는 데 도움이 됩니다.

        손실 방지: 동시성 문제로 인해 데이터가 손실되는 것을 방지합니다. 동시에 업데이트가 발생할 때, MongoDB는 __v 필드를 기반으로 최신 버전의 문서만 업데이트를 반영하고 다른 버전의 문서는 건너뛰게 됩니다.

        라이브러리 호환성: Mongoose와 같은 ODM 라이브러리는 __v 필드를 사용하여 업데이트 된 문서의 버전을 관리하고 동시성 제어를 제공합니다.

        따라서 __v 필드는 MongoDB와 Mongoose를 사용하는 환경에서 데이터 무결성과 동시성 관리를 지원하기 위해 사용됩니다. 이 필드를 사용하면 데이터베이스에서 안정적인 동작을 보장하고 데이터 일관성을 유지할 수 있습니다.
    ```

## Query option
- link : [$gte, $lte](https://mongoosejs.com/docs/tutorials/dates.html)
- link : [$in](https://kb.objectrocket.com/mongo-db/the-mongoose-in-operator-1015)
- link : [$ne](https://www.mongodb.com/docs/manual/reference/operator/query/ne/)

## MongoDB
- 'SoftDelete' 어떻게 사용하면 좋을까?
    - mongoose 엔 softDelete 개념이 없어 직접 구현을 해야함
    - boolean 으로 하거나 deletedAt 으로 대체할 수 있겠다.
- link : [mongoose 'update' 사용 시 업데이트 된 결과 리턴하는 옵션](https://stackoverflow.com/questions/24747189/update-and-return-document-in-mongodb)
- link : [강좌 4편 find() 메소드 활용 – sort(), limit(), skip()](https://velopert.com/516)
- link : [MongoDB 검색 기능 활용하기](https://sy34.net/mongodb-full-text-search/)
- link : [MongoDB를 쓰면서 알게 된 것들](http://bigmatch.i-um.net/2013/12/09/mongodb%EB%A5%BC-%EC%93%B0%EB%A9%B4%EC%84%9C-%EC%95%8C%EA%B2%8C-%EB%90%9C-%EA%B2%83%EB%93%A4/)
- 대표적인 `NoSQL`
- `JSON` 을 sql로 파싱하지않고 저장한다.