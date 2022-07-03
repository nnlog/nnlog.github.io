---  
layout: post
title:  "M1 MAC install MySql"
image: mysql.png
categories: All apple db  
---  

# M1 맥북 데이터베이스 사용하기  
<hr>  

> 차례  
> 1. MySql 설치  
>
> 2. MySql 보안 적용 명령어  
>
> 3. MySql 기본 실행 및 종료  
>
> 4. 에러  

<br>  

지난번 Oracle Cloud를 이용한 데이터베이스 사용을 해보았는데 이번엔 스터디에서 사용하기로 한 MySql을 설치해볼까 한다.  
모든 데이터베이스의 역할은 똑같지만 이렇게 상황별(프로젝트, 회사 등등)로 써야할 데이터베이스는 여러가지이다. 때문에 이렇게 MySql 설치 과정을 기록해본다.  

항상 느끼지만 이런 프로그램을 다운받을 때 homebrew통한 설치는 아주 간단하다.  

그러니 미리 homebrew를 설치하고 진행해보도록 한다.  

<br>  
<br>  

# MySql 설치  
<hr>  

`brew install mysql`  

위 명령어를 터미널에 입력하면 homebrew가 아래와 같이 파일들을 설치한다.  

<br>  

![mysql 설치](https://user-images.githubusercontent.com/103972967/177037446-968f5a1e-91f2-49b5-9c7e-c910782f7304.png)  

<br>  

그리고 아래와 같이 mysql 문구가 떳다면 정상적으로 설치가 완료된 것이다.  

<br>  

![mysql 설치2](https://user-images.githubusercontent.com/103972967/177037448-41085e8d-0b9a-48a2-80c4-73f5f279b005.png)  

<br>  
<br>  

# MySql 보안 적용 명령어 입력  
<hr>  

`mysql_secure_installation`  

설치 완료 후 위에서 보여지는 것과 같이 보안 적용 명령어를 실행하라는 문구도 볼 수 있다.  

명령어를 실행하면,  

<br>  

![mysql 보안 설정](https://user-images.githubusercontent.com/103972967/177037473-3fe1a499-55ab-47cc-aa55-629995f79d23.png)  

<br>  


**참고 사항**  

* 비밀 번호 설정시 보안강도 선택  

0 = low : 8글자 이상의 문자  

1 = medium : 8글자 이상의 문자(숫자, 대/소문자 혼용 및 특수문자 포함)  

2 = strong : 8글자 이상의 문자(숫자, 대/소문자, 특수문자 그리고 사전파일 포함)  

* New password부분에 mysql 실행시 사용하실 비밀번호 입력을 하면 됩니다.  

위에서 선택한 보안강도를 참고하여 설정하면 이상없이 설정 됩니다.  

<br>  

위 사진에서 빨간 네모칸에서 보이는 것과 같이 질문은 사용자에 맞게  
설정하면 되고(딱히 설정할거 없을 시에는 모두 Yes) 참고 사항을 보고 입력하면 됩니다.  

마지막으로 `All done!`이라는 명령어가 뜨면 성공적으로 설정 완료한 것입니다.  

<br>  
<br>  

# MySql 기본 실행 및 종료  
<hr>  

<br>  

![mysql 실행](https://user-images.githubusercontent.com/103972967/177037495-ecc15f1a-14e5-4295-ad0f-7230e730ac2f.png)  

<br>  

### MySql 서버 실행  

```  
mysql.server start // 서버 켜기  
mysql -uroot -p비밀번호 // 비밀번호 입력 후 접속  
```  

### 종료  

```  
mysql> \q // mysql 나가기  
mysql.sever stop // 서버 종료
```  

<br>  

### MySql을 데몬으로 실행하기  

> 데몬(Daemon)  
> 운영체제의 백그라운드 상태에서 계속 실행되는 프로그램  

```  
brew services start mysql  
mysql -u root -p 비밀번호  
```  

### 종료  

```  
mysql> \q
brew services stop mysql  
```  

<br>  

### 데몬으로 실행되는 프로그램 목록 확인  

`brew services list`  

### 서비스 재시작  

`brew services start mysql`  

<br>  
<br>  

# 에러  
<hr>  

정상적으로 mysql이 설치된 후에  
보안 적용 명령어 `mysql_secure_installation`를 실행시켰지만 에러가 발생한다.  

<br>  

![error](https://user-images.githubusercontent.com/103972967/177037468-dcbd6ead-ad48-4ad4-8b2e-6623c6ff215e.png)  

<br>  

이 문제는 현재 MySql과 연결이 되지 않고 있는 문제이기 때문에  
MySql을 데몬으로 실행시키는 명령어 `brew services start mysql`를 실행한 후 정상 작동하는 것을 확인하였다.  




  



