# SBS-Academy React

            1. 리액트란?
             -> 페이스북 엔지니어 조던 발케가 개발
             -> 페이스북(메타)에서 개발한 오픈소스 라이브러리
             -> 프론트엔드 개발자 사이에서 인기가 많다! => 깃허브 star 수와 npm 패키지 다운로드 수가 리액트가 가장 많음
             -> 페이스북 내부에서 2011년에 뉴스 피드를 만들 때 처음으로 사용!
             -> 대중적으로 공개가 된 시점은 2013년 7월! (나온지 11년?)

            1-1. 리액트에 관해서
             -> 오픈소스 라이브러리니까 돈이 안들고 이미 만들어진 자바 스크립트와 사용 할 수 있다.
             -> 새로운 ui 컴포먼트를 개발하기 위해 사용 웹과 앱을 개발하는데 사용. 
             -> 점점 리액트 사용이 많아지면서 리액트와 자바스크립트 둘 다 사용할 수 있는 사람을 회사에서 많이 구함
             -> 자바스크립트 다음으로 리액트가 중요 = 그래서 자바스크립트를 알아야 리액트 사용가능

            라이브러리 ? vs 프레임워크 ?
             1) 라이브러리: 기능만 가져다 쓰는 것
             2) 프레임워크: 제공되는 틀안에서 우리가 주어진 규칙을 지켜가면서 사용하는 것

            3. 리액트를 사용하는 이유
             1) 사용자의 인터페이스(UI = User Interface)를 만들기 위해 사용
             2) SPA(Single Page Application) - HTML파일을 1개만 사용, 다른 페이지를 보여주고싶을 때 HTML 부분만 싹 갈아치워서 보여줌 
                                               (HTML이 로딩으로 페이지가 바뀌는게 아니라 필요한 부분만 바뀜(?))
        
            4. 장단점 (단점에 비해 장점이 너무 커서 리액트 사용량이 많아짐)
             1) 장점:
                - html 재사용이 편리
                - 컴포넌트 단위로 개발하기 때문에 여러 개발자들이 분업하기 좋음
                - 리액트 네이티브를 사용하면 웹 뿐만아니라 모바일 앱도 개발이 가능
                - 프론트엔드 백엔드 완전히 분리를 한 상태에서 각각 개발이 가능

             2) 단점:
                - js 파일이 너무 많아서 웹페이즈 크기(용량)가 커짐
                - 간단한 사이트도 코드가 쓸데없이 많아질 수 있고 복잡해짐

            5. 기본적인 문법
             1) JSX문법 => JS(Java Script + xml) 확장문법을 사용
                -> 하나의 파일에 js, html 같이 작성함
            
            - 사용 규칙
             1) 여러 요소(tag)가 있다면 꼭 부모요소를 만들어서 감싸주어야함 안싸줄시 -> error
             
             function App() {
                return (
                    <div>, <> -> <> </>와 같이 해줘두됨
                        <h2>Hello</h2>
                        <h2>I'm React</h2> -> 한개면 상관 X
                    </div>, </>
                );
             }

             2) 표현식 사용 가능! -> 단, 표현식 내부안에선 조건문, 반복문은 사용 불가능

             function App() {

                const name = 'React';

                return (
                    <div>
                        <h2>Hello</h2>
                        <h2>I'm {name}</h2>
                    </div>
                );
             } 

             3) 리액트에서는 class = className으로 사용된다.
             
             function App() {

                const name = 'React';

                return (
                    <div>
                        <h2>Hello</h2>
                        <h2>I'm {name}</h2>
                    </div>
                );
             } 

             4) 모든 태그는 여는 태그와 닫는 태그로 반드시 존재!

             function App() {

                const name = 'React';

                return (
                    <div>
                        <h2>Hello</h2>
                        <h2>I'm {name}</h2>
                        <input></input>
                        <br></br> -> 이런식으로 HTML에서 닫는태그가 없는 태그들도 닫는태그를 만들어줘야함.
                    </div>
                );
             } 

             5) style을 적용할 때 객체 형태로 삽입

             function App() {

                const name = 'React';

                return (
                    <div>
                        <h2>Hello</h2>
                        <h2 style={{backgroundColor: 'black', color: 'white';}}>I'm {name}</h2> 
                            -> style=""; 이 아니라 style={{}}이다.
                    </div>
                    <input></input>
                );
             } 

            --------------------------------------------------
             
             function App() {

                const name = 'React';
                const style = {
                    backgroundColor: 'black',                       <-----------
                    color: 'white',
                }

                return (
                    <div>
                        <h2>Hello</h2>
                        <h2 style={style}>I'm {name}</h2>        <-----------
                    </div>
                    <input></input>
                );
             }

