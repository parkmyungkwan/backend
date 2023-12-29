## Domain Model

특정 도메인을 다양한 표현 방식(객체 모델링, 상태 다이어그램 등)을 이용해 개념적으로 표현한 것을 말한다.   
행위(behavior)를 중요시 하기 때문에 Unit Testing 하기에 적합하다.

## Repository

Repository는 객체의 상태를 관리하는 저장소로 영구 저장소를 의미하는 것이 아니고 객체의 상태를 관리하는 저장소이다.

## VO(Value Object)

값 오브젝트로써 값을 위해 쓰이며, read-Only 특징(사용하는 도중에 변경 불가능하며 오직 읽기만 가능)을 가진다.   
DTO와 유사하지만 DTO는 setter를 가지고 있어 값이 변할 수 있다.
