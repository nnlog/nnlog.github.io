---  
layout: post  
title: "algorithm baekjoon 2869 in java"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 2869  

> [beakjoon 2869](https://www.acmicpc.net/problem/2869)  
>   
> **문제** : 땅 위에 달팽이가 있다. 이 달팽이는 높이가 V미터인 나무 막대를 올라갈 것이다.  
> 
> 달팽이는 낮에 A미터 올라갈 수 있다. 하지만, 밤에 잠을 자는 동안 B미터 미끄러진다. 또, 정상에 올라간 후에는 미끄러지지 않는다.  
> 
> 달팽이가 나무 막대를 모두 올라가려면, 며칠이 걸리는지 구하는 프로그램을 작성하시오.  


> **해결** :  
> 1. 수학 공식으로 쉽게 풀어쓰면 A + (A-B)*X >= V가 성립
> 
> 2. 1번식을 풀어쓰면 X >= ( (V-A) / (A-B) )가 나오고 미지수 X값에 대한 풀이식 도출  
> 
> 3. 위 공식은 2번째 날부터 성립되는데 여기서 알수있는점은 day는 힝상 X + 1한 값이기에 식에서 나온 X값에 +1을 더한값이 day값  

---  

<script src="https://gist.github.com/nnlog/6e8a6e58caa3a5f01f5532777467c54d.js"></script>  

---   

p.s. 스캐너 이용해서 계속 돌려대는 바람에.. 시간초과로 너무 고생하다가 BufferReader로 해결했다.. 후 😨