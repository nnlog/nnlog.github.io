---  

layout: post  
title: "jsp study about Tag"  
image: jspstudy.jpg  
categories: All jsp  

---  

<br>  

# **디렉티브 태그**  
<hr>  

디렉티브 태그란 현재 JSP페이지의 특정 영역에 외부 파일의 내용을 포함시키는 태그이다.  

보통 header와 footer 대부분의 페이지에 동일한 내용으로 작성되기 때문에  
유지보수 및 편의를 위하여 외부 파일로 만든 후 include하여 사용한다.  

`<%@ include file="파일명" %>`

<br>  

# **액션 태그**  
<hr>  

JSP페이지에서 동일한 내용이라도 자바 코드를 기술하기 보다는 태그를 기술하는 것이 지저분하지  
않고 깔끔하게 코딩할 수 있어, 가독성 높은 소스코드를 작성할 수 있다. 또한 코드 양을 대폭 줄일 수 있다.  

페이지와 페이지 사이를 제어하거나 다른 페이지의 실행 결과 내용을 현재 페이지에 포함하거나  
자바빈즈(객체)등의 다양한 기능을 제공한다.  

액션 태그는 XML문법을 따른다. 즉, 시작 태그와 함께 반드시 종료 태그를 포함해야 한다.  

**기본 형태** : `<jsp: 속성="값">내용</jsp: 속성="값">`  

**내용이 없는 액션 태그의 형식** : `<jsp: 속성="값"/>`  

<br>  

## 종류  

* forward(<jsp:forward.../>)  
다른 페이지로의 이동, 페이지 흐름 제어  

* include(<jsp:include.../>)  
외부 페이지의 내용을 포함하거나 페이지 모듈화  

* param(<jsp:useBean.../>)  
현재 페이지에서 다른 페이지에 정보를 전달할 때 사용  

* useBean(<jsp:useBean.../>)  
빈(Bean)을 생성하고 사용하기 위한 환경을 정의하는 액션 태그  

* setProperty(<jsp:setProperty.../>)  
빈에서 속성 값을 할당  

* getProperty(<jsp:getProperty.../>)  
빈에서 속성 값을 얻어올 때 사용  

<br>  

# **페이지 이동**  
<hr>  

jsp를 이용하면 보다 수월한 동적 웹 페이지를 만들기 위해 페이지에서 페이지로 이동하는 경우를 계속 마주친다.  

그렇기 때문에 상황(페이지에서 보내야하는 정보)에 맞게 필요한 방식으로 쓸 수 있어야 한다.     

<br>  

## Forward  

forward 방식은 웹 브라우저에서 넘어온 request(요청)에 따른 페이지에서  
또 다른 페이지로 이동하여 결과값을 리턴할 때 사용된다.  

또한 forward는 한번 받아온 변수를 페이지 이동간에 계속해서  
사용된다. 특히 DB와 연결하여 사용할 때 테이블 조회 하여 정보를 가져올 때 탁월하다.  

*사진을 보면 forward의 기능에 대해서 이해하기 쉽다.*  

<br>  

![forward](https://user-images.githubusercontent.com/103972967/175481438-d9c73a79-98db-40ea-9285-1028607d6217.PNG)  

<br>  

**forward 특징**  

1. Request에 담긴 값이 유효하다. (이는 계속해서 패이지간의 이동을 통해 웹페이지에서 받아온 요청을 수행하기 때문에 가능한 특징이다. 그렇기 때문에 request, response가 유지된다.)  

2. 이동된 url이 화면에 안보인다. (사용자가 이동했는지 알 수 없다.)  

**사용 방법**  

1. `<jsp:forward page="이동할 페이지"/>` : 액션 태그 사용  

2. pageContext.forward("이동할 페이지"); : 내장 객체 사용  

<br>  

## Redirect  

반대로 redirect는 웹 페이지에서 받아온 요청에 따른 페이지에서  
이동 없이 웹 페이지를 들려 다른 요청을 수행한다.  

그렇기 때문에 페이지에서 가져오는 변수 값이 유지될 필요가 없는데  
이러한 특징은 차후에 DB와 연결하였을 때 테이블 생성, 삭제 및 수정할 때 사용된다.  

<br>  

![redirect](https://user-images.githubusercontent.com/103972967/175481446-64e3a5da-e0c2-4d82-bf9d-f3e431d5845a.PNG)  

<br>  

**특징**  

1. 클라이언트가 새로 페이지를 요청한 것과 같은 방식으로 페이지가 이동된다. (request, response가 유지되지 않고 새로 만들어진다.)  

2. 이동된 url이 화면에 보인다.  

**사용 방법**  

1. response.sendRedirect(""이동할 페이지);  

<br>  

## ATTRIBUTE SCOPE  

* page : 페이지 내에서 지역 변수처럼 사용  

* request : http 요청을 was가 받아서 웹 브라우저에게 응답할 때까지 변수가 유지되는 경우 사용  

* session : 웹 브라우저 별로 변수가 관리되는 경우 사용  

* application : 웹 어플리케이션이 시작되고 종료될 때까지 변수가 유지되는 경우 사용  

<br>  

> **관련 메서드**  
> 
> `setAttribute(String name, Objext value);`  
> 이름이 name인 속성의 값을 value로 저장한다.  
> 
> `getAttribute(String name);`  
> 이름이 name인 속성의 value를 구한다. 존재하지 않을 경우 null을 반환한다.  
> 
> `removeAttribute(String name);`  
> 이름이 name인 속성을 삭제한다.  








