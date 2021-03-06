---  
layout: post  
title: "algorithm baekjoon 1269 in java"  
image: algorithm.jpg  
categories: All algorithm  
---  

# 대칭 차집합    

> [beakjoon 1269](https://www.acmicpc.net/problem/1269)  
>   
> **문제** : 자연수를 원소로 갖는 공집합이 아닌 두 집합 A와 B가 있다. 이때, 두 집합의 대칭 차집합의 원소의 개수를 출력하는 프로그램을 작성하시오. 두 집합 A와 B가 있을 때, (A-B)와 (B-A)의 합집합을 A와 B의 대칭 차집합이라고 한다.  
> 
> 예를 들어, A = { 1, 2, 4 } 이고, B = { 2, 3, 4, 5, 6 } 라고 할 때,  A-B = { 1 } 이고, B-A = { 3, 5, 6 } 이므로, 대칭 차집합의 원소의 개수는 1 + 3 = 4개이다.  

<br>  

---  

## 해결  

아주 간단하다. 문제를 이해하면 많이 단순하다는걸 알 수 있다.  

첫번째로 A-B, B-A의 차집합 원소의 개수를 알기 위해서는 문제 그대로 양쪽의 집합 차를 구하고 남은 원소의 길이를 합할 수 있지만 간결하지 못하다.  

<br>

그래서 나는 중복되는 원소의 개수를 세어 그 개수만큼을 각각의 집합 길이에서 빼주면 중복되지 않는 원수를 찾을 수 있다. 즉 이 두 집합에서 중복되는 원소를 뺀 두 집합의 원소의 개수를 합하면 그만이다.  

<br>  

간단하게 그림으로 보자.  

![image](https://user-images.githubusercontent.com/103972967/173234734-1f23b6e4-c8f6-475f-bf70-f64289c3a975.png)  

<br>  

이렇게 중복된 원소를 양쪽 집합에서 각각 지우고 나머지 원소를 합치면 남은개수가 바로 명확히 보인다.  

<br>  

**이를 바로 찾을 수 있는 HashSet을 하나 선언하여 A집합으로 사용하고 B만큼 반복하여 입력한 원소값을 바로 `contains()`문을 써서 존재하는지 확인 후에 count++해주어 이 값을 A, B에서 각각 뺄셈하여 결과 값을 합해주면 끝이 난다.**  

---  

<script src="https://gist.github.com/nnlog/32641f3b005dc4d6e52dcefffde89921.js"></script>  

---   

p.s. `아주 쉬운 문제를 아주 쉽게 풀어보았다. ㅎ 오랜만에 백준 채점속도가 빠른걸 보니 뿌듯하다. 😊`