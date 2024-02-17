# JQUERY

## $(document).ready() 를 쓰는 이유

- jquery를 기본적으로 load 하기 위해서가 아니라 html을 전체적으로 로딩한 후에 javascript 코드를 적용하기 위해서이다.
- 브라우저는 `<script>` 를 만나게 되면 렌더링을 멈추고 이를 처리한다. 그렇기에 `<body>` 내 마지막에 js의 link 태그를 둠으로써 렌더링을 방해없이 마친 후 사용자에게 렌더링요소를 먼저 보여지게끔 하는 방식을 사용한다.
- 하지만, `ready`를 사용하게 되면 렌더링을 다 마치고 javascript 처리를 시작하기 때문에 `<body>` 마지막에 link를 놓을 필요가 없어진다.

## etc
- 알아두면 좋음
    ```
        $('<button/>', {
            class: 'btn btn-danger',
            text: `채팅방 입장`,
            click: () => handleAcceptSendbirdInvitation(data.Socialing.id, data.userId),
        })
    ```