
1. SPA와 MPA에 대해 설명해주세요.
SPA(Single Page Application)는 한 개(Single)의 Page로 구성된 Application이고 MPA(Multiple Page Application)는 여러 개(Single)의 Page로 구성된 Application입니다. MPA는 새로운 페이지를 요청할 때마다 정적 리소스가 다운로드 되며 매번 전체 페이지가 다시 렌더링 됩니다.  반면 SPA는 웹 에플리케이션에 필요한 모든 정적 리소스를 최초 한 번에 다운로드하고, 이후 새로운 페이지 요청이 있을 때, 페이지 갱신에 필요한 데이터만 전달 받아서 페이지를 갱신합니다. 그래서 SPA는 주로 CSR(Client Side Rendering) 방식, MPA는 SSR(Server Side Rendering) 방식으로 렌더링한다고 말합니다.



2. CSR과 SSR에 대해 설명해주세요.
CSR은 최초에 한번 서버에서 전체 페이지를 로딩하여 보여주고 이후에는 사용자의 요청이 올 때마다, 리소스를 서버에서 제공한 후 클라이언트가 해석하고 렌더링하는 방식이며 SEO가 어렵다는 단점이 있습니다. SSR은 모든 템플릿을 서버측에서 렌더링하고 완성된 페이지 형태로 응답하며 SEO에 좋다는 장점이 있습니다




3. Hoisting이란 무엇인가요?
JavaScript에서 호이스팅은 인터프리터가 코드를 실행하기 전에 함수, 변수, 클래스 또는 임포트(import)의 선언문을 해당 범위의 맨 위로 끌어올리는 것처럼 보이는 현상을 뜻합니다. 
