# 별찍기로 만든 피라미드

## 알고리즘
사용자에게 키보드로 원하는 층을 입력하여 만들고 그 층 만큼 반복 하여야 하는데 <br\>
원하는 층 만큼 반복하고, 그 안에 공백 출력과 별을 출력하는 반복문이 필요하다. <br\>
모양은 1, 3, 5, 7, 9... 처럼 2씩 증가하고 공백의 갯수로 모양을 <br\> 
잡아야하기때문에 공백 출력을 하는데 공백 출력을 하는 공식은 (현재층 - 현재층)을 하면 공백 출력을 하고 <br\>
그 다음 별 출력을 해주어야 하는데, 별을 출력하는 공식은 ((현재층 - 1) * 2 + 1)을 해주면 별이 출력된다.<br\> 

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
