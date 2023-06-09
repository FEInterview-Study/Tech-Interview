## StateUpdate

1. State는 어떤 방식으로 업데이트 되나요?

   > State는 이벤트 핸들러가 동작하면 바로 업데이트 되는 것이 아니라 한꺼번에 업데이트가 되어도 안전할 때 업데이트 되며 이것을 배칭이라고 부릅니다. 리액트에서는 좀 더 빠르게 효율적으로 처리하기 위해 배칭을 합니다.

2. 만약 한 이벤트 내에서 state를 세번 업데이트 하고 싶을 경우 어떻게 해야 하나요?

   > 이벤트 내에 set해주는 함수를 세번 호출한 후, 각 함수의 인자 값으로 화살표함수를 적용하여 이전의 state를 인자로 넘겨주어 계산합니다.

3. 리액트에서 이벤트 핸들러 함수 내부에 set해주는 함수가 여러 개 있을 경우 어떻게 동작하나요?
   > set함수가 이전 state를 받아와 계산하는 화살표함수일 경우 이전의 state 값으로 계산하여 업데이트 시켜줍니다. 반면 set함수에 값을 넣어주게 되면 그 값으로 대체됩니다.
