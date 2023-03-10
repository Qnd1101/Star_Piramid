# 별찍기로 만든 피라미드

## 알고리즘


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
## 코드 출력
![image](https://user-images.githubusercontent.com/107795830/224196508-b4b51e3c-2985-4716-a12f-7b0badd3a1d3.png)

## 코드 해석
```java
do {
	System.out.println("몇단 삼각형 입니까?");
	n = sc.nextInt();
}while (n <= 0); 
```
입력한 값이 0보다 작거나 같을 경우에 다시 입력하기위해서 이 코드를 작성했습니다.

```java
for(int i = 0; i < n; i++) {			// n단 피라미드 출력
	for(int j = 0; j < n-i-1; j++) {	// 공백 출력 for문 
	System.out.print(" ");			// 공백 출력
	}	
	for(int j = 0; j < i*2+1; j++) {	// 1, 3, 5, 7, 9... 2씩 늘어나는 for문
	System.out.print("*");			// 별 출력
	}
	System.out.println();			// 줄바꿈 
}
```
* 첫번째 for문은 줄바꿈을 위해서 작성하였습니다. <br\>
* 두번째 for문은 공백을 출력하기 위하여 작성하였는데 반복 조건이 n-i-1인 이유는 
