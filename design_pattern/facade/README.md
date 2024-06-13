# FACADE PATTERN

- facade는 정면, 대문을 나타낸다. 그 정면 뒤에는 뭐가 있는지 알 수 없다는 컨셉이 이 디자인 패턴의 핵심이다. 복잡한 동작들을 한 데 묶어 클라이언트입장에서는 간단한 명령하나로 그 동작들을 한꺼번에 수행할 수 있게 된다. 예를 들어, NestFactory의 initialize() 메서드 같은 것들이 있겠다.

- link : [Are the roles of a service and a façade similar?](https://stackoverflow.com/questions/15038324/are-the-roles-of-a-service-and-a-fa%c3%a7ade-similar)
  - At the end of the day it's all code - design patterns are simply ways of talking about how you organize your code, and are named after their purpose. This helps greatly when talking to others who are also 'in' on the idea. It's jargon. A facade is a collection of helper methods whose purpose is to hide a library or group of libraries from the application (a facade to a building hides the ugly bits behind it). So at one level you are right, but if you do access the rest, that would subvert the purpose of the name, and so confuse other developers, so the jargon no longer helps.
  - 디자인패턴의 사용이유는 너의 코드가 어떠한 목적으로 작성되었는지를 효과적으로 나타내기 위함에 있다. 가장 우선적으로 너의 코드가 어떤 목적성을 가지고 있는지 확실히 해라.
- link : [Difference between the facade pattern and service layer pattern](https://stackoverflow.com/questions/74574576/difference-between-the-facade-pattern-and-service-layer-pattern)
  - `service`는 아키텍쳐 패턴이고, `facade`는 우선 구조적 디자인 패턴이다. 어떤식으로 service코드를 작성하게 될지 모르겠지만(service layer를 표현하는 클래스가 어떠한 모습일지는 모르겠지만) 모든 service가 facade인 것은 아니고 경우에 따라 facade가 될 수도 있지 않을끼?
