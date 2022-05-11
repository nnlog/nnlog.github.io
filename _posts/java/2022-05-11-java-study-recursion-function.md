---  

layout: post  
title: "java study about Recursion Function"  
image: javastudy.jpg  
categories: All java  

---  

# Recursion Function  

문득 백준 문제를 풀다가 **재귀함수**라는 문제를 풀게 되었는데 뭐지? 어디서 들어본것같은데? 하면서 구글링을 해보는 나를 보고 모른다는걸 확신했다.  

그렇게 재귀함수에 대해서 몆자 끄적여놓고 까먹을 때 한번씩 보려고 글을 작성한다.  

> **재귀함수란?**  
> 
> * 재귀함수는 정의 단계에서 자신을 재참조하는 함수를 뜻한다.  
> 
> * 어떤 사건이 자기 자신을 포함하고 다시 자기 자신을 사용하여 정의될 때 재귀적(recursive)이라고 한다. 설명 할 때 자기를 포함한 것이라고 생각하면 편하다. 그냥 자기를 설명할 때 나는 나야 나라는 건 나야 이렇게 설명하는 것이라고 볼 수 있다.  

<br>  

---  

<br>  

## Recursion Function(재귀함수) 사용법  

### 팩토리얼  
```  
public class main{
    public static void main(String[] args) {
        System.out.println( factorial[10] ); // 10! 결과 값 출력
    }

    // 팩토리얼 메서드 선언  
    public static int factorial(int n){
        if(n == 0){
            return 1;   // 메서드의 값이 0이되면 함수를 리턴하는것이 아닌 1을 리턴해서 끝낸다.  
        } else {
            return n * factorial( n-1 ); // 함수를 다시 리턴해주어 반복한다.
                                         // n * (n-1) * (n-2) ... * factorial(0) 이런식으로 계속해서 함수를 부른다.
        }
    }
}
```  

이렇게 보이듯이 함수안에서 반복적으로 자기자신(함수)을 선언하는 것을 **재귀 함수**라고 한다.  
이렇게 반복적으로 무언가를 수행할 때, 반복문 대신 재귀함수로도 표현할 수 있다.  

예제를 하나더 살펴보자.  

### 피보나치의 수열  
```  
public class main{
    public static void main(String[] args){
        int n = 10;

        for(int i=0; i<n; i++){
            System.out.print(fibonacci(i) + " ");  
        }
    }

    // 피보나치를 나타내는 메서드
    public static int fibonacci(int n){
        if(n == 0) return 0;  
        else if(n == 1 || n == 2) return 1;  
        else return fibonacci(n-1) + fibonacci(n-2);  
    }
}
```

피보나치 수열을 보면 1 1 2 3 5 8 13 ...  

이런식으로 N = (N-1) + (N-2)이 계속해서 나타나는걸 볼 수 있다.  

이렇듯 재귀함수를 이용해서 피보나치 수열을 만들 수 있단걸 확인할 수 있다.  

