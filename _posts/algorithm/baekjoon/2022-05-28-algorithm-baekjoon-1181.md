---  
layout: post  
title: "algorithm baekjoon 1181 in java"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 1181  

> [beakjoon 1181](https://www.acmicpc.net/problem/1181)  
>   
> **문제** : 알파벳 소문자로 이루어진 N개의 단어가 들어오면 아래와 같은 조건에 따라 정렬하는 프로그램을 작성하시오.  
> 
> 1. 길이가 짧은 것부터  
> 
> 2. 길이가 같으면 사전 순으로  

> **해결** :  
> 1. N번만큼 단어를 입력  
> 
> 2. 입력된 단어들이 저장된 배열을 Arrays.sort()를 이용해 길이를 비교하고 같을시에는 다음 알파벳을 비교하는 compareTo를 이용  
> 
> 3. 마지막으로 출력문에서 같은 단어가 있을시 중복 되지 않게 출력  

---  

<script src="https://gist.github.com/nnlog/dcafc6df27868b6ba5dcd6511f76b0ef.js"></script>  

---   

p.s. `비교는 Arrays.sort() ! 🙃`