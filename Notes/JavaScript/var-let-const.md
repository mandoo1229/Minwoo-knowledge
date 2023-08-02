## var

ES6가 등장하기 전에는 대부분 var를 사용하였다. 그러나 var로 선언된 변수에는 몇 몇 문제가 있었고, 이를 보완하기 위해 새로운 변수 선언 방식이 등장해야만 했다.

### var의 스코프

- 스코프(scope)는 기본적인 변수를 사용할 수 있는 위치를 의미한다. var선언은 전역(global)변수로 사용되거나 함수, 지역(local)변수로도 사용된다.
- var변수가 함수 외부에 선언되면 스코프는 전역(global)이 된다. 즉, 함수 블록 외부에 var로 선언된 모든 변수를 전체 window에서 사용할 수 있다.
- var가 함수 내에서 선언되면 함수 스코프르 갖는다. 즉, 해당 함수 내에서만 사용 가능하며, 액세스 할 수 있다.

```
var minoo = "hi minwoo";
function newFunction () {
   var hello = "hello";
}
```

여기서 minoo는 ㅎ마수 밖에 존재하는 전역 스코프이며, hello는 함수 내에 있으므로 함수 스코프이다. 그래서 함수 밖에서는 hello에 접근할 수 없다.

```
var test = "hey hi";
기능 newFunction() {
  var hello = "hello";
}
console.log(hello); //오류: hello가 정의 되지 않았다.
```

함수 밖에서는 hello를 사용할 수 없기 때문에 오류가 발생한다.

### var는 재선언 및 업데이트가 가능하다.

즉, var는 아래와 같이 동일한 스코프 내에서 변수 재선언을 할 수 있고 오류가 발생하지 않는다.

```
var test = "Hi Minwoo";
var test = "By Minwoo";l
```

그리고 업데이트도 가능하다.

```
var test = "Hi minwoo";
test = "By Minwoo";
```

### var의 호이스팅

**JavaScript에서 호이스팅(hoisting)이란?**

> 인터프리터가 변수와 함수의 메모리 공간을 선언 전에 미리 할당하는 것을 의미한다. var로 선언한 변수의 경우 호이스팅 시 undefied로 변수를 초기화 한다. 반면 let과 const로 선언한 변수의 경우 호이스팅 시 변수를 초기화 하지 않는다.
> 호이스팅을 설명할 땐 주로 "변수의 선언과 초기화를 분리한 후, 선언만 코드의 최상단으로 옮기는"것으로 말하곤 한다. 따라서 변수를 정의하는 코드보단 사용하는 코드가 앞서 등장할 수 있다. 다만 선언과 초기화를 함께 수행하는 경우, 선언 코드까지 실행해야 변수가 초기화된 상태가 됨을 주의해야한다.

호이스팅은 변수와 함수 선언이 코드 실행 전에 해당 스코프의 맨 위로 이동하는 자바스크립트 매커니즘이다. 즉, 아래와 같은 코드를 실행하면

```
console.log(test);
var test = "hello"
```

다음과 같이 해석된다.

```
var test;
console.log(test); //test is undefined
test = "hello"
```

즉, var변수는 해당 스코프의 맨 위로 올라가고 undefined 값으로 초기화 된다.

### var의 문제점

하지만 var에는 문제점이 있다.

```
var test = "hello Minwoo";
var times = 4;
if (times > 3) {
   var test = "By Minwoo";
}
console.log(test) //"By Minwoo"
```

times > 3는 true를 반환하기 때문에, test는 처음에 정의된 "hello Minwoo"대신, "By Minwoo"로 다시 정의 된다. test를 다시 정의하려는 경우에는 문제가 되지 않지만 test가 이전에 이미 정의되어 있다는 것을 인지하지 못하는 경우에는 문제가 된다.
즉, 코드의 다른 부분에서 test를 사용한 경우, 의도하지 않는 값이 출력될 수 있으며, 코드에 많은 버그가 발생할 수 있다. 그래서 let과 const가 필요한 이유이다.

### let

최근 변수 선언에는 let이 더 선호된다. let은 앞서 설명한 var의 문제점을 해결해준다.

### let은 블록 스코프 내에서 작동한다.

블록(block)은 {}으로 바인딩된 코드 덩어리이다. 즉, {}안에 있는 것들은 모두 블록이다.
따라서 블록에 let으로 선언된 변수에는 해당 블록 내에서만 사용할 수 있다.

```
let test = "Hi Minwoo";
let times = 4;

if (times > 3) {
   let hello = "Hello Minwoo";
   console.log(hello);  // "Hello Minwoo"
}
console.log(hello) //hello is not defined
```

블록 외부에서 hello를 사용하면 undifined오류가 반환된다. 이는 let변수는 블록 스코프내에서만 작동되기 때문이다.

### let은 업데이트할 수 있지만 재선언은 할 수 없다.

var와 마찬가지로, let으로 선언된 변수는 스코프 내에서 업데이트될 수 있다. 하지만, var와 달리 let 변수는 해당 스코프 내에서 다시 선언할 수 없다.
아래 코드는 작동이 되지만

```
let test = "Hi Minoo";
test = "Hello Minwoo";
```

아래는 오류를 오류를 반환한다.

```
let test = "Hi Minwoo";
let test = "Hello Minoo"; // error: Identifier 'greeting' has already been declared
```

그러나 동일한 변수가 다른 스코프에서 정의되면 오류가 발생하지 않는다.

```
let test = "Hi Minwoo";
if (true) {
   let test = "Hello Minwoo";
   console.log(test); //"Hello Minwoo";
}
console.log(test); //"Hi Minwoo";
```

오류가 나지 않는 이유는 두 인스턴스의 스코프가 다르기 때문에 아예 다른 변수로 취급되기 때문이다.
그래서 **let**이 **var**보다 더 선호된다. **let**을 사용할 때는 변수가 해당 스코프 내에서만 존재하므로, 이전에 동일한 변수명을 사용한적이 있는지 없는지 신경쓸 필요가 없다.
또한 변수는 한 스코프 내에서 두 번 이상 선언될 수 없기 때문에 앞에서 얘기한 **var**의 문제는 더이상 발생하지 않는다.

### let호이스팅

**var**처럼, **let**은 선언을 최상단으로 끌어올린다. 하지만 **undifined**으로 초기화되는 **var**와 달리 **let**변수는 초기화되지 않는다. 따라서 선언 전에 **let** 변수를 사용하려고 하면 Reference Error가 발생한다.

### const

const로 선언된 변수는 상수 값을 유지한다. const선언은 let선언과 몇 가지 유사점을 공유한다.

### const 선언은 블록 스코프이다.

let선언과 마찬가지로, const 선언은 선언된 블록 내에서만 접근할 수 있다.

### const를 업데이트하거나 다시 선언할 수 없다.

즉, const로 선언된 변수의 값은 해당 스코프 내에서 항상 동일하게 유지됨을 의미한다. const로 선언된 변수는 업데이트하거나 다시 선언할 수 없다. 따라서 변수를 const로 선언하면 아래 작업을 수행할 수 없다.

```
const test = "Hi Minwoo";
test = "Hello Minwoo" //error: Assignment to constant variable.
```

동일하게 아래 작업도 수행할 수 없다.

```
const test = "Hi Minwoo";
const test = "Hello Minwoo";
```

따라서 모든 const는 첫 선언에서 초기화 되어야 한다.
하지만 const로 선언된 객체(object)에 대해서는 다소 다르게 동작한다. const 객체는 업데이트할 수 없지만 이 객체의 속성은 업데이트할 수 있다. 따라서 const 객체를 다음과 같이 선언하면

```
const test = {
   message: "Hi Minwoo",
   times: 4
}
```

아래와 같이 변경할 수 없지만

```
test = {
   words: "Hello".
   number: "five"
} //error: Assignment to constant variable.
```

다음을 수행할 수 있다.

```
test.message = "Hi Minwoo";
```

이렇게 하면 오류를 반환하지 않고 test.message값이 업데이트 된다.

### const의 호이스팅

let과 마찬가지로 const 선언 역시 최상단으로 호이스팅 되지지만, 초기화되지는 않는다.

마무리 정리

- var선언은 전역 혹은 함수 스코프지만, let 및 const는 블록 스코프이다.
- var변수는 해당 스코프 내에서 업데이트 및 재선언 될 수 있다. let변수는 업데이트될 수 있지만 재선언할 수 없다. const변수는 업데이트와 재선언 모두 불가하다.
- 세가지 모두 최상단으로 호이스팅된다. 차이점은, var는 undefined 상태로 초기화 되지만, let과 const는 초기화 되지 않는다.
- var와 let은 초기화하지 않고 선안할 수 있지만, const는 선언과 동시에 초기화해야 한다.
