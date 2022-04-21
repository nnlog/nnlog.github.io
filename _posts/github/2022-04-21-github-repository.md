---  
layout: post  
title: "fork repository copy in new repository"  
image: github.jpg  
categories: All github  
---

# fork repository copy in new repository  

깃허브를 시작한지 얼마안되어 열정에 사로잡혀 글을 쓰다보니 눈에 들어온 것이 있었는데 바로 github의 꽃인 contibutions이다.  

이 초록초록한걸로 말하자면 일종의 개발 일기 같은거다.  

> 여기서 문제 발생    
> fork repository에서 작성(commit)한 내용은 contribution이 되지 않는다.  

근데 블로그 글을 업로드해도 contribution이 초록불이 안들어와 심기 불편하던 그때 구글링을 통해 방법을 찾았다.

비슷한 경험을 겪는 사람들에게 도움이 되었으면 싶어 글을 작성해본다.  
  
<mr/>  

## 1. 자주 쓰는 저장공간에 새로운 폴더를 생성  

`mkdir {새로운 폴더 이름}`으로 폴더생성 후 `cd {새로운 폴더}`로 폴더 진입  

<mr/>  

## 2. old repository를 새로운 폴더에 복사  

<br/>  

<img width="1411" alt="스크린샷 2022-04-21 오후 11 24 05" src="https://user-images.githubusercontent.com/103972967/164480652-e13fe794-c13c-4864-b18b-06ba733e166e.png">  

<br/>  

`git clone --mirror {old repository url}` 입력 하면 새로운폴더에 전에 쓰던 repository 파일들이 복사된다.  

이렇게 `--mirror`코드를 입력하면 커밋이력까지 함께 가져온다.  

또한 폴더안에 {old repository name}.git이 생성되는데 `cd {old repository name}.git`으로 이동한다.  

<mr/>  

## 3. new repository에 붙혀넣기  

`git remote set-url --push origin {new repository url}`  
new repository url부분에 새로 만든 repository url을 붙혀 넣고 입력한다.  

마지막으로 `git push --mirror`로 입력해주면 모든 파일들이 전부 새로운 repository로 들어간다.  

이후에는 `rm -rf .git` -> `cd ..` -> `rm -rf {새로만든폴더}`순으로 입력해 잠시 거쳐간 폴더를 지워준다.  


p.s. `push --mirror`과정에서 github username, password 물어볼 수 있는데 그건 [github password No! token Yes!!]()에서 확인 할 수 있다.
