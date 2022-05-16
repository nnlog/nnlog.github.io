---  
layout: post  
title: "algorithm baekjoon 7568"  
image: algorithm.jpg  
categories: All algorithm  
---  

# baekjoon 7568  

> [beakjoon 7568](https://www.acmicpc.net/problem/7568)  
>   
> **문제** : 우리는 사람의 덩치를 키와 몸무게, 이 두 개의 값으로 표현하여 그 등수를 매겨보려고 한다. 어떤 사람의 몸무게가 x kg이고 키가 y cm라면 이 사람의 덩치는 (x, y)로 표시된다. 두 사람 A 와 B의 덩치가 각각 (x, y), (p, q)라고 할 때 x > p 그리고 y > q 이라면 우리는 A의 덩치가 B의 덩치보다 "더 크다"고 말한다. 예를 들어 어떤 A, B 두 사람의 덩치가 각각 (56, 177), (45, 165) 라고 한다면 A의 덩치가 B보다 큰 셈이 된다. 그런데 서로 다른 덩치끼리 크기를 정할 수 없는 경우도 있다. 예를 들어 두 사람 C와 D의 덩치가 각각 (45, 181), (55, 173)이라면 몸무게는 D가 C보다 더 무겁고, 키는 C가 더 크므로, "덩치"로만 볼 때 C와 D는 누구도 상대방보다 더 크다고 말할 수 없다.  
> 
> N명의 집단에서 각 사람의 덩치 등수는 자신보다 더 "큰 덩치"의 사람의 수로 정해진다. 만일 자신보다 더 큰 덩치의 사람이 k명이라면 그 사람의 덩치 등수는 k+1이 된다. 이렇게 등수를 결정하면 같은 덩치 등수를 가진 사람은 여러 명도 가능하다. 아래는 5명으로 이루어진 집단에서 각 사람의 덩치와 그 등수가 표시된 표이다.  

> **해결** :  
> 1. 테스트 n과 (몸무게, 키)에 해당하는 값을 입력 (* 이때 몸무게, 키는 2차원배열로 저장)  
> 
> 2. 배열에 저장된 데이터들을 2중 for문으로 모두 비교하여 나보다 덩치큰사람이 있을 때마다 변수 count에 ++ (* count는 본인의 덩치크기 순위를 나타내는 변수)  
> 
> 3. 마지막으로 2차원배열에 순서에 맞게 count된 변수를 새로운 배열에 넘겨주어 저장 후 출력  

---  

<script src="https://gist.github.com/nnlog/5afdb3a43a125b6d38239e8e1ad680c5.js"></script>  

---   

p.s. `생각보다 간단하다. 이런 비교 문제가 나오면 예외상황을 생각하고 2중 for문으로 쉽게 풀어나가면 될것같다. 😁`