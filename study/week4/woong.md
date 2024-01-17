### 4주차 Question
1. ### 렉시컬 환경과 렉시컬 스코프에 대해 설명해주세요.
   렉시컬 환경은 코드 실행 컨텍스트에 대한 정보를 담고 있으며, 주로 변수와 스코프와 관련된 정보를 관리합니다.
   렉시컬 환경에는 Environment Record와 Outer Environment Reference라는 두 가지 구성 요소가 있습니다.
   Environment Record는 현재 스코프 내에서 선언된 변수와 함수 등의 식별자에 대한 정보를 저장합니다.<br/>
   Outer Environment Reference는 현재 렉시컬 환경과 연결된 상위 렉시컬 환경을 가리킵니다.이것이 스코프 체인을 형성하며,
   변수를 찾을 때 외부 스코프로 이동할 수 있도록 합니다.<br/>
   렉시컬 스코프는 함수나 블록이 정의(선언)된 위치에 기반하여 스코프를 결정합니다.
   https://www.youtube.com/watch?v=OPc73p2d0T8
2. ### 이벤트 루프에 대해 설명해주세요.
   이벤트 루프는 콜 스택과 태스크 큐를 모니터링을 하고 콜 스택이 비어있을 때 태스크 큐에 있는 작업을 콜 스택으로 보내주어
   실행시키는 역할을 합니다.
   https://www.youtube.com/watch?v=QFHyPInNhbo
3. ### JavaScript에서 비동기 실행은 어떻게 하나요?
   콜백 함수 : 콜백 함수는 자바스크립트에서 다른 함수 안에 넣어서 사용하는 함수입니다.
   setTimeout 함수는 비동기적으로 동작하므로 태스크 큐에서 대기하다 콜 스택이 비워지면 실행되게 되는 비동기 실행이 일어납니다.<br/>
   Promise : Promise는 비동기 작업의 성공 또는 실패를 다루기 위한 객체입니다. 프로미스는 성공 시 "resolve" 콜백 함수가 실행을,
   실패하면 "reject" 콜백 함수가 실행됩니다.<br/>
   Async/Await : async를 함수 앞에 붙이면 그 함수는 비동기 함수가 되고 항상 Promise 객체를 반환합니다.
   await은 비동기로 처리되는 부분 앞에 붙이면 Promise를 반환할 때까지 기다립니다.
   https://inpa.tistory.com/entry/JS-%F0%9F%93%9A-%EB%B9%84%EB%8F%99%EA%B8%B0%EC%B2%98%EB%A6%AC-async-await

