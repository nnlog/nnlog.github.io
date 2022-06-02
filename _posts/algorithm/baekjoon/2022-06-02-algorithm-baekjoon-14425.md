---  
layout: post  
title: "algorithm baekjoon 14425 in java"  
image: algorithm2.jpg  
categories: All algorithm  
---  

# 문자열집합  

> [beakjoon 14425](https://www.acmicpc.net/problem/14425)  
>   
> **문제** : 총 N개의 문자열로 이루어진 집합 S가 주어진다.  
> 
> 입력으로 주어지는 M개의 문자열 중에서 집합 S에 포함되어 있는 것이 총 몇 개인지 구하는 프로그램을 작성하시오.  

<br>  

---  

## 해결  

요번 문제는 아주아주 간단한 문제이다. 우선 문제에서 명시한 S배열에 단어를 입력하고 M번 입력하는 단어들을 포함되어 있는지 검사하면 되는데 **배열리스트**로 풀어도 되지만 난 더욱 간결한 **메서드**를 생성해서 풀어볼까한다.  

그래서 우선 BufferedReader로 N번 입력하여 배열 S를 채워주고 그 다음에 오는 M번의 문자들은 따로 배열에 저장하지 않고 바로 for문안에서 메서드로 보내는 방식으로 처리해보려고 한다.  

메서드 또한 간단하게 짤 수 있는데, 우선 가독성이 좋아질만한 메서드 이름을 includeWord로 짓고 배열 S[]와 그 순간 입력된 문자열 m을 매개변수로 지정해 줄 것이다.  

이렇게 파라미터로 넘어온 문자배열과 문자열을 비교하는 식,

`if( S[i].equals(m) )을 `이용하여 값을 boolean값으로 리턴해준다. 해당 if문에 걸리지 않는다면 존재하지 않는 단어이기 때문에 마무리로 `return false;`를 꼭 해주자.  

<br>

---  

## 완성본  

---  

<script src="https://gist.github.com/nnlog/0152054ecfda6ef257c946bab53ca49c.js"></script>  

---   

p.s. `메서드 이용하는것도 바로바로 나오는것 같고 재밌기도하다. 😁`