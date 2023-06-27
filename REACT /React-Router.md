# React Router

- **SPA**
    
    Single Page Application (싱글 페이지 어플리케이션)는, 페이지가 1개인 어플리케이션이란 뜻입니다. 전통적인 웹어플리케이션의 구조는 여러 페이지로 구성되어있습니다. 유저가 요청 할 때 마다 페이지가 새로고침되고, 페이지를 로딩 할 때 마다 서버로부터 리소스를 전달받아 렌더링을 합니다. 최근엔 웹의 정보가 방대해져 속도 문제가 생겼고, 이를 해소하기 위하여 캐싱과 압축을 하여 서비스가 제공되는데요. 이는 사용자와 인터랙션이 많은 모던 웹 어플리케이션에서는 충분하지 않을 수도 있습니다. 렌더링하는것을 서버쪽에서 담당한다는것은, 그 만큼 렌더링을 위한 서버 자원이 사용되는것이고, 불필요한 트래픽도 낭비되기 때문이지요. 그래서 우리는 리액트 같은 라이브러리 혹은 프레임워크를 사용해서 정말 필요한 데이터만 전달받아 보여주게 됩니다.
    
- ***React-Router***
    
    **간단하게 설명하자면, URL 경로를 제어하여 URL 변경 및 매개변수 사용에 도움을 주며, URL 경로에 맞는 레이아웃 구성 및 컴포넌트 렌더링을 가능하게 도와줍니다**
    
    ***React-Router*를 사용하게 되면**, **새로운 페이지를 로드하지 않고 하나의 페이지 안에서 필요한 데이터만 가져오는 형태를 가지기 떄문에 불필요한 렌더링을 막을수 있다**
    
- **설치**
    
    ```jsx
    $ create-react-app react-router
    //create-react-app 으로 프로젝트를 생성
    $ npm install react-router-dom
    // npm i 를 통해 react-router-dom 설치
    ```
    
    • ***react-router-dom***: 브라우저에서 사용되는 리액트 라우터 입니다.
    
- **사용**
    
    ```jsx
    function Page {
      return (
        <div>
          <h1>페이지</h1>
        </div>
      );
    };
    export default Home;
    // 페이지 컴포넌트 생성
    
    <BrowserRouter>
    	<Routes>
    	  <Route path="/" element={<Page />}>
    		</Route>
    		<Route path="/main" element={<Main />}>
    		</Route>
    	</Routes>
    </BrowserRouter>
    // 경로 설정
    
    ```
    
- ***Link*를 통한 이동**
    - ***LINK*를 통한 페이지이동**
        
        ```tsx
        <Link to="/main">
           <MainButton type="button">링크로 이동</MainButton>
        </Link>
        ```
