## REEST란?

REST(Representational State Transfer)의 약자이다. URI(Uniform Resource Identifier)를 통해 자원을 명시하고, HTTP method를 통해 자원에 대한 CRUD Operation을 적용하는 것을 의미한다.

## REST의 특징

- Server-Client (서버-클라이언트 구조)
    - 자원이 있는 쪽이 Server, 자원을 요청하는 쪽이 Client
    - 서로 간의 의존성이 줄어듦
- Stateless(무상태)
    - Client의 context를 Server에 저장하지 않는다. (세션, 쿠키 등의 정보를 저장하지 않아도 되기 때문에 구현이 단순해짐.)
    - Server는 각각의 요청을 별개의 것으로 인식하고 처리한다.
    - 이전 요청이 다음 요청의 처리에 연관되어서는 안된다. (Server의 처리 방식에 일관성을 부여하고 부담이 줄어들며, 서비스의 자유도가 높아진다.)
- Cacheable(캐시 처리 가능)
    - 웹 표준 HTTP 프로토콜을 그대로 활용하므로, 기존 캐싱 기능을 적용할 수 있다.
    - 캐시 사용을 통해 응답시간이 빨라지고, REST Server 트랜잭션이 발생하지 않기 때문에 전체 응답시간, 성능, 서버의 자원 이용률을 향상시킬 수 있다.
- Layered System(계층화)
    - Client는 REST API Server만 호출한다.
    - REST Server는 다중 계층으로 구성될 수 있다.
        - API Server는 순수 비즈니스 로직만 수행하고, 보안, 암호화, 사용자 인증 등을 추가하여 구조상의 유연성을 줄 수 있다.
        - 로드밸런싱, 공유 캐시 등을 통해 확장성과 보안성을 향상시킬 수 있다.
- Code-On-Demand(optional)
    - Server로부터 스크립트를 받아서 Client에서 실행.
    - 반드시 충족할 필요는 없다.
- Uniform Interface(인터페이스 일관성)
    - URI로 지정한 자원에 대한 조작을 통일되고 한정적인 인터페이스로 수행한다.
    - HTTP 표준 프로토콜을 따르는 모든 플랫폼에서 사용 가능하며, 특정 언어나 기술에 종속되지 않는다.

## RESTful이란?

REST API를 제공하는 웹 서비스를 RESTful하다고 할 수 있다.

## RESTful의 목적

이해하기 쉽고 사용하기 쉬운 REST API를 만드는 것.

성능이 매우 중요한 상황에서는 굳이 RESTful한 API를 구현할 필요는 없다.

- RESTful 하지 못한 경우 예시
    - CRUD 기능을 모두 POST로만 처리하는 API
    - route에 resource, id 외의 정보가 들어가는 경우 (/students/updateName)
