# Execution Context

## Execution Context
- ECMAScript 스펙에 따르면 실행 컨텍스트를 실행 가능한 코드를 형상화하고 구분하는 추상적인 개념이라고 정의한다.
- 자바스크립트에서 **함수를 실행**시키면 콜 스택이라는 통에 함수에 대한 정보를 가지고 있는 실행 컨텍스트를 저장한다.
  
  
## Global Execution Context
![image](https://user-images.githubusercontent.com/41819129/154962401-9bf16633-6600-47a3-8d12-a6f0aa549364.png)
- 자바스크립트 코드를 실행시키면 자바스크립트 엔진은 콜 스택이라는 통에 전역 실행 컨텍스트를 담는다.
- 위 사진에서 보는 것과 같이 전역 실행 컨텍스트 위에 개별 함수 실행 컨텍스트가 쌓이고 실행되고 없어지고를 반복한다.
- 전역 실행 컨텍스트는 애플리케이션이 종료될 때(웹 페이지에서 나가거나 브라우저를 닫을 때)까지 유지된다.
  
  
## 실행 컨텍스트가 가지는 정보
![image](https://user-images.githubusercontent.com/41819129/154963030-f663d734-7d07-4802-9c79-937df5a80c23.png)
- 변수 정보 (변수, 함수 선언, 매개 변수 등)
- 스코프 정보 (스코프 체인: 자기 자신의 스코프와 상위 스코프들 (전역 스코프 까지) 정보)
- this 정보 (실행될 때 결정)
