### 1. Execution Context (실행 컨텍스트) 란?
실행 컨텍스트는 자바스크립트 코드가 실행되는 환경입니다. 모든 JavaScript 코드는 실행 컨텍스트 내부에서 실행된다고 생각할 수 있습니다.
즉, 함수가 실행되면 함수 실행에 해당하는 실행 컨텍스트가 생성되고, 자바스크립트 엔진에 있는 콜 스택에 차곡차곡 쌓입니다.
그리고 가장 위에 쌓여있는 컨텍스트와 관련 있는 코드를 실행하면서(LIFO), 전체 코드의 환경과 순서를 보장하게 됩니다.
실행 컨텍스트는 식별자(변수, 함수, 클래스 등의 이름)를 등록하고 관리하는 스코프와 코드 실행 순서 관리를 구현한 내부 매커니즘이라고도 할 수 있습니다.</br>
[참고링크1](https://velog.io/@edie_ko/js-execution-context)</br>
[참고링크2](https://junilhwang.github.io/TIL/Javascript/Domain/Execution-Context/#reference)</br>
[참고링크3](https://taenami.tistory.com/109)</br>

### 2. 브라우저 렌더링 과정을 설명해주세요.
브라우저가 페이지를 렌더링 하려면 파싱, 스타일, 레이아웃, 페인트, 컴포지팅 총 5 단계를 거칩니다. 우선 받아온 HTML 파일을 해석하는 파싱이 필요합니다. 
파싱 단계는 HTML 파일을 해석하여 DOM(Document Object Model) Tree를 구성하는 것으로, 파싱 중 HTML에 CSS가 포함되어 있다면 CSSOM(CSS Object Model) Tree 구성 작업도 함께 진행합니다.
스타일 단계에서는 형성 된 각각의 Tree를 결합하여 Render Tree를 만듭니다. Render Tree는 실제로 화면에 그려질 Tree를 의미하며 스타일트리라고도 합니다.
레이아웃 단계에서는 Render Tree를 기반으로 각 노드의 위치와 크기를 계산하고, 페인트 단게에서는 계산된 값을 이용해 각 노드를 화면상의 실제 픽셀로 변환하고, 레이어를 만듭니다.
마지막으로 컴포지싱 단계에서는 레이어를 합성하여 실제 화면에 나타냅니다. 
각 단계는 반드시 전 단계의 데이터가 필요하며, html의 레이아웃이 변경될 경우 레이아웃 단계에서 랜더 트리가 재생성되는데 이를 리플로우, 레이아웃과 관련없는 스타일이 변경될 경우 페인트 단계가 다시 실행됩니다. 이를 리페인트라고합니다.</br>
[참고링크-MDN](https://developer.mozilla.org/ko/docs/Web/Performance/How_browsers_work#%EB%A0%8C%EB%8D%94render) </br>
[참고링크-브라우저 렌더링 과정 이해하기](https://tecoble.techcourse.co.kr/post/2021-10-24-browser-rendering/)</br>

### 3. REST API란 무엇인가요?
REST란 HTTP를 잘 사용하기 위한 아키텍처 스타일을 의미하며, REST API란 REST한 방식으로 데이터를 상호교환 하도록 설계된 API 입니다.
[참고링크1](https://thalals.tistory.com/335) </br>
[참고링크2](https://hahahoho5915.tistory.com/54)
