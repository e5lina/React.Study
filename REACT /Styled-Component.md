# 스타일 컴포넌트 ( Styled-Components )

***React***에는 여러 방법을 통해 ***CSS***를 적용할 수 있다. 그 중 Styled Components는 터미널 명령어를 통해 관리되는 패키지이기 때문에, 간단한 명령어를 통해 설치할 수 있다.

```bash
$ npm i styled-components
```

- ***Styled Components***를 사용하기 위해서는 가장 먼저, 아까 설치한 `styled-components` 패키지에서 `styled`를 import 해야 한다.

```tsx
import styled from "styled-components";
```

- ***html*** 의 모든 태그들에 스타일을 적용할 수 있다. 적용 방법은 `styled.태그명` 을 작성한 후 백틱으로 감싸서 사용하고 싶은 ***css*** 태그를 사용하면 된다.

```tsx
import styled from "styled-components";

const Head1 = styled.header`
	width : 100%;
	height : 150px;
	margin : 0 auto;
	display : flex;
	justify-content : center;
`;

const Cont1 = styled.article`
  width: 400px;
  height: 400px;
	border: 1px solid red;
	background-color: red;
`;

const Cont2 = styled.article`
  width: 400px;
  height: 400px;
	border: 1px solid blue;
	background-color: blue
`;

const App = () => {
  return (
	<Wrapper>
    <Header />
		<Cont1 />
		<Cont2 />
	</Wrapper>
  );
};
```

- **이미지 파일 불러오기**
    - ***src*** 폴더에 폴더 생성
    - 원하는 이미지 생성한 폴더에 넣기
    - ***import***로 원하는 이미지 불러오기 `import Logo from "../ImgFile/이미지명.파일형식(jpeg,jpg등등..)";`
    - i**mg src**로 연결시키기 `<img src={Logo} alt="logo"/>`

- ***background-image* 적용하기**
    
    ```tsx
    import bgImg from "../ImgFile/bgImg.jpeg";
    
    const Lock = styled.div`
    	background-image: url(${BgImg});
    `
    ```
    

- ***img* 적용하기**
    
    ```tsx
    import srcImg from "../ImgFile/srcImg.jpeg";
    
    const Lock = styled.img.attrs({
      src: `${srcImg}`,
    })`
    `;
    
    // ***attrs***는 말 그대로 attributes를 삽입하기 위한 메서드이며 1개의 객체타입의 arg를 받는다
    ```
    

- **선택자**
    - ***Styled-Component*** 사용중 내부에 ***&***를 선택자로 사용할 수 있다.
    - `&`는 자기 자신을 참조
    - `& > div` 는 참조한 자신의 자식 선택자
    - `& div` 는 참조한 자신의 후손 선택자

- 위 방법이 기본적인 ***Styled-Component***의 사용법이지만, ***Styled-Component***의 사용법은 무궁무진하기 때문에 추후 지속적으로 추가할 예정
