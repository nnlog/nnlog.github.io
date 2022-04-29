# Overloading VS Overriding  
오버라이딩과 오버로딩, 이름이 비슷한 두 개의 차이점을 살펴보려고 한다.  

## 1. Overloading  
한 클래스 내에 같은 이름의 메서드를 여러 개 정의하는 것을 '메서드 오버로딩' 또는 '오버로딩'이라 한다.  

> 조건  
> 1. **메서드 이름이 같아야 한다.**  
> 
> 2. **매개변수의 개수 또는 타입이 달라야 한다.**  
> 
> 3. **반환 타입은 관계 없다.**  

PintStream클래스에는 어떤 종류의 매개변수를 지정해도 출력할 수 있도록 아래와 같이 10개의 오버로딩된 prinln메서드를 정의해놓고 있다.  

`void println()`  
`void println(boolean x)`  
`void println(char x)`  
`void println(char[] x)`  
`void println(double x)`  
`void println(float x)`  
`void println(int x)`  
`void println(long x)`  
`void println(Object x)`  
`void println(String x)`  

위 정의된대로 어떤 매개변수가 오더라도 println메서드를 호출할 수 있게 되어있다.  

몇가지 예를 들어 오버로딩에 대해 자세히 살펴봅시다.  

```  
int add(int a, int b) { return a+b; }  
int add(int x, int y) { return x+y; }  
```  
위의 두 메서드는 매개변수의 이름만 다를 뿐 매개변수의 타입이 같기 때문에 오버로딩 성립 **X**  

```  
int add(int a, int b) { return a+b; }  
long add(int a, int b) { return (long)(a+b); }  
```  
이번 경우는 리턴 타입만 다른 경우이다. 매개변수의 타입과 개수가 일치하기 때문에 add(3,3)과 같이 호출하였을 때 어떤 메서드가 호출될 것인지 결정할 수 없기 때문에 오버로딩으로 간주되지 않는다.  

```  
long add(int a, long b) { return a+b; }  
long add(long a, int b) { return a+b; }  
```  
두 메서드는 매개변수의 순서가 다르다. 이 같은 경우에는 호출시 매개변수 타입에 따라 호출될 메서드가 분명하기에 오버로딩이 **성립**된다.  

<br>  

---  

## 2. Overriding  
부모 클래스로부터 상속받은 메서드의 내용을 변경하는 것을 오버라이딩이라고한다.  

> 조건  
> 1. **접근 제어자는 부모 클래스의 메서드보다 좁은 범위로 변경할 수 없다.**  
> 
> 2. **부모 클래스의 메서드보다 많은 수의 예외를 선언할 수 없다.**  

ex) 예외 선언  
```  
class Parent {
    void parentMethod() throws IOException, SQLException {
        ...  
    }  
}  

class Child extends Parent {
    void parentMethod() throws IOException {
        ...  
    }  
}  
```  

오버라이딩의 예시를 살펴봅시다.  

```  
class Point {
    int x;  
    int y;  

    String getLocation() {
        return "x :" + x + ", y :" + y;
    }  
}  

class Point3D extends Point {
    int z;  
    
    String getLocation() {  // 오버라이딩  
        return "x :" + x + ", y :" + y + ", z :" + z;  
    }  
}  
```  

위의 예시를 보면 부모클래스의 메소드를 자식클래스에서 재정의하것을 볼 수 있는데, 이처럼 상황에 맞게 자식클래스에서 메소드를 재정의하는것을 오버라이딩이라고 한다.  

<br>  

---  

## 3. Overloading VS Overriding  

> **오버로딩(Overloading) : 기존에 없는 새로운 메소드를 정의하는 것(new)**  
> 
> **오버라이딩(Overriding) : 상속받은 메서드의 내용을 변경하는 것(change, modify)**  

오버로딩과 오버라이딩은 서로 혼동하기 쉽지만 사실 그 차이는 명백하다.  

마지막으로, 아래 코드를 보고 오버로딩과 오버라이딩을 쉽게 이해해봅시다.  

```  
class Parent {
    void parentMethod() {}  
}  

class Child extends Parent {
    void parentMethod() {}          // 오버라이딩    
    void parentMethod(int i) {}     // 오버로딩  

    void childMethod() {}  
    void childMethod(int i) {}      // 오버로딩  
    void childMethod() {}           // *에러, 중복정의 되었음    
}
```  
