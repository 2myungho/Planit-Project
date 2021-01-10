# 📒 플랜잇(PLAN IT)

<img src="img/플랜잇_로고.png" alt="플랜잇_로고" style="zoom:80%;" />

![플랜잇_텍스트](/img/플랜잇_텍스트.png)

## 👨‍👨‍👧‍👧 Members

- #### 정승훈 [shoon2430](https://github.com/shoon2430)

- #### 박민재 [parkmm14](https://github.com/parkmm14)

- #### 이명호 [2myungho](https://github.com/2myungho)

- #### 이은송 [eunsongsong](https://github.com/eunsongsong)

## 프로젝트 기능별 서비스

- [플랜잇](https://github.com/JL2P)

  - [Front-end](https://github.com/JL2P/PlanList-Frontend)
  - [Auth-Service](https://github.com/JL2P/Auth-service)
  - [Account-Service](https://github.com/JL2P/Account-service)
  - [Todo-Service](https://github.com/JL2P/Todo-service)
  - [Group-Service](https://github.com/JL2P/Group-service)
  - [Point-Service](https://github.com/JL2P/Point-service)

  

## 📝 Document

- #### [프로젝트 관리](https://github.com/JL2P/Project/wiki)



## 0. 실행 방법

* **AWS EC2** 서버에 **Docker**을 설치해서 활용했습니다.
* **Docker Compose**를 사용해 각각의 기능 서비스를 컨테이너에 나누어 **MSA** 방식으로 배포했습니다. 
  * http://myplanit.co.kr/
  * _요금 발생으로 EC2 인스턴스가 중지되어 있습니다._



## 1. 프로젝트 소개

* 플랜잇 서비스를 통해 사람들이 계획을 공유하여 동기부여와 능률을 향상시키고, 계획을 세우는 것 자체가 어려운 경우 다른 사람의 계획을 통해 정보를 얻을 수도 있습니다. 
* 위 목표를 바탕으로 사람들과 계획으로 소통하는 SNS Todo 서비스를 기획하게 되었습니다. 💬



## 2. 사용 기술 및 개발 계획 📌

### 1) 사용 기술

##### 기능 구현

* Java
* Spring Boot
* Javasctipt
* React.js
* MSA

##### 데이터베이스

* MariaDB

##### 클라우드 기능

* AWS EC2 + Docker
* AWS S3

##### 에디터

* Visual Studio
* IntelliJ

##### 기타

* PuttTTy

### 2) 개발 계획

* **1차 진행 기간 : 2020.09.19 ~ 2020.09.24**
  * 프로젝트 기획 및 팀 구성
  * SNS 성향을 가진 Todo 서비스를 만들기로 확정
* **2차 진행 기간 : 2020.09.24 ~ 2020.11.14**
  * Todo, Group, Account, Auth 서비스 완료
  * 팀별 중간 점검
* **3차 진행 기간 : 2020.11.14 ~ 2020.12.04**
  * 아직 완료되지 못한 핵심기능 및 Point 서비스 개발
  * 최종 점검
* **프로젝트 목표** 
  * 교육 기간 동안 배운 기술을 모두 사용해 볼 수 있는 시간이 되었으면 한다!
  * 업무 분담을 기능 서비스 단위로 나누어 팀원 개개인이 프론트엔드 부분과 백엔드 부분 모두 다룰 수 있도록 했다.



## 3) 업무 분담

😊 **정승훈 :**  [shoon2430](https://github.com/shoon2430)

* 감독/총괄 및 Data(store) 관리
* Todo 서비스 개발
* 인증 서비스 개발
* 프로젝트 배포 참여

😊 **이명호 :**  [2myungho](https://github.com/2myungho)

* Group 서비스 개발
* S3 파일 업로드 서비스 개발
* 프로젝트 배포 참여
* 풀스택 개발

😊 **박민재 :** [parkmm14](https://github.com/parkmm14)

* 백엔드 개발
* Follow 서비스 개발
* Point 서비스 개발

😊 **이은송 :** [eunsongsong](https://github.com/eunsongsong)

* Account 서비스 개발
* 개인 Point 및 Ranking 서비스 개발
* 프론트 엔드 개발



## 4) 핵심 기능 🔑

### 1) Auth - service

> * **소셜 로그인 기능** 
>   * 카카오 Oauth2 인증을 통해 로그인, 회원가입 기능을 구현했다.
>   * 로그인 시 JWT를 발급하여 로그인 상태를 유지한다.
>   * Planit의 모든 서비스는 발급받은 JWT를 통해 회원인지 인증한다.

### 2) Account - service

> * **나의 프로필 관리 기능**
> * **나의 계획 관리 기능**
> * **다른 사용자 조회 기능**

### 3) Group - service

> * **그룹 생성 및 조회 기능**
> * **나의 그룹 관리 기능 (그룹장)**
> * **나의 그룹 관리 기능 (그룹원)**
> * **그룹 가입 신청 기능**
> * **그룹 Todo 기능**

### 4) Todo - service

> * **개인 Todo 기능**
>   * 내가 작성한 Todo와 팔로우한 사람들의 Todo를 한번에 조회할 수 있다.
>   * Todo에 이미지를 첨부할 수 있다.
>   * Todo에 좋아요와 댓글을 작성할 수 있다.
>   * 반복적인 계획을 세우는 경우를 대비하여 특정 기간을 선택하여 한번에 Todo를 여러 개 작성할 수있다.

### 5) Point - service

> * **개인 점수 기능**
>   * 계획의 완료 여부와 좋아요 개수에 따라 점수를 취득한다.
>   * 무분별한 계획 생성을 방지하기 위해 하루 최대 취득 가능한 점수에 제한을 두었다.
>   * 좋아요 10개   : 1점  (하루 최대   5점 취득 가능)
>   * 계획 완료 1개 : 25점 (하루 최대 100점 취득 가능)
>
> * **나의 레벨 조회 기능** 
>   * 사용자가 취득한 총점(누적 점수)를 기준으로 나의 레벨을 조회할 수 있다.
>   * 하루 최대 취득 가능한 개인 점수 105점을 기준으로 특정 기간 동안 계획을 완료하면 Level 등급이 부여된다.
>   * (예) 3  일 계획 완료 시 Level1
>         7  일 계획 완료 시 Level2
>         14 일 계획 완료 시 Level3
>         30 일 계획 완료 시 Level4  
>         …
>     전체 사용자 랭킹 조회 및 나의 랭킹 조회 기능
>   * 전체 사용자 랭킹을 구간 별 평균 점수로 조회할 수 있다.
>   * 내가 속한 랭킹 구간을 조회할 수 있다.
>
> * **전체 그룹 랭킹 리스트 조회 기능**
>
> * **내가 속한 그룹의 랭킹, 그룹 점수 조회 기능**
>
> * **내 그룹 안에서 그룹원들의 랭킹 리스트 조회 기능**

### 6) Follow 

> * **나의 팔로워 리스트, 팔로잉 리스트 관리 기능**
> * **팔로잉 신청 수락/거절 기능**
> * **팔로잉, 팔로워 계정 프로필, todo 조회 기능**
> * **팔로잉 요청 실시간 알림 기능**



## 시나리오 & 결과 📢

