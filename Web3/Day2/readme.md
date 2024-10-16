- SBS-Academy Day2 - Java Script 여러 연산자 및 조건문

                [ 연산자 ]
                 - 하나 이상의 표현식을 대상으로 연산을 수행하여 하나의 값을 만드는 것
  
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

==================================================================================

                [ 조건문 ]
                 -주어진 조건에 따라 실행하는 조건문
                
                 1) if문
                   [ 조건이 참 거짓 2개일 때 ]
                   문법식 => if(조건) {
                              조건이 참일 때 실행될 코드
                          } else {
                              조건이 거짓말일 때 실행될 코드
                          };

                   [ 조건이 3개 이상일 때 ]
                   문법식 => if(조건) {
                              조건이 참일 때 실행될 코드
                          } else if(조건) {
                              실행될 코드2
                          } else if(조건) {
                              
                          } else {
                                                      <= 위에 조건들이 다 만족하지않았을 때 실행되는 코드 작성
                          };

                   let a = 25;
                   let b = 40;
                 
                   if(a > b){
                      console.log('true');
                   } else {
                      console.log('false');
                   }

                   ( if문 예시 )
                   let adult = 20;
                   let age = prompt('나이를 입력하세요');

                   if(age <= 19){
                       console.log('미성년자입니다.');
                   } 
                   else {
                       console.log('성인입니다.');
                   }
                
                   let result = adult < age ? '성인입니다' : '미성년자입니다'
                   20보다 나이가 많냐?            true    :     false
                   개발자들은 한줄이라도 줄이는게 엄청 큰 일 이기 때문에 삼항 연산자를 이용해 if문을 간단하게 정리할 수 있다.

                   document.write(result);


                 2) switch문
                  - 주어진 케이스 조건에 따라 실행하는 조건문

                   switch(조건) {
                      case 조건값: 조건이 참일 때 실행문;
                          break;
                      case 조건값: 조건이 참일 때 실행문;
                          break;

                          ...

                      default: 일치하는 조건이 없을 때 실행문
                      } 

                   let subject = prompt('과목을 선택하세요. 1 - 웹, 2 - 편집, 3 - 드로잉');

                   switch(subject){
                   case '1': document.write('웹 과목');
                      break;
                   case '2': document.write('편집 과목');
                      break;
                   case '3': document.write('드로잉 과목');
                      break;
                   default: alert('해당 과목은 없습니다');
                   }  
