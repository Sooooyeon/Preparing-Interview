## this의 용법에 대해 아는대로 설명해주세요. ##

전역 실행 맥락에서 this는 엄격 모드 여부에 관계 없이 전역 객체를 참조합니다.<br>

함수 내부에서 this의 값은 함수를 호출한 방법에 의해 좌우됩니다.
- 단순 호출에서 엄격 모드일 경우 this 값은 실행 문맥에 진입하며 설정되는 값을 유지합니다.
- 화살표 함수에서 this는 자신을 감싼 정적 범위입니다. 전역 코드에서는 전역 객체를 가리킵니다.
- 함수를 어떤 객체의 메서드로 호출하면 this의 값은 그 객체를 사용합니다.
- 함수를 접근자와 설정자에서 호출하더라도 접근자나 설정자로 사용하는 함수의 this는 접근하거나 설정하는 속성을 가진 객체로 묶입니다.
- 함수를 new 키워드와 함께 생성자로 사용하면 this는 새로 생긴 객체에 묶입니다.
- 함수를 이벤트 처리기로 사용하면 this는 이벤트를 발사한 요소로 설정됩니다.
- 코드를 인라인 이벤트 처리기로 사용하면 this는 처리기를 배치한 DOM 요소로 설정됩니다.

[MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/this#%ED%95%A8%EC%88%98_%EB%AC%B8%EB%A7%A5)

## React의 라이프 사이클에 대해 설명해주세요. ##

라이프 사이클은 크게 세가지 유형으로 나눌 수 있는게 그것은 컴포넌트가 로딩되기 시작하는 Mounting, 컴포넌트의 업데이트인 Updating 그리고 컴포넌트의 삭제 Unmounting 입니다.<br>

Mounting 부분에는 먼저 constructor(클래스 생성자) 메소드가 실행됩니다. constructor는 클래스 인스턴스 객체를 생성하고 초기화하는 메소드로 리액트에서 컴포넌트를 만들 때 처음으로 실행됩니다.
constructor메소드가 실행된 이후에는 props로 받아 온 값을 state에 동기화시키는 용도로 사용하는 getDerivedStateFromProp 메소드가 실행됩니다. 이후 실행되는 shouldComponentUpdate 메소드는 기본적으로 true를 반환합니다.
조건에 따라 false를 반환하면 해당 조건에는 render 함수를 호출하지 않습니다. true로 반환을 했다면 render 메소드가 실행됩니다. render 메소드가 실행되면서 JSX가 HTML로 변환되어 우리가 보는 웹 브라우저에 나타나게 됩니다.
마지막으로 render 메소드에 있는 모든 부분들이 브라우저에 나타나게 되었을 때만 실행되는 componentDidMount 메소드가 실행되면서 mounting부분은 끝이납니다.<br>

업데이트는 Props나 State가 바뀔때, 부모 컴포넌트가 리렌더링 될 때, 그리고 this.forceUpdate로 강제로 렌더링을 trigger하는 상황에서 발생합니다.
업데이트 부분에서는 먼저 컴포넌트가 새로운 속성을 전달받을 때 실행되는 componentWillReceiveProps 메소드가 호출됩니다. 
그 후 Mounting 부분에서도 실행되는 shouldComponentUpdate가 실행되고 true로 반환이 됐다면 render 메소드를 실행합니다. render 메소드가 실행이 됐다면 차례대로 getSnapShotBeforeUpdate, componentWillUpdate가 차례대로 호출됩니다.
마지막으로 componentDidUpdate 메소드가 실행되고 업데이트 부분이 끝납니다.<br>

Unmount는 JSX에 포함되었다가 이후에 제거되는 경우에 발생합니다.
Unmounting 부분에는 컴포넌트를 DOM에서 제거할 때 실행하는 ComponentWillUnmount 메서드를 실행합니다.

[참고자료1](https://ljh86029926.gitbook.io/coding-apple-react/2/undefined-1/what-is-life-cycle)
[참고자료2](https://velog.io/@remon/React-%EB%A6%AC%EC%95%A1%ED%8A%B8-%EB%9D%BC%EC%9D%B4%ED%94%84-%EC%82%AC%EC%9D%B4%ED%81%B4)

## 이벤트 전파(버블링, 캡처링)에 대해 설명해주세요. ##

**이벤트 버블링**은 한 요소에 이벤트가 발생하면, 이 요소에 할당된 핸들러가 동작하고, 이어서 부모 요소의 핸들러가 동작한 뒤
가장 최상단의 조상 요소를 만날 때까지 이 과정이 반복되면서 요소 각각에 할당된 핸들러가 동작하는 원리를 가지고 있습니다.
거의 모든 이벤트는 버블링 되지만 focus 이벤트와 같이 버블링 되지 않는 몇몇 이벤트도 있습니다. <br>

**이벤트 캡처링**은 이벤트 버블링과는 반대로 이벤트가 하위 요소로 전파되는 이벤트 전파 방식입니다. 

[참고자료](https://ko.javascript.info/bubbling-and-capturing)

