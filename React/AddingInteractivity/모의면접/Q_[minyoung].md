Q\_질문

-   State란 무엇인가요?
-   props에 대해 설명해주세요
-   props와 state를 비교해서 설명해 주세요
-   왜 리액트의 훅은 컴포넌트의 최상단에서 불러야하나요?
-   React가 JSX를 사용하는 이유는? 필수인가요?
-   props를 다룰 때 순수 함수처럼 동작해야한다는게 무슨 의미 일까요?
-   Nested object 내부의 state를 변경시키려면 어떻게 해야하나요?
-   깊은복사 vs 얕은복사에 대해 설명해주세요
-   함수 컴포넌트와 클래스 컴포넌트간의 차이점에 대해 설명해 보세요
-   strict mode 가 무엇인가요, 왜 사용하나요?
-   setState 이후 setTimeout을 바로 실행하면, 변경된 state값이 setTimeout에 적용이될까요?

A\_답변

-   리액트에서 상태를 저장, 상태 변화 리렌더 유발 state리렌더 트리거
-   상위 → 하위컴포넌트로 전달해줄 수 있음 , 변경 X , 변경할수잇지만 리렌더링 반영 X
-   리액트에서 데이터, state → 리렌더링해서 변경하고싶을 때 , props → 하위컴포넌트로 데이터로 전달
-   훅의 규칙 , 조건문이나 루프문안에서 훅이 불려졌을대는 훅이 배열로 관리 , 만약 조건문이면 조건에 해당 X → 훅이 제대로 동작하지 X
-   필수 X, 자스의 확장문법, 자스에서 html을 가시적으로 표현하기 위해 사용, 하나의 컴포넌트 안에서 html, js 동시에 사용가능
-   input, output값이 동일, props값이 변경될수없다, 변경되지 않기 때문에 전달된 컴포넌트로 렌더링되어야한다.
-   오브젝트의 state값을 변경하자면, 동일한 배열을 복사(스프레드 연산자) , 복사한 값의 오브젝트를 변경해야함, 깊어질수록 스프레드 연산자 사용
-   깊은복사 - 값자체를 복사, 원본값에 영향 X, 얕복 - 참조, 원본값에 영향O , 배열과 같은 값을 스프레드 연산자로 복사할 경우
-   구현방법의 차이, 어떤것이 더 좋다X , 차이점은 공부
-   리액트에서 개발모드같은 경우 두번 함수를 실행, 순수함수인지 판단, 두번째 함수를 실행했을 때 값이 변하는지를 보고 안변한다면 순수함수로 잘 작성, 변한다면 순수X 개발자에게 코드를 좀더 쉽게 구현해주는
-   아뇨, state의 상태가 스냅샷처럼 촬영, setState에서 변경된 값은 다음 렌더에 , 이전 값으로 setTimeout 에 적용
