### 1. 렉시컬 환경과 렉시컬 스코프에 대해 설명해주세요.
렉시컬 환경이란 특정 코드가 작성, 선언된 환경을 의미합니다. 
자바스크립트에서 실행 중인 함수, 코드 블록 {...}, 스크립트 전체는 렉시컬 환경(Lexical Environment) 이라 불리는 내부 숨김 연관 객체(internal hidden associated object)를 갖습니다.
렉시컬 환경 객체는 모든 지역 변수를 프로퍼티로 저장하고 있는 객체인 환경 레코드(Environment Record)와 외부 렉시컬 환경(Outer Lexical Environment) 에 대한 참조로 구성됩니다.

렉시컬 스코프란 렉시컬 특성을 활용한 스코프 방식으로 렉시컬 환경의 ‘외부 렉시컬 환경에 대한 참조’에 저장할 참조값,
즉 상위 스코프에 대한 참조는 함수가 정의되는 시점에 함수가 정의된 환경(위치)에 의해 결정되는 것을 말합니다.

[변수의 유효 범위와 렉시컬 환경](https://lakelouise.tistory.com/166)</br>
[렉시컬 환경](https://ko.javascript.info/closure#ref-151)</br>
[클로저와 렉시컬 환경](https://hanna-log.tistory.com/472)</br>

</br>

### 2. 이벤트 루프에 대해 설명해주세요.
이벤트 루프(Event Loop)는 싱글 스레드인 자바스크립트의 작업을 멀티 스레드로 돌려 작업을 동시에 처리시키게 하며, 여러 작업 중 어떤 작업을 우선으로 동작시킬 것인지 컨트롤 합니다.
브라우저 내부의 Call Stack, Callback Queue, Web APIs 등의 요소들을 모니터링하면서 비동기적으로 실행되는 작업들을 관리하고, 이를 순서대로 처리하여 프로그램의 실행 흐름을 제어합니다.

[이벤트 루프 동작 구조](https://inpa.tistory.com/entry/%F0%9F%94%84-%EC%9E%90%EB%B0%94%EC%8A%A4%ED%81%AC%EB%A6%BD%ED%8A%B8-%EC%9D%B4%EB%B2%A4%ED%8A%B8-%EB%A3%A8%ED%94%84-%EA%B5%AC%EC%A1%B0-%EB%8F%99%EC%9E%91-%EC%9B%90%EB%A6%AC)

</br>

### 3. JavaScript에서 비동기 실행은 어떻게 하나요?
JavaScript에서는 async/await 방식으로 비동기 처리를 동기 처리처럼 구협합니다. 
async/await는 Promise를 기반으로 동작하며, then/catch/finally와 같은 후속 처리 메서드 없이 마치 동기 처리처럼 사용할 수 있습니다.
이전에 콜백 함수나 Promise를 사용해 비동기 처리를 할 때는 무조건 api를 호출한 후, 또 다른 콜백 함수를 실행하여 데이터의 처리가 가능했지만,
async/await는 해당 함수 내부에서 바로 동기 처리처럼 데이터를 수정할 수 있습니다. 또한, try/catch 문으로 에러 처리도 훨씬 수월합니다.

[비동기](https://www.howdy-mj.me/javascript/asynchronous-programming)
