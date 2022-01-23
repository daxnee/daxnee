
<if , eles>

if (true) {   
			System.out.println("result : true");
=> if가 true라면 값은 result : true 로 출력
		} else {
			System.out.println("result : false");
		}
=> 만약 if가 false라면 값은 result : false 로 출력

<else if>
	ex_1)
	if (false) {
		System.out.println("result : true"); // => if가 false니까 실행 안하고 다음으로 넘김
	} else if (true) {
		System.out.println("result : true");
		=> if가 true니까 실행 됨. 결과는 result : true
	} else {
		System.out.println("result : false");
	}

    **수 많은 조건문 중 가장 먼저 'true를 충족하는' 실행문 하나만 실행되고 
    if문을 나오게 됨 (뒤에 true가 있던 말던 노상관)
    ** else는 생략도 가능함
       
        *else if 는 여러번 올 수 있지만 else는 마지막에 딱 한번 나온다.

	ex_2)
	int y = 0;
	if (y == 1) {
		System.out.println("result : true"); // => if가 false니까 실행 안하고 다음으로 넘김
	} else if (y == 2) {
		System.out.println("result : true");
	} else {
		System.out.println("result : false");
	}

결과:
result : false



<스캐너>
    Scanner scan = new Scanner(System.in);//crtl + shift + o
    System.out.print("숫자를 입력하세요 ==>");
    int value = scan.nextInt();
    if(value <= 100) {
        if((value%2) == 0) {
            System.out.println("2의 배수입니다.");
        }
        if((value%3) == 0) {
            System.out.println("3의 배수입니다.");
        }
    }else{
        System.out.println("100을 넘었습니다!!");
    }

결과 실행 방법:
ctrl + f10 - 숫자 입력 - 엔터 - 결과 출력


<While 문>  ...?
      int i =0;
		int sum =0;
		final int MAX_VALUE = 55;
		while(true) {
	   System.out.println("stop");
		++i;
		sum = sum + i;
		if(sum == MAX_VALUE) {
			break;} 
		}

결과:
stop
stop
stop
stop
stop
stop
stop
stop
stop
stop



<for문 연습하기>

int sum=0;
		for(int i=1; i<=10; i++) {
			sum = sum + i;   // => == sum += i; 
			System.out.print(i);
			if(i<=9)
				System.out.print("+");
		else {
			System.out.print("=");
			System.out.print(sum);
		}
		}

답:
1+2+3+4+5+6+7+8+9+10=55




<구구단 문제 풀기>
        for (int i = 2; i <= 9; ++i) {
	  1번 : i가 1이니까 i <=9 의 조건 성립(true) -> 2단
        	System.out.println(i + "단");
			for (int j = 1; j <= 9; ++j) {}
            2번 : j는 1이고 j<=9 의 조건 성립 
            3번 : 아래 실행문 실행 => 2x1 = 2
            4번 : for문 마지막 실행으로 인해 j=2가 됨 
            j가 9까지 되면 조건문을 전부 충족했으니까 
            다시 처음의 for문으로 가서 3단 시작 (i++)
				System.out.println(i + "x" + j + "=" + (i * j));
			}
		}

        


 <별문제1>

 	for (int i = 0; i < 6; ++i) { 
		 1번 : i=0 이니까 i<6 조건문에 충족 밑의 이중for문으로 넘어감
		 3번 : ++i로 인해 i =1 이됨. 조건 충족하니까 다시 이중for문으로 감
			for (int j = 1; j <= i; ++j) {
			2번 : j=1이고 i=0이라서 조건 충족x 공백으로 실행됨
			4번 : j=1 이고 i=1 조건문 1<=1 충족하니까 *실행  
				System.out.print("*");
			}
			System.out.println();
		}


답:
*
**
***
****
*****
             


<배열 정리>
		int 배열[] = {10,7,3};
		int temp = 0; 
		temp = 배열[1]; =>temp는 7임
		배열[1] = 배열[0]; => 배열[1]의 값은 10
		배열[0] = temp; => 배열[0]의 값은 7
		
		
		int 배열[] = {10,7,3}
		배열[1]=배열[2]+배열[0];
		//=> 배열1의 값은? 13
		배열[0] = 배열[2]; => 배열[0]의 값은 3
		배열[2] = 배열[0]; => 배열[2]의 값은 3
		System.out.println(배열[2]);
		// => 배열2의 값은? 3
