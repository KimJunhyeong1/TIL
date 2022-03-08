# Asynchronous
![image](https://user-images.githubusercontent.com/41819129/157248489-2ca7dea2-b91b-4b1d-b8d9-c4c2afebcdd6.png)
## 자바스크립트 엔진
- 자바스크립트 엔진이 브라우저에 포함되어 있다.
- 엔진을 통해 우리의 자바스크립트 코드를 해석하고 실행해준다.
- 대표적인 엔진으로는 구굴에서 만든 크롬 V8 엔진이 있다.
- 위에 그림과 같이 자바스크립트는 런타임에서 하나의 CallStack만 들고있다, 이것은 싱글스레드를 의미한다.
  
  
## WebAPI
- 자바스크립트가 아닌 부라우저가 제공해주는 기능이다.
- DOM, AJAX, Timeout(setTimeout)에 관련된 메서드를 자바스크립트를 실행하면 WebAPI에서 해당 메서드를 처리한다.
- WebAPI에서 해당 동작이 처리가 완료되면 Callback Queue에 담는다.
  
  
## 자바스크립트에서의 비동기 처리
- 앞서 말했듯이 자바스크립트는 싱글스레드이다.
- 하지만 위에서 설명했던 WebAPI와 Callback Queue 그리고 Event Loop를 통해 비동기 처리가 가능하다.
- Event Loop의 역활은 콜 스택과 Callback Queue를 주시하는 것이다.
- 만약 우리의 코드가 콜 스택에 담겼다가 모두 실행된 후 최종 main 함수까지 실행되면 콜 스택이 비게된다.
- 이 때 Event Loop는 콜 스택이 비어있는 걸 확인하고 Callback Queue에 제일 먼저 들어온 Callback 함수를 콜 스택에 담는다.
- 콜 스택에 담겨진 Callback 함수를 꺼내 실행시킨다.
- 이렇게 WebAPI에 비동기 관련 코드를 위임함으로써 자바스크립트에서 비동기 작업이 가능하게 해준다.
