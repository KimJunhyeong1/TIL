### reduce

- Array의 prototype으로 메서드가 정의되어 있다.
- callback 함수를 전달하고 각 요소들에 대해 실행된다.
- callback함수는 네 가지 인수를 받는다
    - accumulator : 초기값을 가지는 축적되는 값
    - currentValue: 현재 요소의 값
    - currentIndex: 현재 요소의 인덱스
    - array: reduce를 호출한 배열

```jsx
var sum = [0, 1, 2, 3].reduce(function (accumulator, currentValue) {
  return accumulator + currentValue;
}, 0);
// sum is 6
```
