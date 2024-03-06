## 자바스크립트의 this란?
> <p>this란 현재 실행중인 코드에서 사용되는 객체를 나타냅니다.this의 값은 함수를 "호출"한 방법에 의해 결정이 됩니다. 객체 안에서의 this는 자신을 가리키게 됩니다.일반 함수에서의 this는 "호출"한 방법에 의해 결정이 되므로 동적 스코프입니다. 따라서 함수 안의 일반 함수에 this 값은 window(전역)이 됩니다. 이렇게 동적으로 this 값이 결정되는데 일반 함수에서는 .bind 메소드로 호출되는 this의 값을 고정시킬 수 있습니다. 또 엄격 모드가 적용되는 경우 참조 값이 달라지는데, 엄격 모드가 적용 시 일반 함수 내부의 this는 undefinded 가 바인딩 됩니다. 화살표 함수에서의 this는 함수가 속해있는 곳의 상위 스코프의 this를 결정하게 되므로 정적 스코프입니다. 화살표 함수에서는 .bind 메소드를 사용 할 수 없어서 가리킬 this를 고정시킬 수 없습니다.</p>
</br>
<p>$\scr{\normalsize{\color{#69A65A}👇참고 \ 링크 👇}}$</p>
[자바스크립트의 this는 무엇인가?](https://www.zerocho.com/category/JavaScript/post/5b0645cc7e3e36001bf676eb)<br/>
[개발자 면접 단골질문 자바스크립트 this](https://www.youtube.com/watch?v=tDZROpAdJ9w&t=2s)</br>
[this 란?](https://hanamon.kr/javascript-this%EB%9E%80-%EB%AC%B4%EC%97%87%EC%9D%BC%EA%B9%8C/)</br>
[MDN](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/this#%ED%95%A8%EC%88%98_%EB%AC%B8%EB%A7%A5)
