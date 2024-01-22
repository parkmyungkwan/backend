## 관심사의 분리(SoC)

관심사의 분리란 각 부문이 각자의 관심사를 갖도록 컴퓨터 프로그램을 여러 부문으로 나누는 설계 원칙을 말한다.

## 응집도

응집도란 한 모듈 내의 구성요소들 간의 연관 정도를 의미한다.   
응집도의 강도 단계는 기능적, 순차적, 절차적, 시간적, 논리적, 우연적 척도로 분리되며, 이 따 모듈의 품질을 측정할 수 있다. 기능적 응집도 쪽으로 갈 수록 좋은 품질이고 우연적 응집도로 갈수록 나쁜 품질이 된다.   

#### 기능적 응집도

- 모듈 내부의 모든 기능이 단일 목적을 위해 수행되는 경우

#### 순차적 응집도

- 모듈 내에서 한 활동으로부터 나온 출력 값을 다른 활동이 사용할 경우

#### 교환적 응집도

- 동일한 입력과 출력을 사용해 다른 기능을 수행하는 활동들이 모여있을 경우

#### 절차적 응집도

- 모듈이 다수 관련 기능을 가질 때 모듈 안의 구성요소들이 그 기능을 순차적으로 수행할 경우

#### 시간적 응집도

- 연관된 기능이라기 보단 특정 시간에 처리되어야 하는 활동들을 한 모듈에서 처리할 경우

#### 논리적 응집도

- 유사한 성격을 갖거나 특정 형태로 분류되는 처리 요소들이 한 모듈에서 처리되는 경우

#### 우연적 응집도

- 모듈 내부의 각 구성요소들이 연관이 없을 경우

## 결합도

결합도는 모듈(클래스 파일)간의 상호 의존 정도 또는 연관된 관계의 끈끈함 정도를 의미한다.   
좋은 소프트웨어는 낮은 결합도(low coupling)를 가지고 있다.   
결합도는 자료, 스탬프, 제어, 외부, 공통, 내용 결합도의 척도로 나타낸다.   

#### 자료 결합도

- 모듈간의 인터페이스로 전달되는 파라미터(데이터)를 통해서만 상호 작용이 일어나는 경우

#### 스탬프 결합도

- 모듈간의 인터페이스로 배열이나 객체, 자료 구조 등이 전달되는 경우

#### 제어 결합도

- 어떤 모듈이 다른 모듈 내부의 논리적인 흐름을 제어하는 제어 요소를 전달하는 경우

#### 외부 결합도

- 어떤 모듈이 외부에 있는 다른 모듈의 데이터를 참조하는 경우 (데이터, 통신 프로토콜 등)

#### 공통 결합도

- 여러 개의 모듈이 하나의 공통 데이터 영역(전역 변수 참조 및 갱신)을 사용하는 경우

#### 내용 결합도

- 어떤 모듈 내부에 있는 변수나 기능을 다른 모듈에서 사용하는 경우

## Layered Architecture

Layered Architecture는 소프트웨어 개발에서 가장 일반적으로 널리 사용되는 아키텍처이다. 구성되는 계층의 숫자에 따라 N 계층 아키텍처 (N-tier Architecture) 라고도 한다.

각 계층은 어플리케이션 내에서의 특정 역할과 관심사(화면 표시, 비즈니스 로직 수행, DB 작업 등)별로 구분된다. 이는 Layered Architecture 의 강력한 기능인 '관심사의 분리 (Separation of Concern)' 를 의미한다. 특정 계층의 구성요소는 해당 계층에 관련된 기능만 수행한다. 이런 특징은 높은 유지보수성과 쉬운 테스트라는 장점이 존재한다.

## UUID

UUID는 Universally Unique IDentifier의 약자로, 전세계에 하나밖에 없는 ID라는 뜻이다.