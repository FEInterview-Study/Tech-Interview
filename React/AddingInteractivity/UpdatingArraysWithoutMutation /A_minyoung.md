## UpdatingArraysWithoutMutation

1. react에서 array의 불변성을 유지하면서 state를 변화시키는 방법은?

   > array를 깊은복사를 통해 복사하여 원본값은 유지시키며 복사된 값의 state를 변화시키는 방법이 있습니다.

2. map vs foreach / filter vs find

   > map은 배열을 순회한 후 배열로 반환하고, foreach는 순회만 하며 배열을 반환하지 않습니다.
   > filter는 조건에 맞는 값을 찾은 후 배열로 반환하고, find는 조건에 맞는 값만 찾으며 배열을 반환하지 않습니다.

3. slice 와 splice 차이는?
   > slice는 배열을 얕은복사 해주거나 원하는 인덱스까지 자른 배열을 반환합니다. 반면 splice는 원하는 인덱스부터 지정한 수만큼을 배열로 리턴합니다.
