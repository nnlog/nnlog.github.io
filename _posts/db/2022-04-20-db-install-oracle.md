---  
published: true
layout: post
title:  "M1 MAC install Oracle(for dbeaver)"
image: m1.jpg
categories: All apple db  
---  

# M1 맥북 데이터베이스 사용하기  

> 1. Oracle JDBC Driver  
> 2. Oracle 전자지갑 만들기  
> 3. DB 접속 툴(editor)  
  
현재 나는 M1 맥북을 이용하여 국비수업을 듣고있다.   
국비수업을 듣는 사람들 또한 나처럼 당황할게 분명해 이렇게 글을 쓰게 되었다.   
  
현재 M1 맥북으로는 docker를 통해서도 데이터베이스를 쓸 수 없는걸로 알고있다.  그 이유는 Oracle DB가 공식적으로 M1을 지원하지 않는다고 선언하였기 때문이다. 그래서 M1을 가지신 분들은 데이터베이스를 이용하기 위해서 저 위에 3가지 도구를 통해 대신할 수 있다.   

---  

## 1. Oracle JDBC Driver 다운  

Oracle JDBC 공식 홈페이지에 접속한 뒤, **19c버전**을 다운받는다.  
그 이유는 뒤에 Oracle 전자지갑 버전이 **19c**이기에 버전을 맞추기 위함이다.  

---  

## 2. Oracle 전자지갑 다운
먼저 전자지갑을 다운받기 위해서는 **Oracle Cloud**에 회원가입을 해야한다.  
회원가입 중간에 신용카드를 등록하라는 단계가 있는데 어차피 무료범위에서만 쓸거기 때문에 걱정안하고 등록해도 된다.  

로그인을 하면 가장 먼저 홈에 여러가지 이용가능 툴들이 보이는데  
이중에서 `ATP 데이터베이스 생성`을 클릭하여 진행해 볼거다.  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F25bbe4a9-2c16-4b0a-b6d5-a33627139fdf%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-30%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%2012.35.30.png)   

<br/>  

---  

### 자율운영 데이터베이스 생성. 

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F90d31c00-d96f-482b-99bb-f1be6ca35379%2FOracle%20Cloud%20Infrastructure%20%E1%84%87%E1%85%A9%E1%86%A8%E1%84%89%E1%85%A1%E1%84%87%E1%85%A9%E1%86%AB.png)  

<br/>  

체크 부분 잘 맞추어 `데이터베이스 생성`버튼 클릭해주면 된다.  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F7b03f03e-daec-4274-89ec-2368b97b5709%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-29%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%203.08.09.png)  

<br/>  

이렇게 `🟢사용가능`이라고 뜬다면 성공적으로 생성된것이다.  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F0fc4e562-c42b-425f-885e-f16e2ae1e070%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-30%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%2012.57.15.png)  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F9e9b97de-93ec-46e7-ba42-08745c4e39b8%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-30%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%202.41.03.png)  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2Fb9a8b000-f3d7-41d5-b033-58a915654a2a%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-30%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%202.43.11.png)  

<br/>  

순서대로 진행한 다음에,  
전자지갑 비밀번호를 새로 생성해주면 된다.  

---  

## 3. DBeaver 설치 및 연결

`brew install --cask dbeaver-community`  

본 명령어를 통해서 간편하게 설치해준다.  
(*만일 노트북에 homebrew가 설치 되어 있지 않을 때는 홈페이지에서 다운로드한다.)  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2Ff47cd739-ebc6-4747-8bb7-6c9d60a9bf44%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-30%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%203.33.15.png)  

<br/>  

순서대로 **Oracle** -> `다음`클릭  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F3d2704c1-8e08-46d7-89b2-acc0dfa91dc4%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-29%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.38.17.png)  

<br/>  

### 1. Connection type을 Custom으로 변경  

### 2. JDBC URL Template을 아래와 같이 삽입  

`jdbc:oracle:thin:@데이터베이스 이름_medium?TNS_ADMIN=/전자지갑경로/Wallet_데이터베이스 이름/`

* **데이터베이스 이름**은 처음에 설정했던 이름으로 오라클 클라우드 사이트에서 확인할 수 있다.  
* **전자지갑경로**는 전자지갑을 저장한 위치이다.  
  경로를 알고자 하면, 전자지갑 파일을 복사한뒤 `terminal` 및 `iterm`에 붙여넣기 하면 경로가 뜬다.

### 3. Username/Password 입력  

* ATP 데이터베이스 만들면서 설정한 관리자 아이디와 비밀번호  
  Username = ADMIN  
  Password = 설정한 비밀번호  

### 4. Edit Driver Setting 클릭  

### 5. Default Port 확인 및 설정  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F37e8b03f-b8cf-422b-88b7-81fb9e9c04cf%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-29%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.50.23.png)  

<br/>  

* 전자지갑 속 `tnsnames.ora`파일을 열기  
* `(port=1522)`확인 후 변경  

### 6. OJDBC UPLOAD (.jar 파일 전부)  

<br/>  

![image desciption](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2Ff13fbc0c-ea76-4a1e-acec-2e32effe456f%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-29%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%204.51.50.png)  

<br/>  

이제 아까 처음에 받아놓았던 Oracle JDBC Driver를 열고  
폴더 안에 있는 `.jar`파일들을 전부 복사하여 붙여넣어준다.  

(*주의 : 처음 Libraries에 들어있는 파일을 전부 지운 후에 jar파일들을 붙여넣기 해야한다.)  

<br/>  

![image description](https://velog.velcdn.com/images%2Fejayjeon%2Fpost%2F848e6699-0cb1-49b3-8fc5-f36e5b713601%2F%E1%84%89%E1%85%B3%E1%84%8F%E1%85%B3%E1%84%85%E1%85%B5%E1%86%AB%E1%84%89%E1%85%A3%E1%86%BA%202021-09-29%20%E1%84%8B%E1%85%A9%E1%84%92%E1%85%AE%205.06.25.png)  

<br/>  

* 파일 모두 추가 후, `Find Class`버튼 클릭
* `Driver Class`생성 확인 후, 확인버튼 클릭  

### 7. Test Connection 클릭  

이 과정이 한번에 성공한다면 아주 좋겠지만 나도 그렇고 처음엔 실패투성이다.  
그래도 성공한케이스를 업로드해놓고 나중에 세팅할일 있으면 두고두고 꺼내봐야겠다.  

### 오류가 정말 많이 생길수 있지만, 계속해서 구글링으로 전부 해결해볼거다!  

출처 : [J Log](https://velog.io/@ejayjeon/M1%EC%97%90%EC%84%9C-%EC%98%A4%EB%9D%BC%ED%81%B4-%EC%A0%84%EC%9E%90%EC%A7%80%EA%B0%91%EC%9C%BC%EB%A1%9C-DB-%EC%9D%B4%EC%9A%A9%ED%95%98%EA%B8%B0%EC%97%B0%EA%B2%B0-%ED%8E%B8)



