## Hook

1. 리액트 훅의 규칙이 무엇인가요?
> JavaScript Functions이 아닌 React Functions에서 불려져야 하며, 훅은 최상단에서 불려와져야하고 조건문이나 반복문과 같은 내부에서 사용되면 안됩니다.

2. 리액트의 훅은 어느 위치에서 호출해야하나요?
>  훅은 항상 컴포넌트 내 최상단에서 불려와져야하고 조건문이나 반복문과 같은 내부에서 사용되면 안됩니다.

3. 왜 리액트의 훅은 컴포넌트의 최상단에서 불러야하나요?
> 리액트에서 만약 useState라는 훅을 호출하였을때, state라는 하나의 배열내에서 여러 상태를 순서에 따라서 관리하게됩니다. 만약, 조건문이나 반복문내에서 훅을 호출하게된다면, 그 조건이 false인 경우에는 훅이 실행되지않고 넘어가기에 배열의 순서가 뒤바뀔수 있게 되며, 그렇게되면 다음 렌더시 정상적으로 동작하지 않게되는 문제를 일으키게 되기 때문입니다.
