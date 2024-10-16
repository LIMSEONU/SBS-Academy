#SBS-Academy Day2 - Java Script 여러 연산자
                < 산술연산자(+, -, *, /, %) >
                 - 01.html (오칙연산)

                < 복합대입연산자(+=, -=, *=, /=, %=) >

                 += : 기존 변수의 값에 값을 더함
                 -= : 기존 변수의 값에 값을 뺌
                 *= : 기존 변수의 값에 값을 곱함
                 /= : 기존 변수의 값에 값을 나눔
                 %= : 기본 변수의 값에 나머지를 구함

                 a = x ( x는 정수 )
                 a = a + x => a += x
                 a = a - x => a -= x
                 a = a * x => a *= x
                 a = a / x => a /= x
                 a = a % x => a %= x

                 let a = 20;
                 console.log(a += 5); => 25
                 console.log(a -= 5); => 20
                 console.log(a *= 5); => 100
                 console.log(a /= 5); => 20
                 console.log(a %= 5); => 0


                < 증감 연산자 >
                 - 복합대입연산자에 1씩 증가 또는 1씩 감소할 때 사용하는 연산자

                 ex) a = a + 1 => a += 1 => a++ ( 후위 증강자 ), ++a ( 전위 증강자 )
                     a = a - 1 => a -= 1 => a--, --a


                    ( y = ++x )
                    전위 증강자는 먼저 x값을 증가 시켜주고 그대로 값이 앞으로 전해짐
                    ( y = x++ )
                    후위 증강자는 먼저 x값을 y에 넘겨주고 x값이 증가됨 
                    
                    let a = 20;
                    console.log(a++); result = 20
                    console.log(++a); result = 21


                < 비교 연산자 >
                 - 비교하는 두 항의 크기를 비교하여 결과를 참, 거짓으로 표현

                 let a = 20;
                 let b = '30';

                 console.log(a < b);
                 console.log(a > b);
                 console.log(a == b); ( a와 b의 값이 같다 )
                 console.log(a != b); ( a와 b의 값이 다르다 )

                 console.log(a === b); ( 값을 먼저 비교하고, 타입값도 같은지를 비교( 문자열인지~ 숫자인지~ 확인하는법 ) )
                 console.log(a !== b);


                < 논리연산자 >
                 - 항을 비교할 때 사용

                 and(&&) => 둘 중에 하나라도 거짓이면 거짓
                 or(||) => 둘 중에 하나라도 참일 때 참
                 not(!) => 기준의 반대일 때

                 let a = 10;
                 let b = 20;
                 let c = 30;

                 console.log(a < b && a < c); => true (10<20 && 10<30 - 다 맞으니 true)
                 console.log(a > b && a < c); => false (10>20 && 10<30 - 하나라도 거짓이니 false)

                 console.log(a > b || a < c); => true (10>20 || 10<30 - 하나라도 참이니 true)

                 console.log(a != 10); => false (10인데 10이 아니라고 하니 false)
                 

                < 삼항연산자 >
                 - 조건의 결과에 따라 다른 실행 결과
                 - 피연산자 3개 필요(조건, 코드1, 코드2)
                 문법식 => 조건식 ? 참일 때 코드 : 거짓일 때 코드

                 let a = 10;
                 let b = 20;

                 let result = a < b ? 'true' : 'false';

                 console.log(result);
