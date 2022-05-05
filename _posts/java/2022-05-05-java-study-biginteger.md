---  

layout: post  
title: "java study about BigInteger"  
image: javastudy.jpg  
categories: All java  

---  

# BigInteger  

> * BigIntegr는 문자열 형태로 이루어져 있어 숫자의 범위가 무한하기에 어떠한 숫자든지 담을 수 있다.  
> 
> * 따라서, 정수형태 long의 범위를 넘어가는 상황에 필요하다.  

<br>  

---  

## 1. int, long 타입의 범위  

|Type|범위|
|--|--|
|int|-2,147,483,648 ~ 2,147,483,647|
|long|-9,223,372,036,854,775,808 ~ 9,223,372,036,854,775,808|  

long타입의 범위가 정말 커서 넘을일이 별로 없지만 특이상황에서는 혹시나하는 최악의 일이 발생하지 않도록 BigInteger를 쓰는게 현명하다.  

<br>  

---  

## 2. BigInteger 사용볍  

`BigInteger bigNumber = new BigInteger("100000000000000000000")`  

보이는 것과 같이 선언하면 된다. 특이한 점이라고는 BigInteger를 초기화 하기 위해서는 반드시 문자열로 값을 넘겨주어야 한다.  

```  
BigInteger bitNumber1 = new BigInteger("100000000");  
BigInteger bitNumber2 = new BigInteger("1000000000000");  

Systerm.out.println("+ : " + bigNumber1.add(bigNumber2));  
Systerm.out.println("- : " + bigNumber1.subtract(bigNumber2));  
Systerm.out.println("* : " + bigNumber1.multiply(bigNumber2));  
Systerm.out.println("/ : " + bigNumber1.divide(bigNumber2));  
Systerm.out.println("% : " + bigNumber1.remainder(bigNumber2));  
```  

위와 같이 기본적인 계산식을 명령어를 통해 해결할 수 있다.  

```  
int int_bigNum = bigNumber.intvalue();  // int로 형 변환  
long long_bigNum = bigNumber.longvalue();  // long로 형 변환  
```  

형변환 또한 명령어를 통해 해결가능하다. 나머지 float, double, string으로 똑같은 형태로 선언하면 된다.  

