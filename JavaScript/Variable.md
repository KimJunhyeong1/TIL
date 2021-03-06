# 4장 변수 (모던 자바스크립트 Deep Dive)

## 4.1 변수란 무엇인가? 왜 필요한가?

- 자바스크립트는 개발자의 직접적인 메모리 제어를 허용하지 않는다.
- 변수는 하나의 값을 저장하기 위해 확보한 메모리 공간 자체 또는 그 메모리 공간을 식별하기 위해 붙힌 이름을 말한다.
- 변수 이름은 첫아이 이름을 짓듯이 심사숙고해서 지어야 한다.

## 4.2 식별자

- 식별자는 어떤 값을 구별해서 식별할 수 있는 고유한 이름을 말한다.
- 식별자 = 변수
- 변수, 함수, 클래스 등의 이름과 같은 식별자는 네이밍 규칙을 준수해야 하며, 선언에 의해 자바스크립트 엔진에 식별자의 존재를 알린다.

## 4.4 변수 선언의 실행 시점과 변수 호이스팅

- 변수 선언이 소스코드가 한 줄씩 순차적으로 실행되는 시점, 즉 런타임이 아니라 그 이전 단계에서 먼저 실행된다.
- 변수 선언문이 코드의 선두로 끌어 올려진 것처럼 동작하는 자바스크립트 고유의 특징을 변수 호이스팅이라고 한다.
- 모든 선언문은 런타임 이전 단계에서 먼저 실행되기 때문이다.

## 4.5 값의 할당

- 변수 선언은 소스코드가 순차적으로 실행되는 시점인 런타임 이전에 먼저 실행되지만 값의 할당은 소스코드가 순차적으로 실행되는 런타임 시점에 실행된다.
- 할당할 때 이전 메모리 공간에 새로운 값을 할당하는게 아니라, 새로운 메모리 공간을 확보하고 그곳에 할당 값 80을 저장한다

## 4.6 값의 재할당

- 재할당을 하다보면 이전에 사용했던 메모리 공간에 값들이 남아있을 것이다.
- 이러한 불필요한 값들은 가비지 컬렉터에 의해 메모리에서 자동 해제된다.
- 자바스크립트는 매니지드 언어로써 똑똑한 사람들이 개발한 가비지 콜렉터를 통해 메모리 누수를 방지한다.
