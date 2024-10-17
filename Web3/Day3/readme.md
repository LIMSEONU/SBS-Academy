- SBS-Academy Web3 JavaScript 반복문


                반목문: 일정한 규칙으로 조건이 만족할 때까지 실행하는 반복문
  
                 - 시작값 => 초기화 해줄 코드
                 - 끝값 => 조건식
                 - 일정한 규칙반복 => 증감식(4번째)

                 for(초기화값; 조건식; 증감식) {
                 조건이 만족할때까지 반복되는 실행문
                 }

                       (1)        (2)   (4)
                 for (let i = 0; i < 5; i++){
                    // code (3)
                 } 
                    (1) > (2) > (3) > (4) > (1) > (2) ...
                     - 계속 반복하며 조건이 만족할 때까지 실행한다
                     

                 < 기초 반복문 응용 문제 >
                 for (let i = 0; i < 10; i++) {
                    document.write(i);
                    // 0부터 9까지 출력하기
                 }
                 for (let i = 1; i <= 10; i++) {
                 document.write(i);
                    // 1부터 10까지 출력하기
                 }


                 < 기초 반복문 짝수만 찾아내는 방법 >
                 for (let i = 1; i <= 10; i++) {
                 if(i % 2 === 0){
                     document.write(i + '<br/>');
                  }
                 }

                 - if문에 === <= 넣은이유가 넘버와 데이터타입까지 같아야 되기 때문

                
                 < 기초 반복문 홀수만 찾아내는 방법 > 
                  for (let i = 1; i <= 10; i++) {
                 if(i % 2 === 1) {
                    document.write(i + '<br/>');
                  }
                 }


                 < 중첩 for문 예시 >
                 for(let i = 1; i <= 5; i++) {
                    document.write('<h1>' + i + '</h1>') //부모 i를 1~5까지 1씩 증가하면서 출력
                    for(let j = 6; j <= 8; j++){ 
                        document.write(j + '<br/>'); //자녀 j를 6~8까지 1씩 증가하면서 출력
                  }
                 }
                 < for문을 이용한 삼각형 만들기 예제 >
                 for(let i = 0; i < 5; i++){
                    document.write('<br/>');
                    for(let j = 0; j <= i; j++){
                        document.write('*');
                  }
                 }

                 < for문을 이용한 사각형 만들기 예제 >
                 for(let i = 0; i < 5; i++){
                    document.write('<br/>');
                    for(let j = 0; j < 5; j++){
                        document.write('*');
                  }
                 }
                 < for문을 이용한 구구단 만들기 >
                 for(let i = 2; i <= 9; i++){
                    document.write(i + '단');
                    document.write('<br/>');
                 for(let j = 2; j <= 9; j++){
                    document.write(i + ' * ' + j + ' = ' + (i*j));
                    document.write('<br/>');
                  }
                 }
