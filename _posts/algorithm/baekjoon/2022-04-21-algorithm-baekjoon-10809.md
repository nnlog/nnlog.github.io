---
layout: post
title:  "algorithm baekjoon 10809 in java"
image: algorithm.jpg  
categories: All algorithm  
---

# baekjoon 10809  

> [baekjoon 10809](https://www.acmicpc.net/problem/10809)  
> 
> **문제** : 알파벳 소문자로만 이루어진 단어 S가 주어진다. 각각의 알파벳에 대해서, 단어에 포함되어 있는 경우 처음 등장하는 위치를, 포함되어있지 않은 경우에는 -1을 출력하는 프로그램을 작성하시오.  

> **해결**  
> 
> 1. 단어 S 입력받기  
> 
> 2. 알파벳과 비교하기 위해 알파벳이 들어있는 문자 배열 선언 후 초기화  
> 
> 3. 2중 for문을 통하여 단어에 들어가는 알파벳 각각 비교 후 알파벳 위치 출력  
> 
> 4. 이때, 존재하지 않은 알파벳을 -1로 출력하기 위해서 변수 count선언 후 검사  
> 
> 5. count값이 0으로 동일하다면 포함되어 있지 않다는 의미로 -1출력 후 초기화  
> 

---  
<script src="https://gist.github.com/nnlog/123c1c80228223b7f32feee09dcc1454.js"></script>
---  

p.s. `이번 문제는 알파벳 문자배열을 비교하는 과정에서 조금 버벅였지만 전체적으로 모르는 부분은 없어서 좋다🤠`  

