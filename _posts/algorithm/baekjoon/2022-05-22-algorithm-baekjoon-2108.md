---  
layout: post  
title: "algorithm baekjoon 2108 in java"  
image: algorithm2.jpg  
categories: All algorithm  
---  

# baekjoon 2108  

> [beakjoon 2108](https://www.acmicpc.net/problem/2108)  
>   
> **문제** : 수를 처리하는 것은 통계학에서 상당히 중요한 일이다. 통계학에서 N개의 수를 대표하는 기본 통계값에는 다음과 같은 것들이 있다. 단, N은 홀수라고 가정하자.  
> 
> 산술평균 : N개의 수들의 합을 N으로 나눈 값  
> 
> 중앙값 : N개의 수들을 증가하는 순서로 나열했을 경우 그 중앙에 위치하는 값  
> 
> 최빈값 : N개의 수들 중 가장 많이 나타나는 값  
> 
> 범위 : N개의 수들 중 최댓값과 최솟값의 차이  
> 
> N개의 수가 주어졌을 때, 네 가지 기본 통계값을 구하는 프로그램을 작성하시오.  

> **해결** :  
> 1. 산술평균, 중앙값, 범위는 출력때 한번에 계산 가능  
> 
> 2. Arrays.sort()함수로 배열안 수를 오름차순으로 정렬  
> 
> 3. 최빈값이 여러개인 경우 2번째로 작은값이 나와야 하기 때문에 boolean값을 주어 2번째로 작은값이 최빈값으로 나오면 flase로 설정하여 다음 최빈값이나와도 바뀌지 않게 설정  

---  

<script src="https://gist.github.com/nnlog/8124d45dd7d47300534524c7ecd616d9.js"></script>  

---   

p.s. `2중 for문으로 최빈값을 검사하였더니 시간초과가 나오는바람에 고민끝에 풀이를 참고하였다. 이해가 안가는부분이 arr[i] == arr[i+1]일때만 count를 매기면 똑같은 수가 3개이상 일경우에는 count가 들어가지않는데 이게 왜 맞을까싶다. 이 조건이 맞으려면 '문제에 똑같은 수가 3번이상 들어갈 수 없습니다'라는 문구가 있어야하지 않나 싶다. 😵`