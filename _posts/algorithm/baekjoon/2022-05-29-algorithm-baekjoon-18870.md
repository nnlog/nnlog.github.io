---  
layout: post  
title: "algorithm baekjoon 18870 in java"  
image: algorithm2.jpg  
categories: All algorithm  
---  

# baekjoon 18870  

> [beakjoon 18870](https://www.acmicpc.net/problem/18870)  
>   
> **문제** : 수직선 위에 N개의 좌표 X1, X2, ..., XN이 있다. 이 좌표에 좌표 압축을 적용하려고 한다.  
> 
> Xi를 좌표 압축한 결과 X'i의 값은 Xi > Xj를 만족하는 서로 다른 좌표의 개수와 같아야 한다.  
> 
> X1, X2, ..., XN에 좌표 압축을 적용한 결과 X'1, X'2, ..., X'N를 출력해보자.  

> **해결** :  
> 1. origin, sorted로 원본, 정렬 및 중복제거된 배열을 만들어 값 입력  
> 
> 2. 정렬된 배열에서 순서대로 값을 가져와서 HashMap에 저장 (*이때 중복된값이 다시 저장되면 안되기때문에 containsKey명령어를 통해 검사)  
> 
> 3. 이번엔 원본 배열에서 값을 순서대로 가져와 HashMap에서 같은 값에 해당하는 인덱스를 변수에 저장 후 StringBuilder로 출력  

---  

<script src="https://gist.github.com/nnlog/cc1efba0e9a67667fc83ecdb7c87c4b1.js"></script>  

---   

p.s. `처음 나는 비슷한 맥락으로 원본 배열을 메소드로 중복 제거 후 정렬 하여 새로운 배열을 가져와 2중 for문으로 같은값에 해당하는 인덱스값을 출력하였는데 시간초과... 답은 똑같이 잘나오는데 2중 for문이 시간복잡도에 걸리기 때문이다. 그래서 고수의 HashMap을 이용한 방법을 배우면서 가져와보았다. 😅`