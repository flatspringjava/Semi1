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
    <img src="images/logo.png" alt="Logo" width="200">
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

<img src="images/mainpage.png" >

<br>
Spring legacy Project / Maven <br>
학원 세미프로젝트 <br>
Spring, JSP, MariaDB를 활용하여 영화 예매 사이트 구현


### Built With
<img src="https://img.shields.io/badge/jsp-white?style=flat&logo=jsp&logoColor=black"/><img src="https://img.shields.io/badge/javascript-F7DF1E?style=flat&logo=javascript&logoColor=black"/><img src="https://img.shields.io/badge/jquery-0868AB?style=flat&logo=jquery&logoColor=white"/> <img src="https://img.shields.io/badge/Bootstrap5-magenta?style=flat&logo=Bootstrap&logoColor=black"/><br>
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

  <img alt="ERD" src="images/ERD.png" width="500">

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
<a href="https://docs.google.com/spreadsheets/d/1vR_ndYQ9Qo1sNOTPU-IdHNJidZm6kdvIH_R9J21spFo/edit?usp=sharing">
  요구사항 정의서, 일정관리, test case, 테이블 명세서, 인터페이스 명세서 등
</a>
<img src="images/document.png"> <br>
위 링크 이동시 하단 sheet를 클릭하여 서류 이동할 수 있음

<br>

#### PPT

<a href="https://www.canva.com/design/DAFgzktHeAY/UTyodLZXtAGB1K2k8WMEqw/view?utm_content=DAFgzktHeAY&utm_campaign=share_your_design&utm_medium=link&utm_source=shareyourdesignpanel">PPT Link</a>

<details>
<summary>PPT Images</summary>
<img src="images/ppt/1.png">
<img src="images/ppt/2.png">
<img src="images/ppt/3.png">
<img src="images/ppt/4.png">
<img src="images/ppt/5.png">
<img src="images/ppt/6.png">
<img src="images/ppt/7.png">
<img src="images/ppt/8.png">
<img src="images/ppt/9.png">
<img src="images/ppt/10.png">
<img src="images/ppt/11.png">
<img src="images/ppt/12.png">
<img src="images/ppt/13.png">
<img src="images/ppt/14.png">
<img src="images/ppt/15.png">
<img src="images/ppt/16.png">
<img src="images/ppt/17.png">
<img src="images/ppt/18.png">
<img src="images/ppt/19.png">
<img src="images/ppt/20.png">
<img src="images/ppt/21.png">
<img src="images/ppt/22.png">
<img src="images/ppt/23.png">
<img src="images/ppt/24.png">
<img src="images/ppt/25.png">
<img src="images/ppt/26.png">
<img src="images/ppt/27.png">
<img src="images/ppt/28.png">
<img src="images/ppt/29.png">
<img src="images/ppt/30.png">
<img src="images/ppt/31.png">
</details>

<br>

#### Digital Prototyping
<a href="https://ovenapp.io/view/9aaHlLOD5IvM5pwGJGYgNHA5T7OIKK3J/RZBG9">Digital Prototyping Link<a/>

### 프로젝트 후기
#### 양찬용
<pre>
저는 회의와 서류에 중점을 두고 프로젝트를 진행했습니다. 
팀원 한 명 한 명이 도태되는 일 없이 프로젝트를 진행하기 위해 
매일 오전에 회의하여 진행도, 서류작업 등 보고를 받았고, 
학원이 끝나는 시간엔 일일업무보고를 디스코드에 올려 서로 업무가 얼마나 
진행되었는지 보고를 받았고, 저 또한 팀원들에게 보고를 했습니다. 
그 결과 서로 막힌 부분이 있거나 시간 관계상 빨리 끝내야 하는 일이 생길 때
던 일을 멈추고 팀원을 도와줘야 되는 경우에도 서로 막힘없이 프로젝트를 진행했고, 
즐겁게 프로젝트를 끝낼 수 있었습니다. 


위 프로젝트를 진행하며 아쉬웠던 점은 시간 관계상 구현하지 못한 
일부 관리자 기능(통계,   실시간 상담, 상품 등록 및 수정 등)입니다. 
프로젝트 설계 단계에서는 많은 관리자 기능이 있었고, 
첫 번째 프로젝트에서 맡았던 일을 똑같이 다시 맡으면 
관리자 기능을 많이 작업할 수 있었지만, 팀원 모두 실력 향상을 위해 
모두 첫 프로젝트와 다른 작업을 하길 원했고 저 또한 그렇게 하길 원했습니다. 
비록 일부 기능을 구현하지 못해서 아쉬웠지만 
다들 큰 폭으로 실력 향상이 되어서 만족스러운 프로젝트였습니다.
</pre>

#### 이동건
<pre>
Spring이 무엇인지도 모르고 프로젝트를 시작했지만 
Controller와 Service, DTO, Mapper등을 사용해보면서 왜 써야하는지, 
왜 필요한지를 알게 되었고, 비동기 처리 또한 많은 부분에서 필요한 것들이 많았으며, 
팀원들과 협동을 통해 프로젝트에 재미를 더 붙일 수 있어서 좋은 시간이었습니다. 
</pre>
#### 이지윤
<pre>
서류 작업부터 여러 가지 툴을 사용하는 프로젝트는 처음이라 
그 과정에서 겪은 어려운 점도 많았지만 프로젝트 덕분에 
스프링과 DB등의 툴 사용이 전보다 익숙해질 수 있었습니다.
</pre>
#### 박연재
<pre>
팀원들과 협력과 강사님의 피드백으로 기능, 
화면 면에서 배울 점들이 많았고, 
코드를 작성하면서 서류도 동시에 작업해야한다는 것과 
그와 동시에 서로 간의 피드백과 의사소통이 엄청 중요하다라는 것을 
프로젝트를 통해 실감하게 되었습니다.
</pre>
#### 이창용
<pre>
ppt 템플릿 조사, 부트스트랩 템플릿 조사, 일일 회의록 주간 회의록 작성 등등 
맡은 업무에 대해 열심히 실천하였고 마음 한편으론 아쉬움이 남았다
</pre>




<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- CONTACT -->
## Contact

Yang Chanyong - cksdyd93@gmail.com

<a href="https://pf3.chanyongyang.com" target="_blank">Demo Link</a>

<a href="https://www.chanyongyang.com" target="_blank">Portfolio Link</a>

<p align="right">(<a href="#readme-top">back to top</a>)</p>



<!-- ACKNOWLEDGMENTS -->
## Acknowledgments

이 프로젝트를 사용해주시고 README를 읽어주신 여러분께 대단히 감사합니다!

### References
README Template : [README-Template](https://github.com/othneildrew/Best-README-Template)<br>
Data Crawling : [지키미몰](https://xn--352blxn61avvg.com/)<br>
Reference : [식자재왕](https://www.ewangmart.com/main/index.do?utm_source=google&utm_medium=sa&utm_campaign=sa_google_pc&utm_content=%EB%A9%94%EC%9D%B8_%EB%B8%8C%EB%9E%9C%EB%93%9C&utm_term=%EC%8B%9D%EC%9E%90%EC%9E%AC%EC%99%95&gad=1&gclid=Cj0KCQjwnf-kBhCnARIsAFlg490cNtHom16NNcR-4PXQOPzO6mPCudFADp0KuDsg63amSdgAijsBm5QaAsh6EALw_wcB)<br>
Reference : [씨엔푸드몰](https://seanfoodmall.com/)<br>


<p align="right">(<a href="#readme-top">back to top</a>)</p>

[![Hits](https://hits.seeyoufarm.com/api/count/incr/badge.svg?url=https%3A%2F%2Fgithub.com%2Fyangchanyong%2FAWS_fullstack_semi_project&count_bg=%23A1EF67&title_bg=%2300FF57&icon=&icon_color=%23E7E7E7&title=hits&edge_flat=false)](https://hits.seeyoufarm.com)
