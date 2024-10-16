# React Day2
                1. 컴포넌트란?
                 - 리액트 화면을 이루는 단위
                
                < 종류 >
                 1) 함수 컴포넌트
                    ex) function App() {
                            return(
                                <div>
                                    <h2>Hello</h2>
                                </div>
                            );
                        }

                 2) 클래스 컴포넌트
                    ex) class Welcome extends React.Component {
                            render() {
                                return () {
                                    <div>
                                        <h1></h1>
                                    </div>
                                };
                            }
                        }

                 [ 컴포넌트 이름을 지을 때 ]
                    - 대문자로 무조건 시작해야함***
                      : 리액트의 경우 소문자로 시작하는 컴포넌트는 html 태그(DOM 태그)로 인식하기 때문
                
                 ** 리액트는 사용자 정의 태그를 만드는 것
                 사용자 정의 태그 = 컴포넌트 **

