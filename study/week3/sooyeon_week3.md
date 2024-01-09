### 1. Reflow와 Repaint가 실행되는 시점에 대해 설명해주세요.
reflow는 생성된 DOM 노드의 레이아웃 수치(너비, 높이, 위치 등) 변경 시 영향 받은 모든 노드의(자신, 자식, 부모, 조상(결국 모든 노드) ) 수치를 다시 계산하여(Recalculate),
렌더 트리를 재생성하는 과정으로 DOM 노드의 추가/제거, DOM 노드의 위치/크기 변경 (width, margin, border 등), Window 창 크기 조절 (위치/크기 값이 상대 값일 경우)
CSS 애니메이션과 트랜지션 사용, 계산된 css 정보 요청(offset, scrollTop 등), 폰트 변경, 이미지 크기 변경, 텍스트 변경 등이 발생하는 경우 실행됩니다.</br></br>
repaint는 reflow 과정이 끝난 후 재생성된 렌더 트리를 다시 그리는 작업으로 화면의 구조가 변경이 될 때는 reflow와 repaint가 모두 발생합니다.
다만, repaint가 발생하기 위해서 항상 reflow가 발생해야 하는 것은 아닙니다. 
수치와 상관없는 color, background-color, visibilityr 등의 스타일 속성 변경 시에는 reflow 과정을 생략한 repaint 작업만 실행됩니다.</br></br>
[참고링크1](https://devowen.com/463) [참고링크2](https://k0102575.github.io/articles/2020-11/reflow-repaint)</br></br>

### 2. 클로저(Closure)란?
자바스크립트는 함수 안에서 또 다른 함수를 선언할 수 있으며 내부함수는 외부함수의 변수에 접근할 수 있습니다.
외부함수의 실행이 끝나서 외부함수가 사라진 이후에도 내부함수가 외부함수의 변수를 참조하는 것을 클로저라고 합니다.</br></br>


### 3. 마이크로태스크 큐, 태스크 큐에 대해 설명해주세요.
자바스크립트는 '단일 스레드' 기반의 언어지만 여러 작업이 동시에 처리됩니다. 이러한 작업에 필요한 것이 '이벤트 루프'이며, 자바스크립트는 태스크를 처리하는 이벤트 루프를 통해 비동기 방식으로 동시 작업을 지원합니다.
비동기 작업은 태스크큐에서 대기하다가 콜 스택으로 넘어가서 실행되는데, 여기서 태스크큐는 마이크로 태스크(micro task)와 매크로 태스크(macro task)로 분리됩니다. 
마이크로 태스크 큐는 매크로 태스크 큐에 비해 우선순위가 높아 콜 스택이 비워지면 마이크로 태스크 큐를 먼저 확인 후 실행하게 되고, 모든 마이크로 태스크 큐가 비워지면 매크로 태스크 큐를 실행합니다.
콜백 함수를 매크로 태스크 큐로 넣는 함수들은 setTimeout, setInterval, setImmediate, I/O, UI 렌더링 등이 있으며,
콜백 함수를 마이크로 태스크 큐로 넣는 함수들은 Promise, process.nextTick, Object.observe, MutationObserver 등이 있습니다.</br></br>

[참고링크1](https://haesoo9410.tistory.com/322) [참고링크2](https://meetup.nhncloud.com/posts/89)
