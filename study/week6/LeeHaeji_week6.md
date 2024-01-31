## 이벤트 위임이란 무엇인가요? ##
이벤트 위임이란 사용자의 액션에 의해 이벤트 발생 시 이벤트 버블링에 의해 document 레벨까지 버블링 되어 올라가는데 이 때문에 자식 엘리먼트에서 발생하는 이벤트를 부모 엘리먼트에서도 감지할 수 있습니다. 
이러한 작동 방식을 이용해 자식 엘리먼트의 하나하나에 모든 이벤트를 주는 것이 아닌 부모에게만 이벤트를 위임하는 방법입니다.
이벤트 위임은 많은 핸들러를 할당하지 않아도 되기 때문에 초기화가 단순해지고 메모리가 절약되며 요소를 추가하거나 제거할 때 해당 요소에 할당된 핸들러를 추가하거나 제거할 필요가 없기 때문에 코드가 짧아진다는 장점이있습니다.

[이벤트 위임이란?](https://velog.io/@hovelopin/JS-%EC%9D%B4%EB%B2%A4%ED%8A%B8-%EC%9C%84%EC%9E%84-ax11zcnh)<br>
[코어자바스크립트](https://ko.javascript.info/event-delegation)

## React Virtual DOM 작동 원리에 대해 설명해주세요. ##
React는 실제 DOM의 UI를 가진 JavaScript 객체를 메모리상에 가지고 있습니다. 이 Vitual DOM은 변화를 감지하면 재조정(Reconcilation) 과정을 통해 실제 DOM과 동기화 합니다.
재조정 과정은 크게 3단계로 나뉩니다. 먼저 UI가 변경을 감지하면 UI를 Virtual DOM으로 렌더링합니다. 이때 실제 화면 상에 렌더링 되는 것이 아니라 비교를 위한 가상 렌더링입니다.
다음으로 현재 Virtual DOM과 이전 Virtual DOM을 비교해 차이를 계산합니다. 그 뒤 변경된 부분을 실제 DOM에 반영하면서 재조정을 끝냅니다.

[React Virtual DOM 비교 원리](https://babycoder05.tistory.com/entry/React-Virtual-DOM-%EA%B3%BC-%EB%B9%84%EA%B5%90-%EC%9B%90%EB%A6%AC%EC%99%80-%EC%96%95%EC%9D%80-%EB%B9%84%EA%B5%90)

## useMemo와 useCallback에 대해 설명해주세요. ##

useMemo는 메모이제이션된 값을 반환하는 함수입니다. useMemo를 사용하면 리렌더링이 발생할 경우, 특정 변수가 변할 때에만 useMemo에 등록한 함수가 실행되도록 처리하면 불필요한 연산을 하지 않게 됩니다. 특히, 복잡한 계산이나 외부 데이터가 필요한 작업에 특히 유용합니다.
useCallback은 메모이제이션된 함수를 반환하는 특징을 가지고 있습니다. 메모이제이션된 함수는 콜백 함수의 의존성이 변경되었을 때에만 변경되며 이는 불필요한 렌더링을 방지하기 위해 참조의 동일성을 보장하거나, 자식 컴포넌트에 의존적인 콜백 함수를 전달할 때 유용합니다.

[참고자료1](https://leehwarang.github.io/2020/05/02/useMemo&useCallback.html)<br>
[참고자료2](https://narup.tistory.com/273)<br>
[참고자료3](https://velog.io/@khy226/useMemo%EC%99%80-useCallback-%ED%9B%91%EC%96%B4%EB%B3%B4%EA%B8%B0)
