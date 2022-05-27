---  
layout: post  
title: "algorithm baekjoon 1427 in java "  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 1427  

> [beakjoon 1427](https://www.acmicpc.net/problem/1427)  
>   
> **문제** : 배열을 정렬하는 것은 쉽다. 수가 주어지면, 그 수의 각 자리수를 내림차순으로 정렬해보자.  

> **해결** :  
> 1. 입력받은 수를 문자열로 변환  
> 
> 2. 문자열로 변환후 2중 for문으로 각 자리 숫자를 바로 옆숫자와 비교  
> 
> 3. 비교 후 만약 앞서 나온 수가 더 큰 경우 새로운 문자변수에 값을 저장하는 방법으로 자리 교체 후 출력(*이때 문자끼리 비교해도 아스키코드값으로 비교되므로 숫자와 똑같이 비교가능하다.)  

---  

<script src="https://gist.github.com/nnlog/ecf2f2fadf7b0ccebfc1031a142950eb.js"></script>  

---   

p.s. `새로운 변수를 이용해서 자리 교체하는게 순발력있게 떠올랐지만 역시 자바이기 때문에 2중 for문으로 인한 시간초과 가능성에 기대도없었다. 근데 이게 되네?🥴`  