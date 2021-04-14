# Cookie

## Overview
- Response 헤더에 쿠키 값을 설정하면 새로고침 하더라도 Request 헤더에 쿠키 값이 남는다.
```javascript
var http = require("http");

http
  .createServer(function (request, response) {
    response.writeHead(200, {
      "Set-Cookie": ["yummy_cookie=choco", "tasty_cookie=strawberry"],
    });

    response.end("Cookie!!");
  })
  .listen(3000);

```

- 쿠키를 사용해서 클라이언트의 설정, 정보(로그인 정보)를 저장해서 웹페이지를 개인화 할 수 있다.

## Permanent cookies
- 쿠키를 설정할 떄 'Max-age' 값을 설정하여 쿠키 만료일자를 지정할 수 있다.

## Session cookies
- 웹 브라우저를 끄면 (세션이 종료되면) 사라지는 휘발성 쿠키

## Secure과 HttpOnly 쿠키
- 'Secure' 옵션은 https로만 통신하는 경우만 해당 쿠키를 서버로 전송하는 것이다.
- 'HttpOnly'는 자바스크립트로 쿠키에 접근하는 것을 막는 욥선

## Path 설정
- 'Path' 옵션에서 디렉토리를 지정하면 해당, 그리고 그 하위 디렉토리에서만 쿠기가 살아있음
