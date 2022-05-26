---  
layout: post  
title: "algorithm baekjoon 10872(JAVA)"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 10872  

> [beakjoon 10872](https://www.acmicpc.net/problem/10872)  
>   
> **문제** : 0보다 크거나 같은 정수 N이 주어진다. 이때, N!을 출력하는 프로그램을 작성하시오.  

> **해결** :  
> 1. N을 입력  
> 
> 2. 입력받은 N을 매개변수로 갖는 메서드를 생성  
> 
> 3. N이 0이되기 전까지 N * function(N-1)의 값을 리턴해주고 0일 때는 숫자 1로 리턴  

---  

<script src="https://gist.github.com/nnlog/78f9fda824b3bcbe66154e85c0449631.js"></script>  

---   

p.s. `재귀함수 음.. for문 짱 😂`