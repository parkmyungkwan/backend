## Spring AOP(Aspect Oriented Programming)

AOP는 Aspect Oriented Programming의 약자로 관점 지향 프로그래밍이라고 부르며,  
관점 지향은 쉽게 말해 어떤 로직을 기준으로 핵심적인 관점, 부가적인 관점으로 나누어서 보고 그 관점을 기준으로 각각 모듈화하겠다는 것이다.  
여기서 모듈화란 어떤 공통된 로직이나 기능을 하나의 단위로 묶는 것을 말한다.

## DI(Dependency Injection)
DI는 외부에서 객체 간의 관계(의존성)를 결정해 주는데 즉, 객체를 직접 생성하는 것이 아니라 외부에서 생성 후 주입시켜 주는 방식이라 할 수 있다.  
DI를 통해 객체 간의 관계를 동적으로 주입하여 유연성을 확보하고 결합도를 낮출 수 있다.  
Spring에서 의존 관계 주입(DI) 방법에는 총 3가지가 있다.

### 생성자주입(Construct Injection)

- 현재 가장 권장되는 의존 관계 주입 방식이다.

    - Spring 공식 문서에서도 생성자 주입을 권장한다.
    - 하나의 생성자가 존재할 때 필드 주입의 대부분의 단점을 극복한다.
    - Spring 4.3부터는 @Autowired가 생략 가능해서 최근에는 생성자를 딱 1개 두고, @Autowired를 생략하는 방법을 주로 사용한다.
    - Lombok 라이브러리의 @RequiredArgsConstructor를 함께 사용하면 생성자를 생략 가능해서 코드가 깔끔해진다.

- 오직 생성자 주입만이 final 키워드를 사용할 수 있고, 생성자를 통해 주입되는 방식이다.

    - final 키워드를 사용하기에 생성자로 인해 인스턴스가 생성될 때 1번만 할당된다.

- final 키워드를 사용해서 값이 한번 할당되면 변경할 수 없기에 객체의 불변성(Immutability)가 보장된다.

    - 불변성에 관해서는 맨 아래에서 추가로 정리하였음.

- 초기에 할당되기에 NPE(Null Pointer Exception)이 절대 발생하지 않는다.

### 필드 주입(Field Injection)

- Bean으로 등록된 객체를 사용하고자 하는 클래스에 Field로 선언한 뒤 @Autowired를 붙여주면 자동으로 의존 관계가 주입된다.
- Spring에서 @Autowired 어노테이션을 사용해서 객체 내 필드에 선언해서 주입하는 방법
- 간편하게 의존 관계 주입이 가능하지만 참조 관계를 눈으로 확인하기 어렵고, 순환 참조를 막을 수 없습니다.

    - 예를 들어 A가 B를 가지고 있고, B가 A를 가지고 있어(순환 참조) 실행 전까지 Error를 잡을 수 없다.


- 생성자 주입을 뺀 나머지(필드 주입, Setter 주입)은 모두 생성자 이후에 호출되므로, 필드에 final 키워드를 사용할 수 없다.

### Setter 주입(Setter injection)

- Spring에서 @Autowired 어노테이션을 사용해서 Setter 메서드를 통해 주입하는 방법

    - @Autowired는 Field, Setter Method, Constructor에 사용 가능하다.

- Spring 3.x 버전까지는 DI 권장 방식이였지만, 현재는 아니다.
- NPE(Null Pointer Exception) 발생할 수 있다.
- 생성자 주입을 뺀 나머지(필드 주입, Setter 주입)은 모두 생성자 이후에 호출되므로, 필드에 final 키워드를 사용할 수 없다.

## 싱글턴 패턴

소프트웨어 디자인 패턴에서 싱글턴 패턴을 따르는 클래스는, 생성자가 여러 차례 호출되더라도 실제로 생성되는 객체는 하나이고 최초 생성 이후에 호출된 생성자는 최초의 생성자가 생성한 객체를 리턴한다.

## IoC(Inversion of Control)

- IoC 란 Inversion Of Control의 약자이며, 제어의 역전 이라고 한다.
    - 일반적인 경우라면 '개발자'가 미리 정한 순서에 따라 생성, 실행을 주도, 의도 했다면(개발자가 제어권을 가졌다.)
    - IoC 가 등장한 이후는 객체의 생성, 생명주기, 관리까지 모든 객체에 대한 주도권을 프레임워크가 가진것이다.(프레임워크가 관리)
- IoC 를 통해 Application을 구성하는 객체 간의 낮은 결합도를 유지할 수 있다. 
- IoC 의 역할을 담당하는것이 Spring Container 이다. (Spring Container가 IoC를 담당한다.)

## Spring Bean

Spring IoC 컨테이너가 관리하는 자바 객체

## BeanFactory

- 빈을 생성하고 의존관계를 설정하는 기능을 담당하는 가장 기본적인 IoC 컨테이너이자 클래스를 말한다. 스프링 빈 컨테이너에 접근하기 위한 최상위 인터페이스이다.
- 스프링 빈을 관리하고 조회하는 역할을 담당한다.
- getBean()을 제공한다.
- Lazy-loading 방식을 사용한다
    - 빈을 사용할 때 빈을 로딩한다. ( 필요할 때만 로딩하기 때문에, 가벼운 경량 컨테이너이다. )
