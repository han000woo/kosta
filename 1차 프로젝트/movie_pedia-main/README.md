KOSTA - 1차 팀 프로젝트 
=======
# 📃목차

- 개요
    - 프로젝트 목적
    - 아이디어 및 배경
- 팀원
    - 소개 및 역할 분담
- 설계
    - 주요 기능
    - 사용된 기술 스택
    - 프로젝트 구조
    - ERD 설계
- 동작 화면
- issue 사항
<br/>


# 📌 프로젝트 목적

- 와챠피디아와 유사한 영화 정보 플랫폼을 구현하여, 사용자에게 최신 영화 정보를 제공합니다.
- API 통신, DB 설계, MVC패턴 로직 구현 등 웹 개발 필요한 지식 습득합니다.
- 클론 코딩을 활용하여 단기간에 프로젝트 개발 합니다.
<br/>


# 💡 아이디어 및 배경

- 1차 프로젝트를 기획하는 단계에서 공공 API를 사용한 프로젝트를 개발하면 좋겠다는 생각이 들었습니다
- 팀장의 제안으로 와챠피디아를 클론코딩하여 프로젝트를 진행하면 좋겠다는 생각이 들었습니다.
<br/>

# 🤼 팀 멤버 소개
| **항목**    | **재원**                                                                                       | **선우**                                                                                       | **정아**                                                                                       | **혁주**                                                                                       |
|:----------|:----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------|
| **역할**   | BackEnd(팀장)                                                                                             | BackEnd(팀원)                                                                                             | FrontEnd(팀원)                                                                                             | FrontEnd(팀원)                                                                                             |
| **GitHub** | [김재원 GitHub](https://github.com/UsoD98)                                                   | [한선우 GitHub](https://github.com/hamster0410)                                                   | [최정아 GitHub](https://github.com/berryicebox)                                                   | [석혁주 GitHub](https://github.com/cocoball0)                                                   |
| **주 작업** | 1. 전체 프로젝트 총괄 <br>2. 회원 CRUD 기능 구현 <br>3. 게시글 평점, 코멘트 구현 <br>4. 소셜 기능 구현 <br>5. 영화 API 설계 <br> 6. ERD 설계 <br> 7. 발표 | 1. 주간, 개봉예정작 API 처리 <br> 2. 위시리스트 기능 구현 <br> 3. 화면 전환 처리 <br> 4. 비밀번호 찾기 기능 구현  <br> 5. 영화 정보 검색기능 구현 <br> 6. PPT 제작| 1. 메인 홈페이지 구현 <br> 2. 로그인 페이지 구현 <br> 3. 영화 detail 페이지 구현 <br> 4. 사용자 개인 페이지 구현 <br> 5. html & css 관리 | 1. 메인 홈페이지 구현 <br> 2. 로그인 페이지 구현 <br> 3. 영화 detail 페이지 구현 <br> 4. 사용자 개인 페이지 구현 <br> 5. html & css 관리 |
<br/>

# 🔑 주요 기능

- **회원 관리**
    - 세션 기반 인증 방식을 활용하여 회원가입, 로그인 유지, 회원 전용 기능을 구현했습니다.
- **실시간 영화 정보 제공**
    - 공공 API를 사용해 실시간 박스오피스 정보를 화면에 출력합니다.
    - 일별, 주간, 공개예정작 정보를 메인페이지에 출력하고 db에 전처리하여 저장합니다.
    - 기능 구현을 위해 두 API영화정보 테이블을  join하여 사용합니다.
- **영화 평점 & 코멘트 기능**
    - 사용자마다 영화별 평점을 기록하고 코멘트를 남깁니다.
    - 메인 페이지에서 다른 사용자에 최근 평점 및 코멘트를 출력합니다.
- **영화 보고싶어요 & 보는 중 기능**
    - 내가 찜한 영화 리스트를 확인합니다.
    - 내가 보는 중인 영화 리스트를 확인합니다.
- **사용자 팔로우 기능**
    - 다른 사용자를 팔로우 하여 소셜 커뮤니케이션 기능을 지원합니다.
- **비밀번호 찾기**
    - 사용자에 메일로 임시 비밀번호를 전달합니다.
<br/>


# 사용된 기술 스택
<img width="1257" height="701" alt="image" src="https://github.com/user-attachments/assets/b8554895-1509-491f-9ddd-e6aada6ce258" />

<br/>


# 프로젝트 구조

```bash
├─main
│  ├─java
│  │  └─com
│  │      └─pedia
│  │          └─movie
│  │              ├─config
│  │              ├─movie
│  │              │  ├─controller
│  │              │  ├─dto
│  │              │  ├─entity
│  │              │  ├─repository
│  │              │  └─service
│  │              └─user
│  │                  ├─controller
│  │                  ├─dto
│  │                  ├─entity
│  │                  ├─repository
│  │                  └─service
│  └─resources
│      ├─static
│      │  └─common
│      │      ├─css
│      │      └─js
│      └─templates
│          ├─fragments
│          └─user
└─test
    └─java
        └─com
            └─pedia
                └─movie
```
<br/>


# 🧱  ERD 설계
<img width="1035" height="538" alt="image" src="https://github.com/user-attachments/assets/db194d67-5495-4bc9-9530-fc92230cf929" />

<br/>


# 🔥 동작 화면
### 홈페이지
<p align="center">
    <img width="1826" height="812" alt="image" src="https://github.com/user-attachments/assets/9dfa0b8a-a890-4ace-b773-858d7669697f" />

</p>
<br/>


### 회원기능
<p align="center">
  <img width="1813" height="650" alt="image" src="https://github.com/user-attachments/assets/8929d72b-0abd-4bda-9693-536f76f8e1d5" />
  <img width="1710" height="781" alt="image" src="https://github.com/user-attachments/assets/d76afbed-fa2f-4704-9232-ab1f134b1b27" />
  <img width="1720" height="514" alt="image" src="https://github.com/user-attachments/assets/a93a3826-cd1f-4d66-966d-a8067cc74605" />
</p>

<br/>

### 평점 및 찜하기
<p align="center">
<img width="930" height="630" alt="image" src="https://github.com/user-attachments/assets/cb238e05-0716-427a-be6c-a19db9c284bf" />
</p>
<br/>

### 코멘트
<p align="center">
  <img width="1826" height="465" alt="image" src="https://github.com/user-attachments/assets/dbcef2e4-c40b-4bc2-aa71-3280c70b2902" />
</p>
<br/>

### 마이페이지
<p align="center">
<img width="1851" height="439" alt="image" src="https://github.com/user-attachments/assets/6f376292-1ca6-48cb-8f86-ef5f50e6d0ce" />
</p>
<br/>

### 영화 검색
<p align="center">
<img width="1683" height="577" alt="image" src="https://github.com/user-attachments/assets/92012c87-485d-4036-a9b3-d2119a0612b5" />
</p>
<br/>

# ❓ Issue 사항
첫 번째 트러블 슈팅:
- API 호출 시간 지연 문제를 해결하기 위해, 상영 예정작 기능에서 KOBIS API 호출을 제거하고 TMDB API만 사용하도록 수정했습니다.
- 이에 따라 데이터베이스의 movieCd 컬럼의 유니크 제약을 제거하고, 일일 및 주간 박스오피스 데이터 처리 로직을 조정했습니다.

두 번째 트러블 슈팅:
- 메인 페이지에서 박스오피스 목록 요청 시 발생한 순환 참조 문제가 발생했습니다.
-  엔티티 클래스 대신 DTO 객체를 사용하여 데이터를 반환하도록 수정했습니다.
<br/>

# 참고자료
ppt : https://www.miricanvas.com/v/13n2jqg
<br>
notion : https://www.notion.so/1-69371a9ec7d2464dadd9e7b598e89a36
