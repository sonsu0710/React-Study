## Why React?
1. 일반적인 JS파일을 통해 HTML을 수정시켜주더라도, 화면을 새로 렌더링 시켜주어야 해당 데이터의 변경 여부를 알 수 있음
2. 리액트에서는 매번 단방향 바인딩 방식을 통해 특정 state가 변경되면, 해당 변경을 감지하여 수정을 바로 반영해준다. 
3. 즉, 데이터의 즉각적인 렌더링을 통해 유저의 편의성을 강화하는게 목표

## React Version
1. 리액트는 현재 18버전까지 업데이트 되어 있음.
2. 하지만 실무에서는 17버전으로 사용하는 경우가 많으니 17버전에 대한 사용법을 알아두는게 좋음
3. 18버전을 사용해도 17버전에서 작동하고, 17버전을 사용해도 18버전에서 작동함. 하지만 하위 버전에서 상위버전의 새로운 기능을 사용하지는 못함.

---

```js
ReactDOM.render(React.createElement(LikeButton), document.querySelector('#root')); // React 17버전 코드
ReactDOM.createRoot(document.querySelector('#root')).render(<LikeButton/>); // React 18버전 코드
```

## JSX
1. JSX는 리액트만의 독특한 HTML 템플릿이다
2. HTML에서 script 태그를 통해 사용하는것보다 가독성 향상이 가능하다. 
3. babel을 통해서 코드를 트랜스컴파일링하여 작동가능하게 변환한다. 
4. HTML에서 JSX를 사용하려면 babel 라이브러리를 받은 후 해당 스크립트 태그에 `type=text/babel`을 삽입한다.
5. 렌더링하는 부분과 로직을 짜는 부분 모두 type 설정을 해 주어야 한다. 

## React의 구조
1. 원래 React는 Class Component 형태로 사용하였지만 현재는 Function Component 형태로 사용한다. 
2. React Component에서 로직을 짜고, return을 통해 HTML 코드를 작성하여 템플릿을 생성한다. 
3. 만들어진 Component는 ReactDOM을 통해 렌더링한다. 

## Class Component의 단점
1. this 바인딩이 불편하다. => Function Component에서는 화살표 함수로 this 바인딩이 가능. (사실 this 쓸 일이 없긴 함)