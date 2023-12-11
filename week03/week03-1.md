## DTO(Data Transfer Object)

계층 간 데이터 전송을 위해 도메인 모델 대신 사용되는 객체이다.   
DTO는 순수하게 데이터를 저장하고, 데이터에 대한 getter, setter만을 가져야한다.

## JavaBeans

Java로 작성된 소프트웨어 컴포넌트이다.   
JavaBeans 클래스로서 작동하기 위해선 아래와 같은 관례를 따라야 한다.

- 클래스는 직렬화되어야 한다.(클래스의 상태를 지속적으로 저장 혹은 복원시키기 위해)
- 클래스는 기본 생성자를 가지고 있어야 한다.
- 클래스의 속성들은 get, set 혹은 표준 명명법을 따르는 메서드들을 사용해 접근할 수 있어야 한다.
- 클래스는 필요한 이벤트 처리 메서드들을 포함하고 있어야 한다.

## EJB(Enterprise JavaBeans)

EJB는 자바 기반의 엔터프라이즈 애플리케이션 개발을 위한 서버 측 컴포넌트 모델이다.   
EJB 사양은 Java EE의 자바 API 중 하나로, 주로 웹 시스템에서 JSP는 화면 로직을 처리하고, EJB는 업무 로직을 처리하는 역할을 한다.

## Java record

불변(immutable) 객체를 쉽게 생성할 수 있도록 하는 유형의 클래스(Java 14부터 지원)   
record 특징
- 멤버변수는 private final로 선언된다.
- getter, equals, hashcode, toString과 같은 기본 메소드를 제공한다
- 모든 멤버변수를 인수로 가지는 생성자를 자동 생성한다.
