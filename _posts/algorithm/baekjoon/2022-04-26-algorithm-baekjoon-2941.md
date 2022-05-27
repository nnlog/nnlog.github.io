---  
layout: post  
title: "algorithm baekjoon 2941 in java"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 2941  

> [beakjoon 2941](https://www.acmicpc.net/problem/2941)  
>   
> **문제** : 예전에는 운영체제에서 크로아티아 알파벳을 입력할 수가 없었다. 따라서, 다음과 같이 크로아티아 알파벳을 변경해서 입력했다.  
> 
> 예를 들어, ljes=njak은 크로아티아 알파벳 6개(lj, e, š, nj, a, k)로 이루어져 있다. 단어가 주어졌을 때, 몇 개의 크로아티아 알파벳으로 이루어져 있는지 출력한다.  
>  
> dž는 무조건 하나의 알파벳으로 쓰이고, d와 ž가 분리된 것으로 보지 않는다. lj와 nj도 마찬가지이다. 위 목록에 없는 알파벳은 한 글자씩 센다.  

> **해결** :  
> 1. 문자열 받아오기  
> 
> 2. 위의 표에 해당하는 알파벳의 경우를 판단하여 새로운 변수에 글자수가 1개가 되도록하는 정수를 저장 (ex. nj > count + 1 , dz= > count + 2)  
> 
> 3. 위 문자열에서 추려낸 정수 변수를 전체 문자열길이에서 빼서 크로아티아 글자수 출력

---  

<script src="https://gist.github.com/nnlog/ac9605a87eb5276566ba0b559468b9f0.js"></script>  

---   
