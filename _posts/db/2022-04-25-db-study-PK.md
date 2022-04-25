---  

layout: post  
title: "DB study about PK adn FK"  
image: study.jpg  
categories: All db  

---  

# DB study about PK and FK  

DB PK(primary key)와 FK(foreign key)에 대하여 정리해본다.  

<br/>  

## 1. PK(Primary Key)  

> **PK ?**  
> 
> * 주 키 또는 프라이머리 키라고 하며, 관계형 데이터베이스에서 조의 식별자로 이용하기에 가장 적합한 것을 관계(태이블)마다 한 설게자의 의해 선택, 정의된 후보 키를 말한다.  
> 
> * 테이블당 하나만 정의 가능하다. (두 개 이상의 PK는 조합 키/ 복합 키라고 불린다.)  
> 
> * PK는 NOT NULL + UNIQUE의 기능을 가지고 있다.  
> 
> * 자동으로 INDEX가 생성이 되는데 이는 검색 키로서 검색 속도를 향상시킨다.  

### 1.1 선언 방법  

```  
create table testtable(
    col1    varchar2(10)    primary key,
    col2    varchar2(10)    constraint pk이름 primary key,
    col3    varchar2(10)    ,
    constraint pk이름 primary key(col3)
);
```  

<br/>  

## 2. FK(Foreign Key)  

> **FK ?**  
> 
> * 외부 키, 외래 키, 참조 키, 외부식별자, FK로 불린다.  
> 
> * FK가 정의된 테이블은 자식 테이블이라 칭한다.  
> 
> * 참조되는 테이블, 즉 PK가 있는 테이블이 부모 테이블이다.  
> 
> * 부모 테이블의 PK 칼럼에 존재하는 데이터만 자식 테이블에 입력할 수 있다.  
> 
> * 부모 테이블은 자식의 데이터나 테이블이 삭제된다고 영향을 받지 않는다.  
> 
> * 참조하는 데이터 칼럼과 데이터 타입이 반드시 일치 해야 한다.  

### 2.1 선언 방법  

**테이블 생성과 함께 선언할 시**  

```  
create table pTable(
    pPK number(10) primary key  
);  

create table cTable(
    pPK     number(10),
    Col1    varchar2(10),  
    constraints fk_code foreign key(pPK)  
        references pTable(pPK) on delete cascade
)  
```  

---  

```  
contraints [제약 조건 명] foreign key([컬럼명])
    references [참조할 테이블 이름]([참조할 컬럼])
    [ on delete cascade || on delete set null ]
```  

**테이블 생성 후 설정**  

```  
alter table [테이블 이름]
add constraints [외래키 이름] foreign key( [참조 컬럼] )
references [참조 테이블 이름]( [참조 컬럼] )  
```  

### 2.2 외래 키 삭제  

1. **on delete cascade** : 참조되는 부모 테이블의 행에 대한 delete를 허용한다. 즉, 참조되는 부모 테이블 값이 삭제되면 자식 테이블 값 역시 **삭제**된다.  

2. **on delete set null** : 참조되는 부모 테이블의 행에 대한 delete를 허용한다. cascade와 다르게 부모 값이 삭제되면 해당 참조하는 자식 테이블의 값들은 **NULL**값으로 설정된다.




