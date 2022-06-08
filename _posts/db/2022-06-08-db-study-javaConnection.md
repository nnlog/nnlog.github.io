---  

layout: post  
title: "DB study about java Connection"  
image: study.jpg  
categories: All db apple java 

---  

# 맥북 m1 DB와 java 연결하기  

<br>  

중요한 정보의 창고 역할을 하는 DB는 표를 만들고 정보를 입력하여 넣을 수 있는데,  
이렇게 정리된 표를 프론트단으로 가져오기 위해서는 java project와 DB를 연결 할 수 있어야 한다.  

<br>  

자바에서 간단하게 Connection이라는 클래스를 통해 DB의 주소를 입력받아 연결할 수 있는데 오늘은 그 방법을 기록하여 다음번에는 헤매지 않게 하려고 한다.  

<br>  

맥북에서나 윈도우에서나 DB의 주소와 사용자 이름만 다를뿐 연결하는 방식은 비슷하니 참고 바란다.  

<br>  

---  

<br>  

## DBConnection.java 생성  

<br>  

우선 eclipse dynamic web project안에 java 또는 src/main/java (버전에 따라 다름)에 DBConnection이라는 클래스를 생성해 준다. 매번 프로젝트에서 DB를 연결하는것은 골치 아프기 때문에 따로 만들어서 사용하는게 유지보수에 확실히 좋다.  

<br>  

전체적인 코드를 먼저 사진으로 보자.  

![DBConnection.java](https://user-images.githubusercontent.com/103972967/172570745-6d0cea9c-2e25-4c67-b946-d127e3809c7e.png)  

프로젝트를 생성하여 그때마다 연결할 Connection을 위해 getConnection()메서드를 생성 후 그 일련의 과정 중 필요한 정보들을 선언한다.  

<br>  

> driver    = "현재 사용중인 드라이버 이름"  
> 
> url       = "jdbc:oracle:thin:@WALLET이름_medium?TNS_ADMIN=WALLET주소"  
> 
> user      = "유저 이름"  
> 
> password  = "DB에 사용중인 비밀번호"  

<br>  

**맥북에 M1칩을 사용중인 분들은 오라클이 제공이 되지 않기 때문에 무조건적으로 오라클 클라우드에서 ATP생성 후 지갑을 통해 연결하였을 것이기 때문에 위에서 나온**  

user = **"ADMIN"**으로 동일 하다.  

<br>  

위 정보는 현재 디비버로 연결해놓았을때 기준으로 EditConnection을 들어가 보면 알 수 있다.  

![DBConnection.java02](https://user-images.githubusercontent.com/103972967/172570836-e9b7f32a-2ddb-4b4b-a90b-430f4e4571c5.png)

<br>  

그 다음은 Class.forName으로 driver주소를 넘겨주고 Connection객체로 생성한 con에  
DriverManager를 통해 위에서 입력 해놓은 url, user, password를 넘겨준다.  

그 후 con을 리턴해줌으로써 getConnection()메서드가 종료된다.  

<br>  

---  

<br>  

## jdbcTest.jsp 생성  

<br>  

DBConnection.java를 연결하고자 하는 디비와 정보를 일치하게 입력하였다면 끝이라고 봐도 무방하다. jdbcTest.jsp는 위에서 연결을 시도했던 메서드가 정상적으로 작동 하였는지 확인 하기 위해서 테스트겸 만드는 것이기 때문에 아주 간단하다.  

<br>  

![jdbcTest.jsp](https://user-images.githubusercontent.com/103972967/172572616-e660dac7-795a-41e9-8ad7-e5279dc5b357.png)  

우선 새로운 jsp에 새로운 Connection con을 생성하여 미리 만들어 놓았던 DBConnection 클래스를 선언해주면 된다.  

이렇게 선언된 상태에서 `if(con == null) -> result = "failed"`를 통해 확인 절차를 밟을 수 있는데 만약 DBConnection 클래스에서 연결이 성공적으로 되지 않는다면 con에는 담겨져 있는 객체가 없기 때문에 null 상태가 되기에 이점을 이용한 것이다.  

<br>  

---  

<br>  

## 결과  

<br>  

입력된 정보가 모두 일치하여 연결에 **성공** 하였다면,  

![result1](https://user-images.githubusercontent.com/103972967/172573728-28341c87-a2ff-417c-8b64-036c0ac03823.png)  

<br>  

**실패**하였다면,  

![result2](https://user-images.githubusercontent.com/103972967/172573734-96141e5e-d904-4b3d-a4da-570e66ea9248.png)  

이렇게 결과 값을 확인할 수 있다.

