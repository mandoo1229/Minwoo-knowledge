## ⭐️JSON

- JSON이란, JavaScript Object Notation라는 의미로 추약어로 데이터를 저장하거나 전송할 때 사용되는 경량의 DATA 교환 형식이다.
- JavaScript에서 객체를 만들 대 사용하는 표현식을 의미한다.
- JSON 표현식은 사람과 기계 모두 이해하기 쉬우며 용량이 작아서, 최근에는 JSON이 XML을 대체해서 데이터 전송등에 많이 사용한다.
- JSON은 데이터 포맷일 뿐이며 어떠한 통신 방법도, 프로그래밍 방법도 아닌 단순히 데이터를 표시하는 표현 방법이다.

## ⭐️JSON의 특징

- 서버와 클라이언트 간의 교류에서 일반적으로 많이 사용한다.
- JavaScript 객체 표기법과 아주 유사하다.
- JavaScript를 이용하여 JSON 형식의 문서를 쉽게 JavaScript 객체로 변환할 수 있는 이점이 있다.
- JSON 문서 형식은 JavaScript 객체의 형식을 기반으로 만들어졌다.
- JavaScript 문법과 유사하지만 텍스트형식일 뿐이다.
- JavaScript뿐만 아니라 다른 프로그래밍 언어를 이용해서도 쉽게 만들 수 있다.
- 특정 언어에 종속되지 않는다. 대부분의 프로그래밍 언어에서 JSON 포맷의 데이터를 핸들링 할 수 있는 라이브러리를 제공한다.

## ⭐️JONS 문법

- XML처럼 태그로 표현하기 보다는 중괄호{} 형식으로 하고, 값을 , 로 나열하기에 표현이 간단하다.
- JSON 형식은 JavaScript 객체와 마찬가지로 key/value 형식으로 구성되며, key값이나 문자열은 항상 쌍따옴표("")를 이용하여 표기한다.
- 객체, 배열 등의 표기를 사용할 수 있다.
- 일반 JavaScript 객체처럼 원하는 만큼 중첩시켜서 사용할 수 있다.
- JSON형식에는 null, number, string, array, object, boolean을 사용할 수 있다.

```
{
  "employees": [
    {
      "name": "Minwoo",
      "lastName": "Nam"
    },
    {
      "name": "Junghyeon",
      "lastName": "Nam"
    },
  ]
}  //JSON 타입이다.
```

## ⭐️JSON형식

### name-value 형식의 쌍

- 여러가지 언어들에는 object, hashtable, struct로 실현되었다.
- {String key: String value}

```
  {
    "firstName": "Nam",
    "lastName": "Minwoo",
    "email": "skaalsdn35@gmail.com"
  }
```

## ⭐️JSON을 JavaScript Object로 변환

- JSON.parse(JSON으로 변화시킬 문자열): JSON형식의 텍스트를 JavaScript 객체로 변환
- JSON.stringify(JSON 문자열로 변환할 값) : JavaScript 객체를 JSON 텍스트로 변환한다.

```
const jsonText = '{ "name": "Minwoo", "lastName:"Nam"}';
const realObject = JSON.parse(jsonText);
const jsonText2 = JSON.stringify(realObject);
```

console.log(realObject); // { name: 'Minwoo', lastName:'Nam' }
console.log(jsonText2); // { "name":"Minwoo", "lastName":"Nam"}
