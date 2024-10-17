- Day2에 대한 복습
  
            < if문으로 공부 >
  
            let x = 100;
            let y = 50;
            if (x > y) {
                console.log('true');
            } else {
                console.log('false');
            }
            

            < 삼항연산자로 공부 >

            let x = 100;
            let y = 50;

            let result = x > y ? 'true' : 'false';

            console.log(result);
            

            < switch문으로 공부 >

            let x = 100;
            let y = 50;

            switch(x > y) {
                case true:
                    console.log('true');
                    break;
                case false:
                    console.log('false');
            }
            

            < switch문 응용한 문제 1 >
  
            const fruit = prompt('put your favorite fruit');

            switch(fruit) {
                case '사과':
                    document.write('사과입니다');
                    break;
                case '귤':
                    document.write('귤입니다');
                    break;
                default:
                    // 연결연산자를 이용해 prompt에 입력된 과일 불러오기
                    // document.write(fruit  + '입니다');
                    document.write(`${fruit} 입니다`);
                    break;
            }
            
            < if문 응용한 문제 1 >
            const fruit = prompt('put your favorite fruit');

            if (fruit === '사과') {
                document.write('사과입니다.');
            } else if (fruit === '귤') {
                // === <= type과 String까지 같을 때 사용
                document.write('귤입니다.');
            } else {
                document.write(`${fruit} 입니다`);
            }

