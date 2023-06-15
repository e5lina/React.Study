# useState

- 컴포넌트에서 동적인 값을 상태(***state***)라고 부릅니다. `useState` 라는 함수를 사용하면 컴포넌트에서 상태를 관리 할 수 있습니다.
- ***useState***()는 **상태의 초기값을 인수**로 전달 받아 호출됩니다. 이때의 **반환값은 상태를 나타내는 배열**로, 배열의 **첫 번째 요소는 현재 상태 값**, **두 번째 요소는 상태 값을 갱신해주는 Setter 함수** 입니다. 즉 초기에는 상태값이 초기값으로 들어가 있고, 이 상태값을 바꾸고 싶다면 상태 함수(새롭게 바뀔 값)를 이용해서 변경할 수 있습니다.
    
    ```jsx
    import { useState } from 'react';
    
    const [상태 값 저장 변수, 상태 값 갱신 함수] = useState(상태 초기 값);
    
    // 또는
    
    const 상태 = useState(상태 초기 값);
    const 상태값 = 상태[0];
    const 갱신함수 = 상태[1];
    ```
    
- useState()를 설명할때 가장 많이 사용되는 예제인 Counter를 예제로 들게되면

```jsx
import React, { useState } from 'react';

function Counter() {
  const [number, setNumber] = useState(0);
// 첫번째 원소는 현재상태 두번째 원소는 Setter 함수
// useState 를 사용 할 때에는 상태의 기본값을 파라미터로 넣어서 호출해줍니다
  const onIncrease = () => {
    setNumber(number + 1);
  }

  const onDecrease = () => {
    setNumber(number - 1);
  }

  return (
    <div>
      <h1>{number}</h1>
      <button onClick={onIncrease}>+1</button>
      <button onClick={onDecrease}>-1</button>
    </div>
  );
}

export default Counter;
```

- 다음과 같은 코드를 작성하게 되면 useState를 사용한 누르는 버튼( - , + ) 에 맞춰 숫자가 1씩 변하게 되는 Counter예제를 완성할 수 있다!
