---
layout: post
title:  "algorithm baekjoon 11720"
image: algorithm.jpg  
categories: All algorithm  
---

# baekjoon 11720

>  [baekjoon 11720](https://www.acmicpc.net/problem/11720)  
> 
> **문제** : N개의 숫자가 공백없이 쓰여있다. 이 숫자를 모두 합해서 출력하는 프로그램을 작성하시오.  

> **해결**  
> 1. 숫자 개수 N 입력받기  
> 2. 숫자를 문자열로 입력  
> 3. 문자열을 substring함수를 이용해서 분해 후 일괄 더하기  

---  

<script src="https://gist.github.com/nnlog/a3aaade0260361750aa505056ada0794.js"></script>  

<br/>  

```java
import java.util.Scanner;

public class Main {

	public static void main(String[] args) {
		
		Scanner scan = new Scanner(System.in);
		
		int n = scan.nextInt();
		String str = scan.next();
		int num = 0;
		
		scan.close();
		
		for(int i=0; i<n; i++) {
			num += Integer.parseInt(str.substring(i, i+1));
		}
		
		System.out.println(num);
	}
	
}
```  
---  

p.s. `Integer.parseInt() 안에 substring 함수를 넣는 부분에서 조금 막힌게 아쉽다.😞`


