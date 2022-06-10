---  
layout: post  
title: "algorithm baekjoon 1764 in java"  
image: algorithm2.jpg  
categories: All algorithm  
---  

# 듣보잡  

> [beakjoon 1764](https://www.acmicpc.net/problem/1764)  
>   
> **문제** : 김진영이 듣도 못한 사람의 명단과, 보도 못한 사람의 명단이 주어질 때, 듣도 보도 못한 사람의 명단을 구하는 프로그램을 작성하시오.  

<br>  

---  

## 해결  

이번 문제는 중복된 이름의 개수와 명단을 출력하는 프로그램을 짜면 된다.  

<br>  

우선 첫번째로 입력할 그릇을 선택해야하는데 첫번째 듣도 못한 사람의 명단은 간편하게 입력 가능한 **HashSet**을 사용할 것이고,  
두 번째로 보도 못한 사람의 명단에는 **ArrayLis**t를 활용할 것인데 그 이유는 오름차순으로 정렬하기에 편리한 **Collections.sort()**가 있기 때문이다. 배열을 정렬하는 메서드인 Arrays.sort()와 기능은 똑같다.  

<br>  

그릇을 정했다면 문제의 반이상은 풀은 샘이다. (나도 Arrays.sort()쓰려다 돌고 돈건 비밀)  

<br>  

HashSet에 각 듣도 못한 사람의 명단을 입력하여 넣어주고 바로 보도 못한사람의 명단에 들어갈 이름을 입력하여 비교하는 contains()메서드를 사용하면 곧 바로 중복되는 명단인지 알 수 있다.  

<br>  

그렇게 중복되는 명단은 ArrayList에 add로 저장하여  
**Collections.sort()**로 정렬해 주고 출력하면 끝이다.  

<br>  

---  

## 완성본  

---  

<script src="https://gist.github.com/nnlog/341ac2724a00e513193f664cc15089b0.js"></script>  

---   

p.s. `ArrayList -> Collections.sort() , Array -> Arrays.sort() 기억하자 ! 그리고 HashSet을 통해 인자 한가지만을 저장하고 contains로 비교할 수 있단 것도 명심! 🤔`