---  
layout: post  
title: "algorithm baekjoon 10814 in java"  
image: algorithm2.jpg  
categories: All algorithm  
---  

# baekjoon 10814  

> [beakjoon 10814](문제 사이트url)  
>   
> **문제** : 온라인 저지에 가입한 사람들의 나이와 이름이 가입한 순서대로 주어진다. 이때, 회원들을 나이가 증가하는 순으로, 나이가 같으면 먼저 가입한 사람이 앞에 오는 순서로 정렬하는 프로그램을 작성하시오.  

> **해결** :  
> 1. 입력한 테스트 N번만큼 2차원 배열에 문자열로 순서대로 나이, 이름을 입력  
> 
> 2. 2차원 배열을 Arrays.sort()를 이용해 나이로 비교후 값을 리턴  
> 
> 3. 순서대로 출력  

---  

<script src="https://gist.github.com/nnlog/83981a3b231150a43da3999fd82a5d1e.js"></script>  

---   

p.s. `계속 풀다보니 이제 Arrays.sort()에 적응되가는게 느껴진다. 정확히 이 기능의 원리를 이해한건 아니지만 몇번쓰다보니 어떤문제를 어떻게 적용시켜야하는지 감이 온다. 😊`