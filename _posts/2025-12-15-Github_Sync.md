---
layout: single
title: "멀티 기기 GITHUB 블로그 동기화"
date: 2025-12-15
categories:
  - GITHUB
  - github_setup
tags: [GitHub, 설정]
author_profile: true
read_time: true
comments: true
share: true
related: true
sidebar:
  nav: "categories_sidebar"
---


# GITHUB 블로그를 여러 기기에서 관리해 보자


노트북에서 사용하던 Jekyll 기반 깃허브 블로그를<br>
데스크톱에서도 운영하기 위해 내가 사용한 방법들을 정리한 글이다.<br>






## 1. Git 설치


먼저 아래 링크를 통해 Git을 설치해 준다.<br><br>


> ** [Git 설치 페이지](https://git-scm.com/downloads) **<br><br>


설치가 끝나면 다음 명령어로 설치 확인을 해준다.<br>


```bash
git --version
```






## 2. Ruby 설치


아래 링크를 통해 Ruby를 설치해 준다.<br><br>


> ** [Ruby 설치 페이지](https://rubyinstaller.org/) **<br><br>


설치 중에 Add Ruby executables to your PATH 항목에 체크를 해준다.<br>
설치가 끝나면 나오는 MSYS2 Devkit 설치에서 → 1번을 선택해 준다.<br>


설치가 끝나면 다음 명령어로 설치 확인을 해준다.<br>


```bash
ruby -v
gem -v
```


주의할 점은 설치 후 명령 프롬프트를 새로 열고 확인을 해야 설치 확인이 가능하다.<br>






## 3. Jekyll & Bundler 설치

아래 명령어를 통해 설치해 준다.<br>


```bash
gem install bundler jekyll
```


마찬가지로 설치 후 확인해 준다.<br>


```bash
jekyll -v
```






## 4. GitHub 블로그 저장소 클론


아래 명령어를 통해 GitHub 블로그 저장소를 클론해 준다.<br>


```bash
git clone https://github.com/아이디/아이디.github.io.git
```


여기서 아이디 부분엔 본인의 아이디를 넣어주면 된다.<br>






## 5. Gem 설치 (⭐ 꼭 필요)


아래 명령어로 블로그 폴더로 이동한다.<br>


```bash
cd 아이디.github.io
```


그리고 여기에서 다음 명령어로 Gem을 설치해 준다.<br>


```bash
bundle install
```






## 6. 로컬 서버 실행


원래 기기에서 하던 것과 같이 로컬 서버를 실행해 준다.<br>


```bash
bundle exec jekyll serve
```


여기서 본인의 블로그 페이지가 보인다면 성공한 것이다.<br>






## 7. 블로그 포스팅


본인은 Visual Studio Code 와 GitHub Desktop으로 글을 관리한다.<br><br>


먼저 GitHub Desktop에 로그인 후, FILE -> Add local repository 로 리포지토리를 불러와 준다.<br><br>


그리고 원래 기기에서 하던 것처럼 글을 수정하고 작성하면 되는데, 주의할 점이 있다.<br><br>


충돌을 막기 위해서 한 기기에서 수정이 끝나 push를 완료하면,<br>
꼭 다른 기기에서 pull로 작업 내용을 가져온 후 수정해야 충돌이 발생하지 않는다.<br><br>


push, pull은 GitHub Desktop의 Fetch Origin 부분을 이용하면 된다.<br>





-----------------------------------------------------------------------<br>


이제 노트북과 데스크톱 어디서든 블로그를 편하게 관리할 수 있다.<br>