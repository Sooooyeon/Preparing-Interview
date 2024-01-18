## 렉시컬 환경과 렉시컬 스코프에 대해 설명해주세요. ##
### 렉시컬 환경(Lexical Environment) ###
렉시컬 환경은 실행할 스코프 범위 안에 있는 변수와 함수를 프로퍼티로 저장하는 객체입니다.
렉시컬 환경은 환경 레코드(Environment Record)와 외부 렉시컬 환경(Outer Lexical Environment) 이 두 부분으로 구성되어 있습니다.
이때, 환경 레코드에는 현재 실행중인 코드 환경의 this값과 선언된 모든 변수와 함수가 저장되고 외부 렉시컬 환경에는 부모 환경의 렉시컬 환경 참조값을 가지고 있어 부모 변수에 접근할 수 있습니다.

[참고자료1](https://developer-alle.tistory.com/407)<br>
[참고자료2](https://kwangsunny.tistory.com/37)

### 렉시컬 스코프(Lexical Scope) ###
렉시컬 스코프는 함수를 어디에 호출하였는지가 아니라 선언하였는지에 따라 상위 스코프가 결정되는 것을 의미합니다.
다른말로 정적 스코프라고 부르기도 합니다.

[참고자료1](https://ziszini.tistory.com/64)<br>
[참고자료2](https://ljtaek2.tistory.com/145)

## 이벤트 루프에 대해 설명해주세요. ## 
자바스크립트는 싱글 스레드 언어이기 때문에 작업을 하나씩만 수행할 수 있고 다수의 작업을 동시에 수행하는 것은 불가능합니다.
하지만 브라우저가 동작하는 것을 살펴보면 많은 작업들이 동시에 실행되는 것처럼 보이는데 이를 가능하게 해주는 것이 이벤트 루프(Event Loop)이며 이벤트 루프는 자바스크립트에게 동시성을 지원해줍니다.
또한 자바스크립트를 구동하는 환경인 브라우저나 Node.js에서 제공하는 다양한 기능 중 하나입니다.<br>
이벤트 루프는 현재 실행중인 Task가 있는지, Queue들에 적재된 Task가 있는지 주기적으로 확인하고,
만약 실행중인 Task가 Call Stack에 없다면 Queue에서 Task를 꺼내와 Call Stack에 올리고 실행시키는 역할을 합니다.

[참고자료1](https://leo-xee.github.io/JavaScript/eventloop/)<br>
[참고자료2](https://gruuuuu.github.io/javascript/async-js/)

## JavaScript에서 비동기 실행은 어떻게 하나요? ##
자바스크립트의 비동기 실행은 특정 코드의 연산이 끝날 때까지 코드의 실행을 멈추지 않고 다음 코드를 먼저 실행합니다.
비동기 실행을 함으로써 동시에 여러가지 작업을 처리할 수 있고 기다리는 과정에서 다른 함수를 호출할수도 있습니다.

[참고자료1](https://kkhcode.tistory.com/6)
