---  
layout: post  
title: "algorithm baekjoon 17478"  
image: algorithm2.jpg  
categories: All algorithm  
---  

# baekjoon 17478  

> [beakjoon 17478](https://www.acmicpc.net/problem/17478)  
>   
> **문제** : 평소에 질문을 잘 받아주기로 유명한 중앙대학교의 JH 교수님은 학생들로부터 재귀함수가 무엇인지에 대하여 많은 질문을 받아왔다.  
> 
> 매번 질문을 잘 받아주셨던 JH 교수님이지만 그는 중앙대학교가 자신과 맞는가에 대한 고민을 항상 해왔다.  
> 
> 중앙대학교와 자신의 길이 맞지 않다고 생각한 JH 교수님은 결국 중앙대학교를 떠나기로 결정하였다.  
> 
> 떠나기 전까지도 제자들을 생각하셨던 JH 교수님은 재귀함수가 무엇인지 물어보는 학생들을 위한 작은 선물로 자동 응답 챗봇을 준비하기로 했다.  
> 
> JH 교수님이 만들 챗봇의 응답을 출력하는 프로그램을 만들어보자.  

> **해결** :  
> 1. 반복되는 구문을 살피고 그 문장들을 출력하는 메서드를 하나 생성  
> 
> 2. 메서드안에 매개변수 n-1만큼 재귀함수 호출  
> 
> 3. 전역변수 str에 ____언더바4개를 한번끝날때마다 더해서 저장  
> 
> 4. 마무리 "라고 답변하였지."부분은 따로 메인함수에서 작성  

---  

<script src="https://gist.github.com/nnlog/efa79e9834205c146520afdded02ef33.js"></script>  

---   

p.s. `아 처음에는 순조롭게 언더바없이 완성시키고 제출하였는데, 정확히 오타없이 만들어야되는걸 알고 좀 대공사를 거쳤다.. 재귀함수에 대해서 공부하기 위해서 낸 문제같은데 굳이 언더바를 넣은 이유가..? 이것때문에 40분고민을 더했던것같다. 어쨋든 성장! 🥲`