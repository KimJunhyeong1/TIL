## Virtual DOM에 대한 이해 및 [Diffing Algorithm](https://ko.reactjs.org/docs/reconciliation.html)에 대한 리서치

### 브라우저 렌더링 과정

- 렌더링 엔진이 HTML을 파싱하여 DOM노드로 이루어진 트리 생성
- CSS파일과 inline 스타일을 파싱하고 DOM + CSSOM을 이용해서 렌더 트리 생성
- 각 노드들의 스크린에서의 좌표에 따라 위치 결정해서 레이아웃 구성
- 실제 화면에 그리는 페인트 과정을 거친다.
- 여기서 변화가 발생하면 다시 렌더트리를 만들고 레이아웃을 구성하고 리페인트 하는 과정을 반복한다.

### Virtual DOM

- 자바스크립트에서 관리하는 실제 DOM의 복사본이다.
- 실제 DOM을 추상화환 Object이다.

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/2f2db4a6-aab3-474f-a03a-84ffa51df751/Untitled.png)

- 메모리 상에서 동작하고 변화를 묶어서 실제 DOM에 한번에 반영해서 연산 횟수를 줄일 수 있다.
- UI의 가상적인 표현을 메모리에 저장하고, 리액트DOM과 같은 라이브러리에 의해 실제 DOM과 동기화
- 동기화 하는 과정을 재조정이라고 부른다.
- 가상DOM은 가볍고 불변성을 유지하고 상태를 가지지 않는다.
- 가상 DOM은 이전 버전과 새롭게 렌더링 된 버전을 비교하는데 이 때 Diffing알고리즘을 사용한다.
- element의 속성 값만 변한 경우에는 속상 값만 업데이트
- element의 태그 또는 컴포넌트가 변경된 경우에는 해당 노드를 포함한 하위 모든 노드를 unmount 후 새로운 가상 DOM으로 대체
- 그러면, Virtual DOM 이 해결 하려고 하는건 무엇이냐? 그 DOM fragment를 관리하는 과정을 수동으로 하나하나 작업 할 필요 없이, 자동화하고 추상화하는거에요
