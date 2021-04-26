# CSS

## CSS (cascading Style Sheet)
* HTML의 겉을 꾸며준다.
![image](https://user-images.githubusercontent.com/41819129/116109398-af195680-a6ef-11eb-948d-ca3451a53042.png)
* 개발자가 작성한 스타일 -> 유저 정의 스타일 -> 브라우저 기본 스타일 순서대로 적용된다.

``` css
* {
  color: Green;
}

li {
  color: blue;
}

#special {
  color: pink;
}

.red {
  width: 100px;
  height: 100px;
  background: yellow;
}

button:hover {
  color: red;
  background: beige;
}

a[href]{
  color: purple;
}
```
* 스타일을 적용할 태그,id,class를 선택자를 이용해서 구분한다.
* property: value 형식이 기본
* 적용시킬 스타일 요소는 MDN을 이용해서 찾고 적용시키자!
