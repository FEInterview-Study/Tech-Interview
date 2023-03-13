## State_Snapshot

1. setState가 리렌더를 트리거하는 방법에 대해 설명해주세요.
> setState 함수는 state를 갱신할 때 사용합니다. 새 state 값을 받아 컴포넌트 리렌더링을 큐에 등록합니다. 이후에, 새로운 상태 값에 따라 리렌더를 일으킵니다.

2. 상태가 업데이트 됐을때 돔이 업데이트 되는 과정에 대해 설명해주세요.
> 리엑트가 먼저 해당 컴포넌트를 실행시키고, 이전 상태와 현재 변경된 state에 해당하는 snapshot을 비교하여 다른 부분을 계산하여 Dom tree를 업데이트 합니다.

3. setState 이후 setTimeout을 바로 실행하면, 변경된 state값이 setTimeout에 적용이될까요?
> 아니요, setState의 값이 변경되는 시점은, 다음 렌더가 될 때 값이 변경됩니다. 때문에, setState 이후 바로 setTimeout을 실행한다면, 리렌더가 되지 않은 상태에서 즉 값이 변경되지 않은 상태에서 setTimeout이 실행됨으로 이전의 state값이 적용됩니다.
