## 1. Reflow와 Repaint가 실행되는 시점 ##

~~최초 페이지가 로딩되면 렌더링 작업이 진행됩니다. 이후 렌더링이 모두 완료된 상태에서 사용자의 인터랙션 또는 해당 페이지의 기능에 따라 화면의 일부 영역에 변경 요인이 발생합니다.
이러한 작업이 발생하면 구성돼 있는 렌더 트리가 변경돼야 하며 리플로우 또는 리페인트가 발생합니다.~~<br>

~~Reflow~~<br>
~~브라우저가 웹 페이지의 위치와 기하학적 구조를 다시 계산할 때 리플로우가 발생~~<br>

~~Repaint~~<br>
~~UI 변경으로 인한 시각적 업데이트를 표시하기 위해 브라우저가 웹 페이지를 다시 그릴 때 발생~~<br>

[👇수정]
> 최초 페이지가 로딩되면 렌더링 작업이 진행됩니다. 이후 렌더링이 모두 완료된 상태에서 사용자의 인터랙션 또는 해당 페이지의 기능에 따라 화면의 일부 영역에 변경 요인이 발생합니다.
이러한 작업이 발생하면 구성돼 있는 렌더 트리가 변경돼야하며 리플로우 또는 리페인트가 발생합니다. 이때 Reflow는 브라우저가 웹 페이지의 위치와 기하학적 구조를 다시 계산할 때 리플로우가 발생하며 Repaint는 UI 변경으로 인한 시각적 업데이트를 표시하기 위해 브라우저가 웹 페이지를 다시 그릴 때 발생합니다.

[참고자료1](https://12bme.tistory.com/140)<br>
[참고자료2](https://developer.mozilla.org/ko/docs/Glossary/Reflow)<br>
[참고자료3](https://developer.mozilla.org/ko/docs/Glossary/Repaint)

## 2. 클로저(Closure)란? ##

> 클로저는 함수와 함수가 선언된 어휘적 환경의 조합입니다.
여기서, 환경이란 클로저가 생성된 시점의 유효 범위 내에 있는 모든 지역 변수로 구성됩니다.
그리고 클로저는 함수가 속한 렉시컬 스코프를 기억하여 함수가 렉시컬 스코프 밖에서 실행될 때도 그 스코프에 접근할 수 있도록 하는 기능을 합니다.

[참고자료1](https://github.com/Esoolgnah/Frontend-Interview-Questions/blob/main/Notes/important-5/closure.md)<br>
[참고자료2](https://developer.mozilla.org/ko/docs/Web/JavaScript/Closures)<br>
[참고자료3](https://velog.io/@wngud4950/%ED%81%B4%EB%A1%9C%EC%A0%80Closure%EB%9E%80)

## 3. 마이크로태스크 큐, 태스크 큐 ##

~~마이크로태스크 큐와 태스크 큐 모두 콜백함수가 들어가지만 들어가는 콜백 함수의 종류가 다릅니다.
마이크로 태스크 큐에는 Promise의 콜백 함수가 들어가며, 태스크 큐에는 setTimeout, setInterval의 콜백 함수가 들어갑니다.
그리고 이벤트 루프는 마이크로 태스크 큐에 있는 모든 태스크를 먼저 처리하고 태스크 큐에있는 태스크를 처리합니다.~~<br>

[👇수정]
> 마이크로태스크 큐와 태스크 큐 모두 콜백함수가 들어가지만 들어가는 콜백 함수의 종류가 다릅니다.
마이크로 태스크 큐에는 Promise와 함께 쓰이는 .then/catch/finally 핸들러인 마이크로태스크가 들어가며 여기에 더하여 Promise를 핸들링하는 또 다른 문법인 await를 한 콜백함수가 들어가기도 합니다. 태스크 큐에는 setTimeout, setInterval의 콜백 함수가 들어갑니다.
그리고 마이크로 태스크 큐의 우선순위가 태스크 큐보다 높기때문에 이벤트 루프는 마이크로 태스크 큐에 있는 모든 태스크를 먼저 처리한 뒤 태스크 큐에있는 태스크를 처리합니다

[참고자료1](https://developer.mozilla.org/ko/docs/Web/API/HTML_DOM_API/Microtask_guide)<br>
[참고자료2](https://developer.mozilla.org/ko/docs/Web/API/HTML_DOM_API/Microtask_guide)<br>
[참고자료3](https://ko.javascript.info/event-loop)

