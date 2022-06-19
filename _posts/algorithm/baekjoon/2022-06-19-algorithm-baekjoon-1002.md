---  
layout: post  
title: "algorithm baekjoon 1002 in java"  
image: algorithm2.jpg  
categories: All algorithm  
---  

# [터렛](https://www.acmicpc.net/problem/1002) 

<br>  

![문제사진](https://user-images.githubusercontent.com/103972967/174479225-ec207377-2c45-46b4-9bc4-47bea813f807.png)  

<br>  

---  

<br>  

## 해결  

<br>  

보기에 어려워 보이는데 실제로 어렵디.  
이게 무슨 문제지 싶은데 알것같다가도 모르겠어서 구글의 힘을 빌려보고 정리한다.  

<br>  

우선 조규현(x1, y1)와 백승환의 좌표(x2, y2)에서 r1, r2만큼 떨어진 위치의 류재명을 구하려면 원으로 접근한다는건 알 것이다.  

여기서 우리는 크게 3가지의 경우로 나눌것인데  

<br>  

### 1. 조규현과 백승환의 위치가 같고 떨어진 거리까지 같을때, 즉 두 원이 정확히 겹칠때  

<br>  

![1](https://user-images.githubusercontent.com/103972967/174480890-555edbf8-00be-43c3-9f77-d1c6ece7b8e4.jpeg)  

x1 == x2, y1 == y2, r1 == r2일때 류재명의 위치는 무수히 많다.  

<br>  

### 2. 원이 만나지 않을때  

<br>  

![2.1](https://user-images.githubusercontent.com/103972967/174480978-1aa6765c-0a84-44b3-83e0-83b621de33ab.jpeg)  

원이 만나지 않을 때는 2가지 경우가 있는데  

첫 번째가 바로 원안에 원이 있을 때 만나지 않는경우다.  

<br>  

![2.2](https://user-images.githubusercontent.com/103972967/174480948-6f188466-ed85-4f20-9d77-d39cff34dbeb.jpeg)  

두 번째는 두 원의 중점거리가 두 원의 반지름 합보다 더 멀리있을 경우 즉,  

원이 겹치지 않고 멀리 떨어져 있을 때이다.

<br>  

### 3. 원이 한점에서 만날때

<br>  

![3.1](https://user-images.githubusercontent.com/103972967/174481060-8c26a4ea-1efa-4871-9182-9dbe2554b3c4.jpeg)  

원이 한점에서 만나는 경우도 2가지가 있는데  

첫 번째가 원안에서 내접할때,

<br>  

![3.2](https://user-images.githubusercontent.com/103972967/174481045-c6739e15-0848-4f27-91ff-eca2663c90c2.jpeg)  

두 번째가 원밖에서 외접할때이다.  

<br>  

---  

<br>  

## 완성본  

<br>  

<script src="https://gist.github.com/nnlog/57299b712d22ae1477b98b60191f5b7b.js"></script>  

---   

p.s. `오랜만에 원의 중점의 거리와 반지름을 통해 만나는 점들을 구해보니 어려웠다... 아 기억이 안나니 문제를 못푸는 내가 화나네 😬`