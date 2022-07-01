---  
layout: post  
title: "[git 에러] remote: Invalid username or password"  
image: github.jpg  
categories: All github  
---

# 원인  
<hr>  

때떄로 터미널에서 `push`하여 깃허브에 파일을 업로드 중  

`remote: Invalid username or password.`와 함께 `push`가 정상적으로 작동하지 않을 때가 있다.  

이는 Git에서 Github로 사용자 계정을 연결하는 과정에서 비밀번호 대신 사용하는 token의  
기한이 만료되면서 정상적으로 연동되지 않아 발생하는 문제이다.  

때문에 이 `token`을 발급 또는 재발급 후 터미널에서 간단한 명령어를 통해 재설정 해주면 된다.  

> [Github Token](https://nnlog.github.io/2022/04/21/github-usertoken/)  

<br>  

# **터미널 설정**  
<hr>  

기존 `origin`을 제거한 후, 다시 추가하는 방법으로 해결한다.  

1. git remote remove origin  
2. git remote add origin http://닉네임:토큰@github.com/repo 경로  

* `닉네임` : 본인의 github 닉네임  
* `토큰` : 발급받은 토큰 입력  
* `repo 경로` : 본인의 repo url을 복붙  

ex) `git remote add origin http://test:token1234@github.com/test/testrepo.io`

