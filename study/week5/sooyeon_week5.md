### 1. this의 용법에 대해 아는대로 설명해주세요.
전역에 선언된 함수에서 this는 항상 window라는 전역 객체를 참조합니다.
this를 객체의 메소드로 사용한 경우 this는 현재 함수를 실행하고 있는 객체를 참조합니다.
함수 내부에서 this의 값은 함수를 호출하는 방법에 의해 달라집니다.
또 엄격 모드가 적용되는 경우 참조 값이 달라지는데, 엄격 모드가 적용 시 일반 함수 내부의 this는 undefinded 가 바인딩 됩니다.
화살표 함수에서는 함수를 선언할 때 this에 바인딩할 객체가 정적으로 결정되는데,
객체 결정 방식은 함수의 상위 스코프를 결정하는 방식인 렉시컬 스코프와 유사해 화살표 함수 안에서 this는 언제나 상위 스코프의 this를 가리킵니다.</br></br>
[this 란?](https://hanamon.kr/javascript-this%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C/)

</br>

### 2. React의 라이프 사이클에 대해 설명해주세요.
리액트에서 클래스형 컴포넌트는 생성(mounting), 업데이트(updating), 제거(unmounting)의 생명주기를 가집니다.</br></br>

컴포넌트가 생성 되는 마운팅 단계에서는 컴포넌트 생성자 메서드인 constructor, props로부터 파생된 state를 가져오는 getDerivedStateFromProps,
컴포넌트를 렌더링하는 메서드인 render, 컴포넌트의 첫번째 렌더링이 마치면 호출되는 메서드인 componentDidMount 와 같은 생명주기 메서드들이 발생합니다.</br></br>

컴포넌트가 업데이트되는 시점인 업데이팅 단계에서는 컴포넌트의 props나 state가 바뀌었을때 호출되는 getDerivedStateFromProps,
컴포넌트가 리렌더링 할지 말지를 결정하는 메서드인 shouldComponentUpdate, 컴포넌트가 업데이트 되고 난 후 발생하는 componentDidUpdate 와 같은 생명주기 메서드들이 호출됩니다.</br></br>

컴포넌트가 화면에서 사라지는 것을 의미하는 언마운팅 단계와 관련된 생명주기 메서드로는 컴포넌트가 화면에서 사라지기 직전에 호출되는 componentWillUnmount가 있습니다.</br></br>

리액트에서 함수형 컴포넌트는 Hook을 사용해 생명주기 기능을 구현합니다. Hook은 class 안에서는 동작하지 않고, class없이 리액트를 사용할 수 있게 합니다.
Hook에서 useEffet()가 위의 클래스형 컴포넌트에서 사용된 생명주기 함수들을 대체합니다. useEffect는 함수를 반환할 수 있습니다. 이를 clean-up 이라고 표현합니다.
clean-up 함수를통해 ComponentWillUnmonut 기능을 구현할 수 있습니다.</br></br>

[react 라이프 사이클](https://velog.io/@minbr0ther/React.js-%EB%A6%AC%EC%95%A1%ED%8A%B8-%EB%9D%BC%EC%9D%B4%ED%94%84%EC%82%AC%EC%9D%B4%ED%81%B4life-cycle-%EC%88%9C%EC%84%9C-%EC%97%AD%ED%95%A0)</br>
[useEffect와 hook 생명주기](https://killu.tistory.com/44)

</br>

### 3. 이벤트 전파(버블링, 캡처링)에 대해 설명해주세요

자바스크립트의 이벤트는 전파되는 특성을 가지고 있으며, 전파되는 방식으로는 Bubbling과 Capturing이 있습니다.
bubbling은 특정 요소에서 event가 발생했을 때 상위 요소로 event가 전파되는 것을 의미하며,
capturing은 특정 요소에서 event가 발생했을 때 bubbling과 반대로 하위 요소로 event가 전파되는 것을 의미합니다.
addEventListener()의 capture 옵션이 false일 경우 bubbling, true일 경우 capturing을 확인 할 수 있습니다.
stopPropagation()은 이벤트 전파를 중단시키는 메서드로 bubbling 이나 capturing을 막아야하는 경우 사용합니다.</br></br>

[JavaScript 이벤트 전파와 중단하기](https://freestrokes.tistory.com/134)

