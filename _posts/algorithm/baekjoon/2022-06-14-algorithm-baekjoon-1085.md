---  
layout: post  
title: "algorithm baekjoon 1085 in java"  
image: algorithm.jpg  
categories: All algorithm  
---  

# 직사각형에서 탈출  

> [beakjoon 1085]((https://www.acmicpc.net/problem/1085))  
>   
> **문제** : 한수는 지금 (x, y)에 있다. 직사각형은 각 변이 좌표축에 평행하고, 왼쪽 아래 꼭짓점은 (0, 0), 오른쪽 위 꼭짓점은 (w, h)에 있다. 직사각형의 경계선까지 가는 거리의 최솟값을 구하는 프로그램을 작성하시오.  

<br>  

---  

<br>  

## 해결  

결국 직사각형의 경계선까지 가는 거리의 경우의 수는  

(0, 0)  (x, y)  (w, h) 이렇게 좌표가 주어질때 현재 위치는 (x, y)이므로  

첫 번째 최단거리 후보는 (x, y) - (0, 0) 즉, 그냥 x, y가 최단거리 후보가 된다.  

두 번째 최단거리 후보는 (w, h) - (x, y) 즉, (w-x, h-y)가 된다.  

<br>  

**여기서 경계선까지 가는 최단거리이기 때문에 x가 될 수 있고 y가 될 수 있고 w-x가 될 수 있고 h-y가 될 수 있다.**  

<br>  

---  

<br>  

## 완성본  

<script src="https://gist.github.com/nnlog/47f7d10aaf77f166a1f289a019c58852.js"></script>  

---   

p.s. `너무 간단한 문제 풀며 쉬어가기 🥲`