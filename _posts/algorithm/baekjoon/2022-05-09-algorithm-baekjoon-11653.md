---  
layout: post  
title: "algorithm baekjoon 11653 in java "  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 11653  

> [beakjoon 11653](https://www.acmicpc.net/problem/11653)  
>   
> **문제** : 정수 N이 주어졌을 때, 소인수분해하는 프로그램을 작성하시오.

> **해결** :  
> 1. 정수 N을 입력  
> 
> 2. if~else문으로 N==1일경우를 예외 처리  
> 
> 3. N은 1이 아닐경우 2부터 시작하여 나누었을 때 나머지가 0으로 딱 나누어떨어지는 인수를 배열에 저장 나누어 떨어지지 않으면 나누는 값을 ++하여 계속해서 증가  
> 
> 4. 계속해서 나누어 떨어지는 값을 배열에 저장후 순서대로 출력  

---  

<script src="https://gist.github.com/nnlog/d4c9980b105140377e1fb697cc0cf40f.js"></script>  

---   

p.s. `처음 N != 0일때까지 while문을 주어서 배열오류가 생기길래 무슨일인가 싶어 N의 값 변화를 계속해서 출력하여 보니 인수분해가 끝나면 N은 0이 아닌 1의 값을 가지게 된다는걸 알고 바로 수정하니 맞았다. 🤩`