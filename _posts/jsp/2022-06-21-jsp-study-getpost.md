---  

layout: post  
title: "jsp study about GET/POST"  
image: jspstudy.jpg  
categories: All jsp  

---  

# GET/POST  

<br>  

> **GET 방식**  
> 
> * 서블릿에 데이터를 전송할 때 URL뒤에 key=value 형태로 전송  
> 
> * 보안에 취약  
> 
> * 전송 가능한 데이터 최대 255자  
> 
> * 기본 전송 방식으로 사용이 쉬움  
> 
> * 웹 브라우저에서 직접 입력하여 전송 가능  
> 
> * 여러 개의 데이터를 전송할 때 '&'로 구분해서 전송  

<br>  

> **POST 방식**  
> 
> * 서블릿에 데이터를 전송할 때 TCP/IP프로토콜 데아터의 HEAD 영역에 숨겨진 채 전송  
> 
> * 보안에 유리  
> 
> * 전송 데이터 용량 무제한  
> 
> * 전송 시 서블릿에서 또 다시 가져오는 작업이 필요하므로 GET방식보다 처리 속도가 느림  

<br>  
<hr>  
<br>  

## 예시  

<br>  

### GET `www.localhost8080/index.jsp?name=자바&age=20`  

여기서 ? 뒤에 오는 name, age가 각각 key가 되고 자바, 20이 그에 맞는 value값이 된다.  

이 값은 서블릿에 데이터를 전송하고 받아올 떄 reqeust.getParameter("name"), request.getParameter("age")로 받아올 수 있다.  

<br>  

### POST `www.localhost8080/index.jsp`  

이와 같이 POST는 데이터를 전송할때 숨겨서 보내기에 보안에 유리하다.  

그렇지만 이 방법도 개발자도구로 요쳥 내용을 볼 수 있기 때문에 아주 중요한 정보는 암호화가 필요하다.  