## Ajax

Asynchronous JavaScript And XML의 약자이다.
자바스크립트를 이용해 클라이언트와 서버 간에 데이터를 주고 받는 비동기 HTTP 통신이다.
XMLHttpRequest(XHR) 객체를 이용해 전체 페이지가 아닌 필요한 데이터만 불러올 수 있다.

### 장점

Jquery를 통해 쉽게 구현이 가능하다.
Error, Success, Complate의 상태를 통해 실행 흐름 조절이 가능하다.

### 단점

Jquery를 사용해야 간편하고 호완성이 보장된다.
Promise기반이 아니다.

## axios

axios는 Node.js와 브라우저를 위한 Promise API를 활용하여 HTTP 통신 라이브러이다.
비동기로 HTTP 통신을 할 수 있으며 return을 promise 객체로 해주기 때문에 response 데이터를 다루기 쉽다.

### 장점

response timeout (fetch에는 없는 기능)처라 방법이 존재하다.
Promise 기반으로 만들어졌기 때문에 데디터 다루기 편리하다.
브라우저 호환성이 뛰어나다.

### 단점

사용을 위해서 모듈을 설치해야한다. (npm install axios)

## fetch

EX6부터 들어온 JavaScript내장 라이브러라이다.
Promise 기반으로 만들어졌기 때문에 axios와 마찬가지로 데이터를 다루기 쉽다.
내장 라이브러리라는 장점이 있다.

### 장점

자바스크립트 내장 라이브러리이므로 별도로 import 할 필요가 없다.
Promise 기반으로 만들어졌기 때문에 데이터 다루기가 편리하다.
내장 라이브러리이기 때문에 업데이트에 따른 에러 방지가 가능하다.

### 단점

지원하지 않는 브라우저가 존재한다. (IE 11)
네트워크 에러 발생 시 response timeout이 없이 기다려야 한다.
JSON으로 변환해주는 과정이 필요하다.
axios에 비해 기능이 부족하다.
