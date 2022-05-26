---  
layout: post  
title: "algorithm baekjoon 2751(JAVA)"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 2751  

> [beakjoon 2751](https://www.acmicpc.net/problem/2751)  
>   
> **문제** : N개의 수가 주어졌을 때, 이를 오름차순으로 정렬하는 프로그램을 작성하시오.

> **해결** :  
> 1. 조금더 시간 단축을 위해서 BufferReader로 입력  
> 
> 2. 입력받은 배열안 수를 오름차순으로 정리하기 위해서 Array.sort()함수를 이용  
> 
> 3. 정리된 배열을 출력  

---  

<script src="https://gist.github.com/nnlog/69527fa4034fd087ba6e522b9500d57f.js"></script>  

---   

p.s. `코드를 보다시피 주석처리되어있는 부분은 내가 간단하게 짜놓은 수 정렬 함수이다. 근데 시간초과가 뜨는걸보니 더욱 빠르길 바라는것같아 알아보니 이중 for문 대신 Array.sort()라는 간단한 정렬함수를 이용하였더니 해결! Array.sort() 대단한 함수 메모... 😲`