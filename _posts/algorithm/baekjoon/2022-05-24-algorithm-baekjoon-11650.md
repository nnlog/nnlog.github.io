---  
layout: post  
title: "algorithm baekjoon 11650 in java "  
image: algorithm2.jpg  
categories: All algorithm  
---  

# baekjoon 11650  

> [beakjoon 11650](https://www.acmicpc.net/problem/11650)  
>   
> **문제** : 2차원 평면 위의 점 N개가 주어진다. 좌표를 x좌표가 증가하는 순으로, x좌표가 같으면 y좌표가 증가하는 순서로 정렬한 다음 출력하는 프로그램을 작성하시오.  

> **해결** :  
> 1. 2차원 배열 arr[i][2]에 x 및 y좌표를 대입  
> 
> 2. Arrays.sort()정렬 함수를 이용할건데 여기에 comparator를 람다식으로 표현하여 자신만의 비교방법(우선순위 판단)을 구현  
> 
> 3. e1, e2를 인자값으로 받아와 if문으로 비교 후 값이 같다면 y값인 e1[1]-e2[1]을 통해 우선순위를 결정하는데 여기서 중요한 점은 e1[1]-e2[1]을 리턴하는 이유는 결과값이 -1, 0, 1 즉 음수, 0, 양수로 나뉘는데 이를 간단히 식으로 표현(* e1[1]이 작을 시 음수를 반납하여 자리를 바꾸지않도록 한다.)  

---  

<script src="https://gist.github.com/nnlog/922428b36c2a40e32f70a369cd000777.js"></script>  

---   

p.s. `어렵다 어려워.. 분명 다른방법으로 알고리즘을 풀었는데 그놈의 시간초과 하.... 아..!!! 생각하다 2시간이 훌쩍지나서 고수의 블로그를 참고하여 한번더 배워간다...!!`  