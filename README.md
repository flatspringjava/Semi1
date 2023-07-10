<!-- Improved compatibility of back to top link: See: https://github.com/othneildrew/Best-README-Template/pull/73 -->
<a name="readme-top"></a>
<!--
*** Thanks for checking out the Best-README-Template. If you have a suggestion
*** that would make this better, please fork the repo and create a pull request
*** or simply open an issue with the tag "enhancement".
*** Don't forget to give the project a star!
*** Thanks again! Now go create something AMAZING! :D
-->


<!-- PROJECT SHIELDS -->
<!--
*** I'm using markdown "reference style" links for readability.
*** Reference links are enclosed in brackets [ ] instead of parentheses ( ).
*** See the bottom of this document for the declaration of the reference variables
*** for contributors-url, forks-url, etc. This is an optional, concise syntax you may use.
*** https://www.markdownguide.org/basic-syntax/#reference-style-links
-->

<!-- PROJECT LOGO -->
<br />
<div align="center">
  <a href="https://https://semi.flatjava.co.kr/" target="_blank">
    <img src="image/logo.png" alt="Logo" width="200">
  </a>

  <h3 align="center">영화 예매 사이트</h3>

  <p align="center">
    Spring Legacy Project를 활용한 영화 좌석 예매 사이트
    <br>
    <p>작업기간 : 2023.03.24~2023.04.26</p>
    vcs worked on svn
    <br>
  </p>
  <a href="https://semi.flatjava.co.kr" target="_blank">View Demo</a>
</div>

<!-- ABOUT THE PROJECT -->
## About The Project

<img src="image/semiIndex.png" >

<br>
Spring legacy Project / Maven <br>
학원 세미프로젝트 <br>
Spring, JSP, MariaDB를 활용하여 영화 예매 사이트 구현


### Built With
<img src="https://img.shields.io/badge/jsp-white?style=flat&logo=jsp&logoColor=black"/><img src="https://img.shields.io/badge/javascript-F7DF1E?style=flat&logo=javascript&logoColor=black"/><img src="https://img.shields.io/badge/jquery-0868AB?style=flat&logo=jquery&logoColor=white"/> <img src="https://img.shields.io/badge/Bootstrap3-magenta?style=flat&logo=Bootstrap&logoColor=black"/><br>
<img src="https://img.shields.io/badge/Java-white?style=flat&logo=java&logoColor=white"/>
<img src="https://img.shields.io/badge/Spring-green?style=flat&logo=spring&logoColor=white"/>
<img src="https://img.shields.io/badge/Mybatis-red?style=flat&logo=Mybatis&logoColor=white"/><br>
<img src="https://img.shields.io/badge/mariaDB-lightgray?style=flat&logo=mariadb&logoColor=white"/><br>
<img src="https://img.shields.io/badge/Tomcat-orange?style=flat&logo=Tomcat&logoColor=white"/><br>


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- GETTING STARTED -->
## Getting Started

프로젝트를 복제하여 로컬에서 설정하는 방법에 대한 설명 입니다. <br>

### 사전준비

#### 저장소 복제
   ```sh
   git clone https://github.com/flatspringjava/Semi1.git
   ```

 #### 데이터베이스 구성

  <img alt="ERD" src="image/ERD.png" width="500">

 #### 데이터베이스 테이블 생성 쿼리
  
  <details>
    <summary>query</summary>  
    
    
    

    


    
    
  </details>
    
    
#### 데이터베이스 연결 <br>
root/src/main/resources/jdbc.properties 생성
<br>

  ```sh
db.classname=net.sf.log4jdbc.sql.jdbcapi.DriverSpy
db.url=jdbc:log4jdbc:mariadb://'DB url':'port'/'DB name'
db.username='username'
db.password='password'
  ```

입력

### 설치

1. JDK 1.8
2. STS 3.9.4
3. MariaDB
4. Lombok
5. Tomcat9

### Web Data Crawling
<pre>
이슈 :

- 부트스트랩3 버전의 템플릿 사용중 버전문제로 인한 오류 -> Document 활용하며 템플릿 버전 호환
- 팀원의 중도 이탈로 인해 공백 발생 -> 영화 감상평의 정보를 리뷰 게시판으로 출력하여 공백을 최소화
- 
</pre>



<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- USAGE EXAMPLES -->
## 사용방법 및 기능소개
#### 기능소개
<pre>
1. 회원 :
    1-1. 회원가입 : id, pw, 이름, email을 입력하여 회원가입
    1-2. 로그인 : id, pw를 입력, DB에 암호화되어 저장된 값을 확인하여 로그인 성공/실패
    1-3. 정보 수정 : 로그인한 유저의 세션을 가져와 기본 정보 및 PW 변경        

2. 영화 관람평 :
     2-1. 관람평 등록 : title, content 안에 값을 대입하여 등록 가능 
	
3. 영화 예매 :
     3-1. 영화선택
     3-2. 극장선택
     3-3. 상영시간선태
     3-4. 시간선택
     3-5. 좌석 선택 : 3-1부터 3-4까지 선택이 되어있는 상태에서 좌석 선택 페이지로 이동 가능
     3-6. 인원에 따른 좌석 선택 : 1명이거나 2명일 경우 선택 가능
     3-7. 티켓 출력 : 영화명, 영화관, 상영관, 상영시간, 좌석 조회
     3-8. 결제

4. Web Data Crawling
   - CGV 사이트 데이터의 이미지, 이미지에 따른 제목과 내용 크롤링
</pre>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

<!-- ROADMAP -->
## 요구사항

### 작업목록
- [x] 작업완료 
- [ ] 작업예정 

#### 회원
- [x] 회원가입
  - [x] 약관 동의
  - [x] 메일 API를 이용하여 메일인증
  - [x] BCrypt 사용하여 비밀번호 암호화 
- [x] 로그인
- [x] 마이페이지
  - [x] 회원정보 수정
    - [x] 휴대폰 메세지 API 이용하여 휴대폰인증
  - [ ] 예매 확인 및 취소
- [x] 영화 리뷰 게시판
- [x] 예매
  - [x] 영화선택
  - [x] 지역선택
  - [x] 날짜선택
  - [x] 시간선택
  - [ ] 좌석등급 선택
  - [x] 좌석선택
  - [x] 결제  
<br>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

## Collaborator
 Team Project 
 <pre>
공통 : DB설계, 디지털 프로토 타이핑, 서류작성 (요구사항 정의서, 일정관리, 업무 분장, 테이블 명세서, TEST CASE, 인터페이스 명세서, 인터페이스 세부 설명)

우성준 : <b>조장</b>, 영화 예매, 결제

김성진 : 영화 리뷰 작성, 영화 시간선택, 날짜 선택

이재원(본인) : 회원(로그인, 회원가입, 마이페이지, 로그아웃)
	 
</pre>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- LICENSE -->
## Etc
#### 작업 서류
<a href="https://docs.google.com/spreadsheets/d/1QOmjC81M1BU16yphY2MsAejwuItjSuybFfhTsvnI_6Q/edit#gid=1535322908">
  요구사항 정의서, 일정관리, test case, 테이블 명세서, 인터페이스 명세서 등
</a>
<img src="image/requirements.png"> <br>
위 링크 이동시 하단 sheet를 클릭하여 서류 이동할 수 있음

<br>

#### PPT

<details>
<summary>PPT Images</summary>
<img src="image/ppt.jpg" alt="">

</details>

<br>

#### Digital Prototyping
<a href="https://docs.google.com/presentation/d/1IbjVC4H1NNLV3bkpN1T8uRg6Sw3itWBEv_LJMcPvDXI/edit#slide=id.g2106b4b94ac_0_0"><a/>

### 프로젝트 후기
#### 우성준
<pre>
먼저 많이 부족한 조장이지만 조원들이 포기하지 않고 따라와줘서 감사했습니다. 

여기까지 올 수 있었던 건 순전히 조원들 덕분이었다고 생각합니다​

학생의 입장에서는 스프링을 학교에서도 배우지 않아서 몹시 어려웠지만 

선생님과 다른 학우분들의 도움으로 스프링을 조금 알 수 있었던 시간이었습니다.​

트랙잭션 같은 예매에서 중요한 작업들을 미쳐 해내지 못한 것이 아쉽지만, 복습의 기회로 삼아 앞으로 나아가려고 합니다.​
</pre>

#### 김성진
<pre>
프로젝트를 진행 하면서 몰랐던 기능구현을 자연스럽게 공부하게 되었고 특히 Spring 등 각각의 프로그램 등을 이용하여 

설계부터 구현까지 모든 것을 한번씩 해본 것에 대해  한층 더 성장할 수 있는 계기가 되었습니다.​

세미프로젝트로서 하기엔 많은 기능에 대한 구현의 어려움이 있었지만 포기하지 않는 열정을 배울 수 있어서 좋은 경험이 

되었다고 생각합니다. ​
</pre>
#### 이재원
<pre>
이번 세미 프로젝트 진행 중 사용했던 개발도구들의 기초지식이나 구현 능력이 부족했으나 사용자에 대한 기능 구현을 하면서 

부족했던 점을 보완할 수 있었다고 생각합니다. 

그리고 이전에 팀원들의 배려가 있었기 때문에 구현에 대해 집중할 수 있었습니다. ​

구현 시간을 단축하려 노력했으나 개인적으로 아쉬움이 남아 다음에는 구현 능력을 높여 팀원들이 덜 고생하도록 

노력해야겠다고 생각 했습니다.
</pre>


<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Lee JaeWon - wodnjsdl01@@gmail.com

<a href="https://semi.flatjava.co.kr/" target="_blank">Demo Link</a>

<a href="https://portfolio.flatjava.co.kr/" target="_blank">Portfolio Link</a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

읽어주셔서 감사합니다 더욱더 노력하겠습니다!

### References
README Template : [README-Template](https://github.com/othneildrew/Best-README-Template)<br>
Data Crawling : [CGV](https://www.cgv.co.kr/)<br>
Reference : [메가박스](https://www.megabox.co.kr/)<br>

<p align="right">(<a href="#readme-top">back to top</a>)</p>

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fyangchanyong%2FAWS_fullstack_semi_project&count_bg=%23A1EF67&title_bg=%2300FF57&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
