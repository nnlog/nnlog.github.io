# Join  
- 두개의 테이블에 하나라도 같은 칼럼이 있어야 한다.
- 두 컬럼의 값은 공유 되어야 한다.
- 보통 조인을 위해서 기본 키(primary key)와 외래 키(foreign key)를 활용한다.  

---  

<br/>  

## 1. Inner Join  

<br/>  

![inner_join](https://user-images.githubusercontent.com/103972967/164183834-fb8a819d-bb2b-414f-bce8-3b0882d02207.PNG)  

<br/>  

 ![inner_join2](https://user-images.githubusercontent.com/103972967/164183896-caffe174-2b47-4a8e-9e92-7a51a7d7c234.PNG)  

<br/>  

> inner join  
> * 각 테이블에서 조인 조건에 일치되는 데이터만 가져온다.  
> * inner join은 '교집합' 이라고도 한다.  

---  

```
select * from sawon a
    inner join license b
;
```   
---  
  
<br/>  

## 2. Outer Join  

> Outer Join  
> * 조인 조건에 일치하는 데이터 및 일치자히 않은 데이터를 모두 select
> * join 조건에 일치하는 데이터가 없다면 **NULL**로 가져온다.  
> * Left Outer Join, Right Outer Join, Full Outer Join 등이 있다.  
  
<br/>  

### 2.1 Left Outer Join  

<br/>  

![left_outer_join](https://user-images.githubusercontent.com/103972967/164183982-06f97b3a-a516-483a-b2ba-bba23da63bd8.PNG)  

<br/>  

![left_outer_join2](https://user-images.githubusercontent.com/103972967/164184055-989ac579-71bc-47ed-a661-662c1267f16f.PNG)  

<br/>  

> Left Outer Join  
> * 왼쪽 테이블이 기준이 된다.  
> * 조인 조건에 부합하지만 데이터가 없다면 **NULL** select 된다.  

--- 

```
select * from sawon a  
    left outer join license b
;
```  

---

<br/>  

### 2.2 Light Outer Join  

<br/>  

![right_outer_join](https://user-images.githubusercontent.com/103972967/164184125-669972f5-1aff-48d1-9901-5336e7d148b5.PNG)  

<br/>  

 ![right_outer_join2](https://user-images.githubusercontent.com/103972967/164184181-3ede6309-15cb-4ba0-a6f0-e356ac02ff02.PNG)  

<br/>  

> Light Outer Join  
> * 오른쪽 테이블이 기준이 된다.  
> * 조인 조건에 부합하지만 데이터가 없다면 **NULL** select 된다.  

---  

```
select * from sawon a  
    right outer join license b  
;
```  

---  

<br/>  

## 3. Full Oter join  

> * 양쪽 테이블 모두 기준이 된다.  
> * 테이블 양쪽이 모두 기준이되기 때문에 많이 쓰이지 않는다. 
 
