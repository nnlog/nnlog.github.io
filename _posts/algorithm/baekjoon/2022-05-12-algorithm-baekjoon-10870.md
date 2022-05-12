---  
layout: post  
title: "algorithm baekjoon 10870"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 10870  

> [beakjoon 10870](https://www.acmicpc.net/problem/10870)  
>   
> **문제** : 피보나치 수는 0과 1로 시작한다. 0번째 피보나치 수는 0이고, 1번째 피보나치 수는 1이다. 그 다음 2번째 부터는 바로 앞 두 피보나치 수의 합이 된다.
>   
> 이를 식으로 써보면 Fn = Fn-1 + Fn-2 (n ≥ 2)가 된다.  
> 
> n=17일때 까지 피보나치 수를 써보면 다음과 같다.  
> 
> 0, 1, 1, 2, 3, 5, 8, 13, 21, 34, 55, 89, 144, 233, 377, 610, 987, 1597  
> 
> n이 주어졌을 때, n번째 피보나치 수를 구하는 프로그램을 작성하시오.  

> **해결** :  
> 1. 입력받은 n을 매개변수로 갖는 피보나치의 함수를 이용한 매서드를 생성  
> 
> 2. 매서드에 if문으로 0일때 0으로 리턴, 1과 2일때는 1값으로 리턴하는 예외처리  
> 
> 3. 메인메서드에서 출력  

---  

<script src="https://gist.github.com/nnlog/0fa028bf231cf9c4d70989af7e871e32.js"></script>  

---   

p.s. `재귀함수를 이용한 피보나치 수열은 앞서 등록해놓은` [재귀함수](https://nnlog.github.io/2022/05/11/java-study-recursion-function/)`게시물을 보면 이해가 쉽다 😀`  