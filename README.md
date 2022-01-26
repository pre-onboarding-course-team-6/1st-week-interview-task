# 경험을 정리하는 팀과제 (면접준비)

## 원본 : [Notion 🔗🔗](https://minbr0ther.notion.site/f60398c803d849aaae6ff565d2fb87ba)

- **주제: CRA Project Structure**
    - CRA로 만든 프로젝트의 폴더구조는 참 다양합니다. 어떤 폴더구조로 프로젝트를 진행하셨나요? 왜 그렇게 나누었는지, 그리고 해당 구조의 장점과 단점은 무엇인가요?
    1. 정민형 : 
    
    공식적인 단어를 선택하기 위해서 아래 참조링크의 ‘[리액트 공식 문서 추천 구조](https://ko.reactjs.org/docs/faq-structure.html)'를 참조하였습니다.
    
    저는 프로젝트를 진행할때 ‘파일의 기능이나 라우트에 의한 분류’ 방법을 사용해서 파일 구조를 정하였습니다.
    
    - 장점 : 각 페이지의 기능에 맞게 라우트로 분류된 폴더를 정하고, 이렇게 했을 때의 장점은 연관성이 있는 파일 끼리 묶어두어서 다른 사람들이 봐도 직관적으로 이해하기 쉽습니다.
    - 단점 : 구조가 복잡해 질 수 록 한 컴포넌트 폴더가 가지는 파일의 수가 너무 늘어나고, 뎁스가 깊어질 수 있습니다. 따라서 규모가 작은 서비스에 적합합니다.
    - 참조링크 🔗
        1. [리액트 공식 문서 추천 구조](https://ko.reactjs.org/docs/faq-structure.html)
        2. [[React] 프로젝트 디렉토리 구조 도대체 어떻게 잡아야 되나요? - 고민하지 마세요🙃](https://xtring-dev.tistory.com/39)
        3. **[리액트 어플리케이션 구조 - 아토믹 디자인](https://ui.toast.com/weekly-pick/ko_20200213) ⭐️⭐️⭐️ ⇒ 이번 과제에 사용해보고 싶은 구조!**
        
    1. 김선명 :  
        1. 프로젝트의 아키텍쳐 구조를 정하는 목적은 개발팀이 장기적으로 생산성을 올릴 수 있게 하기 위해서입니다.
        2. 참조 
            1. 많이 사용되는 폴더구조나 개념에 대해서 설명된 링크입니다.
            2. [https://blog.openreplay.com/react-architecture-patterns-for-your-projects](https://blog.openreplay.com/react-architecture-patterns-for-your-projects)
        3. 온보딩 기간동안 View나 Model을 재활용 할 일은 없어 보이기 때문에 Controller에 신경을 쓰는게 효율적으로 생각됩니다.
        
    2. 이현명 : 사용하는 기능별로 컴포넌트 분리
    
    [출처](https://smoh.tistory.com/385)
    
    <aside>
    💡 src
    
        /components
            /App
                /index.js
                /test.js
           /List
               /index.js
               /test.js
    
    </aside>
    
    1. 민무길 :
        
        View 와 Controller는 분리되어야 한다고 생각합니다. View는 Components폴더에, Controller는 Containers폴더로 분류하는것이 적당하다고 생각합니다.
        
        <aside>
        💡 src
        
              App.js
        
              /Containers
        
              /CalculatorContainer.js
        
        /Components
        
              /CaculatorComponents.js
        
        /utils
        
              /api.js
        
        ...
        
        </aside>
        

- **주제: CSS 작성 방법**
    - React에서 많이 사용하는 CSS 작성 방법은 Styled Component, SASS, CSS Modules 등이 있습니다. 어떤 방식을 선택하셨나요? 선택한 방법의 편리한 점은 무엇이었나요?
    1. 정민형 : 
        1. Styled Component : 
            1. CSS의 컴포넌트화로 스타일시트의 파일을 유지보수 할 필요가 없다. CSS 모델을 문서 레벨이 아닌 컴포넌트 레벨로 추상화한다. (모듈성)
            2. JavaScript와 CSS 사이의 상수와 함수를 쉽게 공유 할 수 있다. 예를 들어, React에서는 props를 활용한 조건부 스타일링이 가능하다.
            3. 현재 사용중인 스타일만 DOM에 포함한다. 컴포넌트 간 CSS 충돌이 없다.
            
        2. Tailwind CSS : 
            1. 랩핑 태그의 클래스명을 사용할 일이 거의 없으므로 **`container`, `wrapper`, `inner-wrapper`와 같은 클래스명을 고민하지 않아도 된다.**
            2. 모든 곳에서 동일한 색상이나 사이즈, 간격 등의 유틸리티 클래스를 사용하므로 일관된 스타일로 구현하기가 수월하다.
            3. emotion이나 styled-components 와 같은 CSS-in-JS 라이브러리와 함께 사용할 수 있다.
        
        - 참조링크 🔗
            1. [https://velog.io/@ken1204/styled-components-선정의-이유](https://velog.io/@ken1204/styled-components-%EC%84%A0%EC%A0%95%EC%9D%98-%EC%9D%B4%EC%9C%A0)
            2. **[Hello Tailwind CSS! | 장점, 단점, 사용법](https://wonny.space/writing/dev/hello-tailwind-css)**
            3. [https://velog.io/@goodenough/Tailwind-CSS-장점-단점](https://velog.io/@goodenough/Tailwind-CSS-%EC%9E%A5%EC%A0%90-%EB%8B%A8%EC%A0%90)
            
    2. 김선명 : 
        1. Git 별 개수로 판단해보았습니다.
            1. SC 35k sass 13k cssmodules 15k tailwindcss 52k
            2. tailwind 는 예시에도 없고 저는 써봤기때문에 styled component를 선택했습니다.
        2. 장점
            1. css 파일을 밖에 두지 않고, 컴포넌트 내부에 넣기 때문에, css가 전역으로 중첩되지 않도록 만들어주는 장점이 있습니다.
    3. 이현명 : 
    
    ![Untitled](%E1%84%80%E1%85%A7%E1%86%BC%E1%84%92%E1%85%A5%E1%86%B7%E1%84%8B%E1%85%B3%E1%86%AF%20%E1%84%8C%E1%85%A5%E1%86%BC%E1%84%85%E1%85%B5%E1%84%92%E1%85%A1%E1%84%82%E1%85%B3%E1%86%AB%20%E1%84%90%E1%85%B5%E1%86%B7%E1%84%80%E1%85%AA%E1%84%8C%E1%85%A6%20(%E1%84%86%E1%85%A7%E1%86%AB%E1%84%8C%E1%85%A5%E1%86%B8%E1%84%8C%E1%85%AE%E1%86%AB%E1%84%87%E1%85%B5)%20057e269af04e45ce96302e245477afbe/Untitled.png)
    
    1. 민무길 :
        1. Styled-Compoent
            - 창의적인 Class명을 지을 필요가 없다
        2. Tailwind
            - tag조차 sementic 해야할 필요가 없다
            - [https://velog.io/@teo/adorable-css](https://velog.io/@teo/adorable-css)
    
- **주제: Commit Message**
    - 팀별로 Commit Message 템플릿 정하셨나요? 어떻게 정하셨는지, 왜 그렇게 하셨는지 알려주세요.
    1. 정민형 :
        1. 교육자료에서 제공해주신 '**Udacity Git Commit Message Style Guide’를 사용해보는 게 어떨까 합니다.**
        2. 특히 커밋메세지를 영어로 작성하기 보다는 네이버, 토스와 같이 타입(feat, fix, docs, ...)를 제외한 나머지를 한글로 작성해서 가독성을 높이면 좋을 것 같다는 생각을 했습니다.
        
    2. 김선명 :
        1. Udacity style 을 추천합니다.
            1. 원래 쓰던건데 아직 이것도 못외움
            
    3.  이현명 : 
        
        commit message
        
        1. 제목과 본문을 한 줄 띄워 분리하기
        2. 제목은 영문 기준 50자 이내로
        3. 제목 첫글자를 대문자로
        4. 제목 끝에 . 금지
        5. 제목은 명령조로
        6. 본문은 영문 기준 72자마다 줄 바꾸기
        7. 본문은 어떻게보다 무엇을, 왜에 맞춰 작성하기
        
        [커밋메세지](https://velog.io/@hyeong412/TIL-%EC%A2%8B%EC%9D%80-%EC%BB%A4%EB%B0%8B-%EB%A9%94%EC%84%B8%EC%A7%80-%EC%9E%91%EC%84%B1%ED%95%98%EA%B8%B0-)
        
    
    ```jsx
    ```jsx
    # <타입> : <제목> 형식으로 작성하며 제목은 최대 50글자 정도로만 입력
    # 제목을 아랫줄에 작성, 제목 끝에 마침표 금지, 무엇을 했는지 명확하게 작성
    
    ################
    # 본문(추가 설명)을 아랫줄에 작성
    
    ################
    # 꼬릿말(footer)을 아랫줄에 작성 (관련된 이슈 번호 등 추가)
    
    ################
    # feature : 새로운 기능 추가
    # fix : 버그 수정
    # docs : 문서 수정
    # test : 테스트 코드 추가
    # refactor : 코드 리팩토링
    # style : 코드 의미에 영향을 주지 않는 변경사항
    # chore : 빌드 부분 혹은 패키지 매니저 수정사항
    ################
    ```
    ```
    
    1. 민무길 :
        
        Udacity Style을 한글로 작성하는것을 추천합니다
        
        commit 타입은 대괄호 [fix]를 사용하는게 더 가독성이 좋아보입니다
        
        예) [add] 환율 정보 갱신 api 작성
