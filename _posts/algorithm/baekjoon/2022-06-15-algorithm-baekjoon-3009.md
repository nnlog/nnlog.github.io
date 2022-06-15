---  
layout: post  
title: "algorithm baekjoon 3009 in java"  
image: algorithm.jpg  
categories: All algorithm  
---  

# 네 번째 점  

> [beakjoon 3009](https://www.acmicpc.net/problem/3009)  
>   
> **문제** : 세 점이 주어졌을 때, 축에 평행한 직사각형을 만들기 위해서 필요한 네 번째 점을 찾는 프로그램을 작성하시오.  

<br>  

---  

<br>  

## 해결  

문제가 무슨 소리인지 계속 쳐다보았다.  
근데 축에 평행한 직사각형을 만들기 위해선 네 점의 x, y값들이 중복되는 값을 가져야한다.  

<br>  

![image](https://user-images.githubusercontent.com/103972967/173857207-718dc6ea-8c2a-4f04-9aaa-9d5798d882cf.png)  

이렇게 (30 20), (10 10), (10 20) 주어진다면 자동적으로 적게 나온 값이 마지막 4번째 x, y의 값이 된다. 즉, x값은 30이 되고 y값은 적게나온 10이 되서 (30, 10)이된다.  

<br>  

---  

<br>  

## 완성본  

<script src="https://gist.github.com/nnlog/4922cd8bb33ad9d35f66bd9e3d5b14ae.js"></script>  

---   

p.s. `간단하게 클리어~ 😃`  