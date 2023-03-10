# 별찍기로 만든 피라미드

## 알고리즘
반복문(for)을 총 3개를 사용하여 줄바꿈, 공백출력, 별출력을 하는것이다. <br/>
3단 피라미드를 출력한다고 가정했을 때, <br/>


## Java Code
```java
import java.util.Scanner;

public class Quiz2 {
	public static void main(String[] args) {
		Scanner sc = new Scanner(System.in);
		
		System.out.println("피라미드 모양을 출력");
		int n;
		
		do {
			System.out.println("몇단 삼각형 입니까?");
			n = sc.nextInt();
		}while (n <= 0); 					// true 일 경우 반복 false 일 경우 do-while문을 빠져나감  
		
		for(int i = 0; i < n; i++) {				// n단 피라미드 출력
			for(int j = 0; j < n-i-1; j++) {		// 공백 출력 for문 
				System.out.print(" ");			// 공백 출력
			}		
			for(int j = 0; j < i*2+1; j++) {		// 1, 3, 5, 7, 9... 2씩 늘어나는 for문
				System.out.print("*");			// 별 출력
			}
			System.out.println();				// 줄바꿈 
		}
	}
}
```
## 코드 해석

* int n 변수 선언 (7번째 줄)
* do-while문으로 몇 단 피라미드를 만들 것인지 물어보고 만약 0보다 작거나 같으면 다시 입력하라고 말하기 위해서
  do-while문으로 작성함 (14번째 줄 ~ 17번째 줄)
* 
