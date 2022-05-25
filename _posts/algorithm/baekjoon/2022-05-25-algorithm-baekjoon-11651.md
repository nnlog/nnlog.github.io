---  
layout: post  
title: "algorithm baekjoon 11651"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 11651  

> [beakjoon 11651](https://www.acmicpc.net/problem/11651)  
>   
> **문제** : 2차원 평면 위의 점 N개가 주어진다. 좌표를 y좌표가 증가하는 순으로, y좌표가 같으면 x좌표가 증가하는 순서로 정렬한 다음 출력하는 프로그램을 작성하시오.  

> **해결** :  
> 1. 2차원 배열 arr[i][2]에 x 및 y좌표를 입력    
> 
> 2. Arrays.sort()정렬 함수를 이용하여 자신만의 비교방법 구현  
> 
> 3. 앞서 풀었던 11650번과 같이 e1, e2를 인자값으로 넘겨주는데 여기서 다른점은 y값이 먼저 비교되어야 하기때문에 if문을 이용하여 e1[1]-e2[1]값을 먼저 리턴해주고 같다면 e1[0]-e2[0]을 비교하여 음수, 0, 양수를 리턴(* 이때 음수이면 앞으로 이동하는 원리, 0은 똑같은 좌표일때 나올수 있는데 이때는 자리변동 x)  

---  

<script src="https://gist.github.com/nnlog/64a261f6c891f1ae304cc3fa9d7511f3.js"></script>  

---   

p.s. `시간 초과 없이 깔끔하게 풀기 어려운 문제다. Arrays.sort()에 대한 이해도가 빠삭해야만 이런식이나오는데 그래도 이번에 두 번째로 써보니 감이온다. x값을 먼저 비교하는 문제는 `[baekjoon 11650](https://nnlog.github.io/2022/05/24/algorithm-baekjoon-11650/) `이 문제를 보면 될듯 싶다. 앞전에 풀어보고 원리만 이해한 상태로 혼자 풀어보았는데 바로 적용되서 기분 좋다. `