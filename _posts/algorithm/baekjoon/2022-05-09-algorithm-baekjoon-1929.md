---  
layout: post  
title: "algorithm baekjoon 1929"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 1929  

> [beakjoon 1929](https://www.acmicpc.net/problem/1929)  
>   
> **문제** : M이상 N이하의 소수를 모두 출력하는 프로그램을 작성하시오.

> **해결** :  
> 1. M과 N을 입력  
> 
> 2. **에라토스테네스의 체**함수 이용  
> 
> 3. 출력  

---  

<script src="https://gist.github.com/nnlog/916cdabc245d76321993fc134cee6ede.js"></script>  

---   

## 내 코드  
```  
import java.io.BufferedReader;
import java.io.IOException;
import java.io.InputStreamReader;
import java.util.StringTokenizer;

public class Main {

	public static void main(String[] args) throws IOException {
		
		BufferedReader br = new BufferedReader(new InputStreamReader(System.in));
		
		StringTokenizer st = new StringTokenizer(br.readLine());
		int M = Integer.parseInt(st.nextToken());
		int N = Integer.parseInt(st.nextToken());
		int count=0;
		
		br.close();
		for(int i=M; i<=N; i++) {
			for(int j=1; j<=i; j++) {
				if(i%j == 0) count++;				// 나누어 떨어지면 인수
			}
			if(count == 2) System.out.println(i); 	// 인수가 1과 자기자신이면 소수
			count = 0;
		}
	}
}

```  

---  

p.s. `문제가 아주 간단하다. 아 근데 분명 내가 작성한 코드가 깔끔하고 답도 정확한데 자꾸 시간초과 시간초과 미치는줄 알았다.. 후 결국 서치해서 에라토스테네스의 체를 이용하여야 성공이라 뜨는게 자바는 자체 출력속도가 현저히 느려서 그렇다한다. 그래도 난 내 코드가 더 읽기쉽다.. 아쉬워서 내 코드도 같이 남겨야지.. 😞`