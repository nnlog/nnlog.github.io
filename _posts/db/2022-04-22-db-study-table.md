---  

layout: post  
title: "DB study about table"  
image: study.jpg  
categories: All db  

---  

# TABLE  

DB table을 관리하는 쿼리에 대하여 간단하게 정리해보려한다.  

## 1. DML(Data Manipulation Language)  

> DML ?  
> 
> 데이터베이스 사용자 또는 응용 프로그램 소프트웨어가 컴퓨터 데이터 베이스 대해 데이터 **검색**, **등록**, **삭제**, **수정**을 위한, *데이터베이스 언어* 또는 *데이터베이스 언어 요소*이다.  
> 
>> 종류 ?  
>> * SELECT   
>> * INSERT  
>> * UPDATE  
>> * DELETE  

<br/>  

### 1.1 SELECT  

---
```  
WHERE    : 어떤 열을 불러올 지를 지정
GROUP BY : 연산 함수가 각 그룹에 적용되게 하도록 속성을 그룹 열에 공유하는 것
HAVING   : GROUP BY 절에서 정의된 그룹 중에서 검색
ORDER BY : 반환하는 열의 정렬 순서를 지정
```  
---  

> * select문은 하나 또는 그 이상의 테이블에서 데이터를 **추출**하는 SQL의 데이터 조작언어(DML) 중 하나이다.  

---  
```
EX)  

SELECT empno, ename
FROM   emp
WHERE  empno IN (7900, 7934);  
```  
---

<br/>  

### 1.2 INSERT  

---  
```
INSERT INTO 테이블_또는_뷰_이름 (컬럼1, [컬럼2, ...]) 
VALUES (값1, [값2, ...]);
```   
---  

---  
```  
INSERT INTO 테이블_또는_뷰_이름 
VALUES (값1, [값2, ...]);
```  
---  

<모든 컬럼에 값을 등록할 때, 대상 컬럼명을 생략할 수 있다.>  

> * insert문은 테이블의 데이터를 **추가**하는 기능을 한다.  
>   
> * 컬럼의 순서와 값의 순서가 같아야 해당 컬럼으로 데이터가 추가된다.  

---  
```  
EX)  

INSERT INTO emp (empno, ename)
VALUES (7369, '박지성');
```  
---  

<br/>  

### 1.3 UPDATE  

---  
```  
UPDATE table_name 
SET    column_name = value 
    [, column_name = value]
    [, ...]
[WHERE condition]
```  
---  

> * update문은 구조화 질의어 중 하나로, 테이블이나 뷰에서 한 개 이상의 행을 **바꾸는** 기능을 한다.  

---  
```  
EX)  

UPDATE emp
SET    salary = 2500000
WHERE  ename  = '손흥민';
```  
---  

<br/>  

### 1.4 DELETE  

---  
```  
DELETE [FROM]table_name 
[WHERE conditions];
```  
---  

> * delete문은 테이블 또는 뷰에서 한 개 이상의 행을 **삭제**한다.  

---  
```  
EX)  

DELETE FROM emp 
WHERE  ename = '손흥민';
```  
---  

<br/>  

## 2. DDL(Data Definition Language)  

> DDL ?  
> 
> 데이터베이스를 정의하는 언어를 말하며 데이터를 **생성**하거나, **수정**, **삭제** 등 데이터의 전체 골격을 결정하는 역할의 언어이다.  
> 
>> 종류 ?  
>> * CREATE  
>> * ALTER  
>> * DROP  
>> * TRUNCATE  

<br/>  

### 2.1 CREATE  

---  
```  
CREATE TABLE table_name (

    column_name1 데이터타입(크기) [DEFAULT value],
    column_name2 데이터타입(크기) [DEFAULT value],
    ...
);
```  
---  

> * create table, create seuquence, create index, create view 등과 같이 객체를 **생성**하는데 사용한다.  
> 
> * 테이블 명은 다른 테이블의 이름과 중복될 수 없다.  
> 
> * 한 테이블 내에서 컬럼명은 중복될 수 없다.  
> 
> * 테이블 명은 영문자로 시작해야 한다.  
> 
> * 내장 키워드는 테이블 명 또는 컬럼 명으로 사용할 수 없다.
>   
> * 이외에 constraints(제약조건), sequence, index등과 함께 쓰인다.

<br/>  

### 2.2 ALTER  

---  
```
ALTER TABLE table_name 
    ADD (컬럼1 데이터타입(크기) [제약조건], 컬럼2 데이터타입(크기)...);
```  
---  

> * alter table, alter sequence, alter index, alter view등과 같이 객체를 **변경**하는데 사용한다.  
> 
> * 이외에 add, modify, rename등과 함께 쓰인다.

<br/>  

### 2.3 DROP  

---  
```  
DROP TABLE table_name;
DROP SEQUENCE sequence_name;
DROP INDEX index_name;
DROP VIEW view_name;
```  
---  

> * drop tabel, drop sequence, drop index, drop view등과 같이 객체를 **삭제**하는데 사용한다.  

<br/>  

### 2.4 TRUNCATE  

---  
```  
TRUNCATE TABLE table_name;
```  
---  

> * 테이블에서 영구적으로 모든 행을 삭제할 때 이 구문을 사용한다.  
> 
> * 롤백되지 않기에 매우 위험한 키워드이다.  

