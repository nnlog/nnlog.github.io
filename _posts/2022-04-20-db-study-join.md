# Join  
- 두개의 테이블에 하나라도 같은 칼럼이 있어야 한다.
- 두 컬럼의 값은 공유 되어야 한다.
- 보통 조인을 위해서 기본 키(primary key)와 외래 키(foreign key)를 활용한다.  

---  

<br/>  

## 1. Inner Join  

<br/>  

<a href="https://imgbb.com/"><img src="https://i.ibb.co/VHcySzM/inner-join.png" alt="inner-join" border="0"></a>  

<br/>  

<a href="https://ibb.co/9cp5Sp6"><img src="https://i.ibb.co/BcfMFfb/inner-join2.png" alt="inner-join2" border="0"></a>  

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

<a href="https://ibb.co/cx6VxK9"><img src="https://i.ibb.co/Tr4drDG/left-outer-join.png" alt="left-outer-join" border="0"></a>  

<br/>  

<a href="https://ibb.co/jRBzW8K"><img src="https://i.ibb.co/JQ0qycL/left-outer-join2.png" alt="left-outer-join2" border="0"></a>  

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

<a href="https://imgbb.com/"><img src="https://i.ibb.co/zmygpHm/right-outer-join.png" alt="right-outer-join" border="0"></a>  

<br/>  

<a href="https://ibb.co/j4CBccR"><img src="https://i.ibb.co/ryBTCCs/right-outer-join2.png" alt="right-outer-join2" border="0"></a>  

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
 