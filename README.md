## 튜토리얼 - 투두 리스트  
플럭스 아키텍처를 예제코드르 설명하기 위해 고전의 투두 MVC 어플리케이션을 만들어보자.
기동 가능한 전체 어플리케이션 코드는 리액트 깃 허브 저장소 내에 flux-todomvc 예제
디렉토리 내에 있지만 각각의 스텝을 개발하며 진행하자.  
  
시작하기 위해, 우리는 어떤 보일러플레이트와 모듈시스템과 기동하는 것이 필요하다. 
CommonJS 기반의 노드의 모듈 시스템은 아주 잘 들어맞으며 우리는 동작하는 리액트 보일러
플레이트를 빠르게 빌드 할 수 있다. 당신이 npm 이 설치 되었다는 가정하에 간단하게 
깃 허브에서 리액트 보일러 플레이트를 복제하고, 결과로서 나온 디렉토리를 터미널
(또는 당신이 선호하는 CLI 중 어떤것이라도) 상에서 네비게이트 해라. 그런 다음 브라우져
파이로 지속적으로 빌드 하기 위해 npm 스크립트 (npm install, then npm run build
, and lastly npm start)를 실행해라.  
  
The TodoMVC example has all this built into it as well, but if you're 
starting with react-boilerplate make sure you edit your package.json 
file to match the file structure and dependencies described in the
 TodoMVC example's package.json, or else your code won't match up with
  the explanations below.
  
## 소스코드 구조
index.html 파일이 결과로 bundle.js을 로드하는 entry point로 사용되지만, 대부분
의 우리의 코드는 js 디렉토리에 있다. Browserify로 그것을 해보자. 그리고 디렉토리
구조를 보기 위해 터미널에서 새로운 탭을 열어라. 그것은 아래와 같이 보일 것이다.
