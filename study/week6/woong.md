## 이벤트 위임이란 무엇인가요?
자식 요소인 타겟에서 이벤트가 발생하면 버블링이 되어 document까지 올라가므로 자식 요소에서 발생하는 이벤트를 부모 요소에서도 알 수 있습니다.
따라서 자식 요소들에게 하나씩 이벤트를 등록하는 것이 아닌 부모에게만 이벤트를 등록하여 자식 요소들이 같은 이벤트를 가질 수 있게 하는 것을 이벤트 위임이라고 합니다.
https://ui.toast.com/weekly-pick/ko_20160826
## React Virtual DOM 작동 원리에 대해 설명해주세요.
React의 Virtual DOM은 실제 돔을 복제한 자바스크립트 객체입니다.
기존의 렌더링 방식은 변경이 일어났을 때 리플로우가 발생해 렌더트리를 다시 그리는 비용이 큰 작업을 하는데
Virtual DOM은 변경이 일어난 부분에 대해서만 실제 돔과 비교하여 교체하는 방식을 사용하여 비용을 낮추려는 방식입니다.
https://ko.legacy.reactjs.org/docs/faq-internals.html#gatsby-focus-wrapper
https://velopert.com/3236
https://www.youtube.com/watch?v=Bdk7QzbbcEI&t=312s
## useMemo와 useCallback에 대해 설명해주세요.
리렌더링을 방지하기 위한 메모이제이션 관련 훅으로는
useCallback과 useMemo가 있습니다.
useCallback은 함수에 대한 메모이제이션,
useMemo는 값에 대한 메모이제이션을 제공합니다.
https://react.vlpt.us/basic/17-useMemo.html
