---  

layout: post  
title: "OAuth"  
image: other.jpg  
categories: All other  

---  

<br>  

> 차례  
> 
> 1. OAuth란 무엇인가?  
> 
> 2. OAuth의 구조  
> 
> 3. OAuth와 API의 차이  

<br>  

# **OAuth란 무엇인가?**  
<hr>  

> OAuth(Open Authorization)는 인터넷 사용자들이 비밀번호를 제공하지 않고 다른  
> 웹사이트 상의 자신들의 정보에 대해 웹사이트나 애플리케이션의 접근 권한을 부여할 수 있는  
> 공통적인 수단으로서 사용되는, 접근 위임을 위한 개방형 표준이다. -*위키백과*  

즉 OAuth란 사용자들이 접근 권한을 부여받아 해당 웹이나 앱에서 구현된 기능들을 이용할  
수 있도록 하는 공통적인 수단입니다. 그렇다면 이 기술은 어떻게 쓰이나 보면 요즘 여느 웹, 앱에서  
로그인 버튼만 클릭하면 여러 메이저 회사들의 로그인 기능을 구현한 페이지를 항상 봐왔을 것입니다.  

**OAuth 2.0은 1.0의 알려진 보안 문제 등을 개선한 버전*

<br>  

![login](https://user-images.githubusercontent.com/56240505/125554097-e3b5f9ff-0cda-4328-a673-03b817166aa2.png)  

<br>  

사진을 예로 들면, 외부 어플리케이션(원티드)은 사용자 인증을 위해 여러 타 업체(Facebook, Apple 등)의 사용자 인증 방식을 사용합니다. 이 때, OAuth를 통해 제 3자 서비스(원티드)는 외부서비스(Facebook, Apple 등)의 특정 자원을 접근 및 사용할 수 있는 권한을 인가 받게 됩니다.  

그만큼 어느 기술보다 사용자들의 편리함을 보다 쉽게 올릴 수 있는 기능인 셈이다.  
하지만 그만큼 믿을만한 사이트가 아닌이상 개인정보 유출 위함도도 따른다. 

<br>  

# **OAuth의 구조**  
<hr>  

![OAuth 구조](https://img1.daumcdn.net/thumb/R1280x0/?scode=mtistory2&fname=https%3A%2F%2Fblog.kakaocdn.net%2Fdn%2FlSmVN%2Fbtq9f5MFUBD%2FBei9NUSJU4983Ck9ysTdF1%2Fimg.png)  

<br>  

|역할|설명|  
|:--:|:--:|  
|자원 소유자(Resource Owner)|보호 자원에 접근 권한을 부여할 수 있는 개체(일반적으로 서비스 이용자)|  
|자원 서버(Resource Server)|보호 자원에 대한 서비스 API를 제공하는 서버 <br> 예) 예급 조회, 이체, 결제, 주문 등|  
|권한 서버(Authorization Server)|자원 접근 권한을 위임 및 관리하는 서버|  
|클라이언트(Client)|자원 서버에서 보호 자원을 요청하고 관련 서비스를 제공하는 애플리케이션 <br>예) 금융 오픈 API를 사용하여 금융 서비스를 제공하는 핀테크 앱|  
|접근 토큰(Access Token)|자원에 대한 접근 권한을 자원 소유자가 **인가**하였음을 나타내는 자격증명|  

> 인가(Authorization)  
> 
> 인증(Authentication)과는 달리 접근 권한을 관리하는 의미로 사용자에게 접근 권한을 부여하는 프로세스를 말한다.  
> 
> 대표적으로, 서버에서 특정 파일을 다운로드할 수 있는 권한을 부여하거나, 개별 사용자에게 관리자 권한으로 애플리케이션에 엑세스할 수 있는 권한을 부여하는 경우가 여기에 해당한다.  

<br>  

대략 OAuth의 구조는 이렇다. 크게 사용자, 클라이언트, 인가 서버, 자원 서버로 나뉘고  
사용자가 입력한 자원 서버 아이디와 비밀번호를 통해 자원 서버(페이스북, 구글, 네이버 등)로부터 접근 권한을 얻는 방식이다.  

이때, 접근 토큰(Access Token)은 클라이언트에서 저장하고 관리한다.

<br>  

# **API**  
<hr>  

> API  
> 
> API(application programming interface 애플리케이션 프로그래밍 인터페이스, 응용 프로그램 프로그래밍 인터페이스)는 컴퓨터나 컴퓨터 프로그램 사이의 연결이다. 일종의 소프트웨어 인터페이스이며 다른 종류의 소프트웨어에 서비스를 제공한다. 이러한 연결이나 인터페이스를 빌드하거나 사용하는 방법을 기술하는 문서나 표준은 API 사양으로 부른다. 이 표준을 충족하는 컴퓨터 시스템은 API가 구현(implement)되었다거나 노출(expose)되었다고 말한다. API라는 용어는 사양이나 구현체를 의미할 수 있다. -*위키백과*  

<br>  

API는 보시다시피 프로그램간의 연결다리와 같다. 인가되어진 사용자가 클라이언트서버에서 리소스 서버(Facebook, Apple 등)의  
서비스를 간편하게 이용할 수 있도록 리소스 서버에서 만든 프로그램 인터페이스이다. 이를 오픈 API라고도 한다.  

<br>  

![payco인증방식](https://developers.payco.com/static/img/@img_guide2.jpg)  

페이코에서 사용하는 OAuth 프로세스를 보면 한눈에 이해하기 쉽다.  

<br>  

# **OAuth의 종류**  
<hr>  

OAuth 2.0의 종류는 총 4가지로 분류된다.  

* Authorization Code Grant  
* Implicit Grant  
* Resource Owner Password Credentials Grant  
* Client Credentials Grant  

<br>  

## Authorization Code Grant  

* 서버 사이드 코드로 인증하는 방식  
* 권한 서버가 클라이언트와 리소스서버간의 중재 역할  
* Access Token을 바로 클라이언트로 전달하지 않아 잠재적 유출을 방지  
* 로그인시 페이지 URL에 response_type=code 라고 넘긴다.  

<br>  

## Implicit Grant  

* token과 scope에 대한 스펙 등은 다르지만 OAuth 1.0a과 가장 비슷한 인증 방식  
* Public Client인 브라우저 기반의 어플리케이션(Javascript application)이나 모바일 어플리케이션에서 이 방식을 사용하면 된다.  
* **OAuth 2.0에서 가장 많이 사용되는 방식이다.**  
* 권한코드 없이 바로 발급되서 보안에 취약  
* 주로 Read only인 서비스에 사용  
* 로그인시에 페이지 URL에 response_type=token 라고 넘긴다.  

<br>  

## Resource Owner Password Credentials Grant  

* Client에 아이디/패스워드를 저장해 놓고 아이디/패스워드로 직접 access token을 받아오는 방식이다.  
* Client 를 믿을 수 없을 때에는 사용하기에 위험하기 때문에 API 서비스의 공식 어플리케이션이나 믿을 수 있는 Client에 한해서만 사용하는 것을 추천한다.  
* 로그인시에 API에 POST로 grant_type=password 라고 넘긴다.  

<br>  

## Client Credentials Grant  

* 어플리케이션이 Confidential Client일 때 id와 secret을 가지고 인증하는 방식이다.  
* 로그인시에 API에 POST로 grant_type=client_credentials 라고 넘긴다.  

<br>  

# Token  
<hr>  

## Aceess Token  

앞서 말한 4가지 권한 요청 방식 모두, 요청 절차를 정상적으로 마치면 클라이언트에게 Access Token이 발급됩니다. 이 토큰은 보호된 리소스에 접근할 때 권한 확인용으로 사용됩니다. 문자열 형태이며 클라이언트에 발급된 권한을 대변하게 됩니다.  

계정 아이디와 비밀번호 등 계정 인증에 필요한 형태들을 이 토큰 하나로 표현함으로써, 리소스 서버는 여러 가지 인증 방식에 각각 대응 하지 않아도 권한을 확인 할 수 있게 됩니다.  

<br>  

## Refresh Token  

한번 발급받은 Access Token 은 사용할 수 있는 시간이 제한되어 있습니다. 사용하고 있던 Access Token 이 유효기간 종료 등으로 만료되면, 새로운 액세스 토큰을 얻어야 하는데 그때 이 Refresh Token 이 활용됩니다.  

권한 서버가 Access Token 을 발급해주는 시점에 Refresh Token 도 함께 발급하여 클라이언트에게 알려주기 때문에, 전용 발급 절차 없이 Refresh Token을 미리 가지고 있을 수 있습니다. 토큰의 형태는 Access Token과 동일하게 문자열 형태입니다. 단 권한 서버에서만 활용되며 리소스 서버에는 전송되지 않습니다.


