# 렌더링 ( Rendering )

- **조건부 렌더링**
    
    React에서는 원하는 동작을 캡슐화하는 컴포넌트를 만들 수 있습니다. 이렇게 하면 애플리케이션의 상태에 따라서 컴포넌트 중 몇 개만을 렌더링할 수 있습니다.
    
    React에서 조건부 렌더링은 JavaScript에서의 조건 처리와 같이 동작합니다. `[if](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Statements/if...else)` 나 `[조건부 연산자](https://developer.mozilla.org/ko/docs/Web/JavaScript/Reference/Operators/Conditional_Operator)` 와 같은 JavaScript 연산자를 현재 상태를 나타내는 엘리먼트를 만드는 데에 사용하세요. 그러면 React는 현재 상태에 맞게 UI를 업데이트할 것입니다.
    
- **배열 렌더링**
    
    보통 리액트를 통해 배열을 렌더링하면 기본적으로는 컴포넌트에 'users[0]' 이런식으로 해서 직접 넣어줘서 코드를 작성할 것이다. 하지만 이렇게 한다면 계속 JSX를 작성해야하기 때문에 굉장히 불편하고 번거로울 것이다.
    
    따라서 배열 컴포넌트 외에 렌더링에 필요한 컴포넌트를 하나 더 생성한다. 그리고 동적인 데이터 처리를 위해 자바스크립트의 내장함수 `map()`을 사용하여 동적인 배열을 렌더링해준다. 마지막으로 배열을 렌더링 할 때는 `key`라는 `props`를 설정해야한다. `key`는 배열의 각 원소들이 가지고 있는 고유값으로 설정해줘야한다. `key`가 있어야만 배열이 업데이트 될 때 효율적으로 렌더링 될 수 있기 때문이다.
