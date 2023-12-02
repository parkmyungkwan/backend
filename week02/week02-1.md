## API(Application Programming Interface)

API는 응용 프로그램에서 사용할 수 있도록, 운영 체제나 프로그래밍 언어가 제공하는 기능을 제어할 수 있게 만든 인터페이스를 뜻한다.

## 정보은닉과 캡슐화

### 정보은닉

객체지향 언어적 요소를 활용하여 객체에 대한 구체적인 정보를 노출시키지 않도록 하는 기법이다.   
Java에서 대표적인 은닉 기법 3가지   
1. 객체의 구체적인 타입 은닉(업캐스팅)
2. 객체의 필드 및 메소드 은닉(캡슐화)
3. 구현은닉(인터페이스 & 추상클래스)

### 캡슐화

**캡슐화**란 쉽게 말하면 변수나 메소드들을 캡슐로 감싸서 안보이게 하는 정보 은닉 개념중 하나이다.   
캡슐화는 객체의 속성(Field)과 행위(Method)를 하나로 묶고, 외부로 부터 내부를 감싸 숨겨 은닉한다.   
또한 외부의 잘못된 접근으로 값이 변하는 의도치 않는 동작을 방지하는 보호 효과도 누를 수 있다.   
Java에서는 대표적으로 protected, default, private의 접근제어자를 통해 구현이 가능하다.   
**캡슐화는 정보은닉의 기법중 하나이다.**

## Architecture와 Architecture Style의 차이

Architecture 설계 시 어떠한 공통적인 방법을 사용할 경우 Architecture Style이라고 부른다.   

## REST

### 필딩제약조건

1. Starting with the Null Style

2. Client-Server
- API를 통해 정보를 교환하는 주체는 클라이언트와 서버 구조를 가져 분리함으로써, 서로 의존하지 않는 구조를 가져야한다.
3. Stateless
- 무상태성
- 클라이언트에서 서버로 요청 시 요청에 대한 모든 정보가 포함되어야 한다.
4. Cacheable
- 캐시 가능 여부, 캐시 사용이 가능하면 클라이언트는 응답 데이터를 재사용 할수 있어야 한다.

5. Uniform Interface
- identification of resources
- manipulation of resources through representation
- self-descriptive messages
- hypermedia as the engine of application state

6. Layered System
- 서버는 중개 서버(게이트웨이, 프록시)나 로드 밸런싱, 공유 캐시 등의 기능을 사용하여 확장성 있는 시스템을 구성할 수 있다.

7. Code-On-Demand
- 서버는 클라이언트로 실행 가능한 프로그램을 전달할 수 있어야 한다.