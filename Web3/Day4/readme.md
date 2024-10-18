- SBS-Academy Web3 JavaScript 배열과 함수

                  배열(array): 같은 타입 또는 다른 타입의 여러 데이터를 한 곳에 모아둔 것
                   - 데이터를 순서대로 나열하고, 인덱스를 통해서 각 요소에 접근할 수 있음

                 [ 배열을 사용하는 이유 ]
                  1) 여러 개의 변수를 사용하지 않고도 데이터를 관리, 조작
                  2) 배열은 데이터를 효율적으로 저장하고 접근할 수 있음 
                  3) 다양한 method(함수)를 통해서 데이터를 쉽게 조작

                 [ 배열의 특징 ]
                  1) 동적인 크기: 크기가 고정되어 있지 않고, 필요에 따라 커질 수도 작아질 수 있음
                  2) 다양한 타입 허용: 숫자, 문자열, 객체 등 다양한 타입 요소를 함께 저장
                  3) 배열의 메소드(함수같은 놈들): 다양한 내장 메소드를 제공하여 데이터를 쉽게 조작 가능

                    index는 0부터 시작, 배열의 요소에 접근할 때
                     const array1 = [];
                     const array2 = [0, 2, 4]; // 배열 안 요소들이라고함
                     const array3 = ['bear', 'fox', 'monkey']; // console.log(array3[3]); => 3번째 인덱스 요소가 없기 때문에 undefined라고 뜸
                     const array4 = [1, 'fox', true];
                     const array5 = [['fox', 1, 3], [1, true, 'monkey']];

                     console.log(array2[0]);

                     배열의 길이 -> 배열명.length 

                     [ 배열 요소 추가하기 ]
                     const array6 = ['apple', 'banana', 'cocoa'];

                     array6.unshift('apricot'); //배열의 첫 위치에 요소를 추가
                     array6.push('durian'); //배열의 마지막 위치에 요소를 추가
                     console.log(array6);

                     [ 배열 요소 삭제하기 ]
                     array6.shift(); //배열의 첫 위치의 요소를 삭제
                     array6.pop(); //배열의 마지막 위치의 요소를 삭제
                     console.log(array6);

                     [ 배열 요소 자르기 ]
                     slice(시작인덱스, 끝 인덱스);

                     < 시작 >
                     0을 시작으로 하는 시작점에 대한 인덱스를 의미
                     배열의 길이보다 큰 경우 빈 배열로 반환

                     < 끝 >
                     추출을 종료할 기준 인덱스
                     slice()는 종료인덱스를 제외하고 추출
                     end값이 생략되거나, 배열의 길이보다 크면 배열의 길이만큼 추출

                     const arr = ['a', 'b', 'c', 'd'];

                     const arr1 = arr.slice(1, 3); //=> [ 'b', 'c' ]
                     const arr2 = arr.slice(1); //=> ['b', 'c', 'd']
                     const arr3 = arr.slice(-3, -1); //=> ['b', 'c'] 

                     document.write(arr1 + '<br>'); 
                     document.write(arr2 + '<br>');
                     document.write(arr3 + '<br>');


                     [ 배열 결합하기 ]
                     const animals = ['ant', 'bison', 'camel', 'duck', 'elephant'];
                     const animal = ['fox', 'gazel'];

                     ( 배열+배열 )
                     const result = animals.concat(animal);
                     console.log(result);
