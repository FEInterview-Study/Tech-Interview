## State_Snapshot

1. setState가 리렌더를 트리거하는 방법에 대해 설명해주세요.
> onClick과 같은 이벤트 핸들러가 실행되었을 때 이벤트에해당하는 state를 setState를 통해 set해주며, 새로운 렌더를 큐에 등록하며, 이후 새로운 상태값에 따라 리렌더를 일으킵니다.

2. 상태가 업데이트 됐을때 돔이 업데이트 되는 과정에 대해 설명해주세요.
> React에서 상태(state)가 업데이트되면 React는 이전 상태와 새로운 상태를 비교합니다. 이전 상태와 새로운 상태가 다르다면, React는 가상 DOM(virtual DOM)을 사용하여 변경된 부분을 계산합니다. 이후, 변경된 부분에 대한 실제 DOM 업데이트를 수행합니다.

3. setState 이후 setTimeout을 바로 실행하면, 변경된 state값이 setTimeout에 적용이될까요?
> setState는 비동기로 동작합니다. 즉, setState를 호출한 이후에도 state 값이 즉시 변경되지 않고, 다음 렌더링 사이클에서 업데이트됩니다.
때문에, setState 함수 호출 직후에 setTimeout을 실행하더라도, 변경된 state 값이 setTimeout에 적용되지 않습니다.
