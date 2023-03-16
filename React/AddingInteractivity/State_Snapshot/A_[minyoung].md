## State_Snapshot

1. setState가 리렌더를 트리거하는 방법에 대해 설명해주세요.
   > 이벤트 핸들러 함수에 setState를 설정해주고 이벤트가 발생한 후 state값이 변경될 때 리렌더를 일으킵니다.
2. 상태가 업데이트 됐을때 돔이 업데이트 되는 과정에 대해 설명해주세요.
   > 상태가 업데이트 되면 리액트의 virtual dom에서 해당 컴포넌트의 스냅샷과 이전의 virtual dom의 스냅샷을 비교한 후 변경된 부분만 실제 Dom에 업데이트 시켜줍니다.
3. setState 이후 setTimeout을 바로 실행하면, 변경된 state값이 setTimeout에 적용이될까요?
   > setState는 비동기처럼 실행이 되므로 변경된 state 값이 setTimeout에 적용되지 않고 이전의 state값이 적용됩니다.
