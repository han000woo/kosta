# KOSTA 3차 프로젝트 : 애니멀핑 🐾 
<br/>

<img src="https://github.com/user-attachments/assets/d2eec0a8-4eba-4288-bf9c-c93846bb3159" width="800"/>


# 목차

- 개요
    - 프로젝트 목적
    - 아이디어 및 배경
    - 프로젝트 플랜
- 팀원
    - 소개 및 역할 분담
- 설계
    - 주요 기능
    - 사용된 기술 스택
    - 프로젝트 구조
    - REST API 설계
    - ERD 설계
    - 흐름도
- 동작 화면
- issue 사항
<br/>


# 프로젝트 목적

- 반려동물 정보를 기반으로한 내 반려동물 맞춤 플랫폼 
- 위치기반 정보, 공공 API를 기반으로한 서비스 제공 
<br/>


# 아이디어 및 배경

- 반려동물을 키우는 사람들이 내가 키우는 반려동물에 대해 더 잘 알고 다양한 생각을 공유하는게 좋다는 생각이 들었습니다. (커뮤니티, 동물백과, 펫 정보 계산기)
- 반려동물을 키우는 사람들이 더 잘 키울 수 있기를 바랍니다. (쇼핑몰 운영 & 관리자와 채팅)
- 반려동물과 함께 가볼만한 곳을 알려주고 싶었습니다. (펫 동반시설 지도 검색)
- 반려동물에게 새 가족을 만들어 주고 싶었습니다. (유기동물 관심상태 등록 및 상태 메일 전송)
  
<br/>

# 프로젝트 일정
<img width="1020" height="455" alt="image" src="https://github.com/user-attachments/assets/91fff53e-c31f-40b1-83e4-925f2ce7e64d" />

<br/>

# 팀 멤버 소개

| **항목**     | **선우**                                                                                      | **소진**                                                                                      | **정아**                                                                                      | **혁주**                                                                                      |
|:------------|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|:---------------------------------------------------------------------------------------------|
| **역할**     | BackEnd(팀장)                                                                                     | FrontEnd(부팀장)                                                                                     | FrontEnd                                                                                     | BackEnd                                                                                     |
| **GitHub**   | [한선우 GitHub](https://github.com/hamster0410)                                               | [최소진 GitHub](https://github.com/sosojean)                                                 | [최정아 GitHub](https://github.com/berryicebox)                                              | [석혁주 GitHub](https://github.com/cocoboll0)                                              |
| **주 작업**  | 1. 팀 전체 관리 <br>2. REST API 설계<br>3. ERD 설계 <br>4. 소셜 로그인, 페이, 소켓 채팅 구현<br>5. 쇼핑몰 CRUD 구현 <br>6. 발표 | 1. 프로젝트 기획 <br>2. 백엔드 통신 설계 <br>3. 지도, 채팅 구현 <br>4. 댓글 및 대댓글 로직 구현<br>5. 판매 데이터 분석 툴 구현<br>6. React 프로젝트 관리 | 1. 팀 회의 서기 <br>2. 내 반려동물 정보 기반 계산기 구현 <br>3. 동물 백과 구현<br>4. 유기동물 검색 구현 <br>5. 장바구니 및 판매 상품 구현 | 1. 팀 일정 관리<br> 2. 오픈 API 전처리 <br>3. 쇼핑몰 CRUD 구현 <br>4. API 명세서 작성 <br>5. 코드 리팩토링 & QA <br>6. 발표 자료 작성 |
<br/>


# 주요 기능

- **커뮤니티**
    - 다양한 카테고리를 가진 게시판을 통해 반려동물을 키우는 사람들이 원하는 주제로 소통합니다. 
- **쇼핑몰**
    - 반려동물을 키우는데 필요한 물건들을 사용자가 직접 사고 판매합니다. 
- **유틸리티**
    - 반려동물을 키우는데 도움이 될만한 기능들을 추가했습니다. 

    
# 사용된 기술 스택
<img width="1076" height="600" alt="image" src="https://github.com/user-attachments/assets/bd7fcbb9-0a68-4b26-9c1b-b6104cc89084" />

<br/>


# 프로젝트 구조

```agda
📁 Front End (React)
├── 📘 App.jsx (.jsx)
├── 📘 App.test.js (.js)
├── 📄 index.css (.css)
├── 📘 index.jsx (.jsx)
├── 📁 assets
│   ├── 📁 fonts
│   ├── 📁 img
│   └── 📁 styles
├── 📁 components
│   ├── 📁 additional
│   │   ├── 📘 adopt.jsx
│   │   ├── 📘 calc.jsx
│   │   └── 📘 wiki.jsx
│   ├── 📘 board.jsx
│   ├── 📘 chatting.jsx
│   ├── 📘 comment.jsx
│   ├── 📘 common.jsx
│   ├── 📘 layout.jsx
│   ├── 📘 map.jsx
│   ├── 📁 member
│   │   ├── 📁 myPage
│   │   │   └── 📘 items.jsx
│   │   ├── 📘 password.jsx
│   │   └── 📁 pet
│   │       └── 📘 register.jsx
│   └── 📁 shop
│       ├── 📁 admin
│       │   └── 📘 notice.jsx
│       ├── 📁 order
│       │   ├── 📘 delivery.jsx
│       ├── 📁 product
│       │   ├── 📘 QnA.jsx
│       │   ├── 📘 detail.jsx
│       │   ├── 📘 option.jsx
│       │   └── 📘 review.jsx
│       └── 📁 seller
│           ├── 📘 itemList.jsx
│           ├── 📘 itemRegister.jsx
│           └── 📘 sellerQna.jsx
├── 📁 pages
│   ├── 📘 additional.jsx
│   ├── 📘 board.jsx
│   ├── 📘 chatting.jsx
│   ├── 📘 map.jsx
│   ├── 📘 member.jsx
│   └── 📁 shop
│       ├── 📘 admin.jsx
│       ├── 📘 order.jsx
│       ├── 📘 product.jsx
│       └── 📘 seller.jsx
└── 📁 utils

----------------------------------------------------------------------------------------

Back End (Spring Boot)

📁 project
├── 📁 community
│   ├── 📁 comment
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 heart_comment
│   │   ├── ☕ controller.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 heart_post
│   │   ├── ☕ controller.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 member
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   └── 📁 post
│       ├── ☕ controller.java
│       ├── ☕ dto.java
│       ├── ☕ entity.java
│       ├── ☕ repository.java
│       └── ☕ service.java
├── 📁 global
│   ├── 📁 admin
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 config
│   ├── 📁 controller
│   ├── 📁 dto
│   ├── 📁 init
│   ├── 📁 pay
│   │   ├── 📁 config
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 security
│   └── 📁 service
├── 📁 shop
│   ├── 📁 cart
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 cart_item
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 delivery
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 item
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 item_comment
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 item_comment_like
│   │   ├── ☕ controller.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 main
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   └── ☕ service.java
│   ├── 📁 order
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 order_item
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   └── ☕ repository.java
│   ├── 📁 pet
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   ├── 📁 point
│   │   ├── ☕ controller.java
│   │   ├── ☕ dto.java
│   │   ├── ☕ entity.java
│   │   ├── ☕ repository.java
│   │   └── ☕ service.java
│   └── 📁 seller
│       └── ☕ controller.java
└── 📁 tools
    ├── 📁 abandoned_animal
    │   ├── ☕ controller.java
    │   ├── ☕ dto.java
    │   ├── ☕ entity.java
    │   ├── ☕ repository.java
    │   └── ☕ service.java
    ├── 📁 calculate
    │   ├── ☕ controller.java
    │   ├── ☕ dto.java
    │   └── ☕ service.java
    ├── 📁 chat
    │   ├── ☕ controller.java
    │   ├── ☕ dto.java
    │   ├── ☕ entity.java
    │   ├── ☕ repository.java
    │   └── ☕ service.java
    ├── 📁 map_service
    │   ├── ☕ controller.java
    │   ├── ☕ dto.java
    │   ├── ☕ entity.java
    │   ├── ☕ repository.java
    │   └── ☕ service.java
    └── 📁 wiki_service
        ├── ☕ controller.java
        ├── ☕ dto.java
        ├── ☕ entity.java
        ├── ☕ repository.java
        └── ☕ service.java


```
<br/>


# ✉REST API 명세서
API에 대한 자세한 내용은 아래 링크를 참고하세요:

[REST API 명세서 보기](https://www.notion.so/api-13ddb7c32eb98022b074dd7562af351e)



# 동작 화면
<img width="1462" height="952" alt="image" src="https://github.com/user-attachments/assets/d2eec0a8-4eba-4288-bf9c-c93846bb3159" />
<img width="995" height="859" alt="image" src="https://github.com/user-attachments/assets/3ffcd60c-f881-4778-b89d-5cf8e66131a4" />
<img width="1140" height="833" alt="image" src="https://github.com/user-attachments/assets/dae1ce63-4642-45ca-bf84-24dd4807f5ef" />
<img width="1334" height="863" alt="image" src="https://github.com/user-attachments/assets/73307f76-8f91-407a-bf7e-f7f092daa140" />


### 소셜 회원가입 & 로그인
<p align="center">
    <img width="1265" height="804" alt="image" src="https://github.com/user-attachments/assets/c869e7b5-b427-414d-a4f8-2d1db1f8c9ae" />
</p>
<br/>

### 비밀번호 수정
<p align="center">
    <img width="1167" height="737" alt="image" src="https://github.com/user-attachments/assets/0d7f532c-1765-4f48-a0fc-b445d8454f42" />
</p>
<br/>


### 댓글 대댓글
<p align="center">
  <img width="790" height="844" alt="image" src="https://github.com/user-attachments/assets/46d8aeb3-d85b-4f18-a9e8-dcb8c318c4ec" />
</p>
<br/>

### 펫 등록
<p align="center">
  <img width="1297" height="858" alt="image" src="https://github.com/user-attachments/assets/47035e41-2cc8-4c96-ba09-1c38ba8b1abb" />
</p>
<br/>

### 펫 맞춤 상품 추천
<p align="center">
  <img width="1267" height="842" alt="image" src="https://github.com/user-attachments/assets/d9ef05e0-fa48-46e5-a97f-9ee1ea6313ce" />
</p>
<br/>

### 장바구니 구매
<p align="center">
  <img width="1075" height="620" alt="image" src="https://github.com/user-attachments/assets/69d2eb60-267c-46bc-8286-042f1adf1327" />
</p>
<br/>

### 계산기
<p align="center">
  <img width="955" height="874" alt="image" src="https://github.com/user-attachments/assets/f11968c6-8c05-46a8-98fa-615acc59217a" />
<br/>

### 동물백과
<p align="center">
  <img width="859" height="746" alt="image" src="https://github.com/user-attachments/assets/5b5214bf-c3cf-4c85-9bce-cb94d9387b60" />
</p>
<br/>

### 위치 기반 지도 검색
<p align="center">
  <img width="1082" height="837" alt="image" src="https://github.com/user-attachments/assets/e27900f9-481c-4794-b5ab-bec6197a6d89" />
</p>
<br/>

### 유기동물 검색
<p align="center">
  <img width="1132" height="945" alt="image" src="https://github.com/user-attachments/assets/70b334b1-85f9-4564-bac6-f74e62b958d0" />
</p>
<br/>

### 판매자 대시보드
<p align="center">
  <img width="1343" height="907" alt="image" src="https://github.com/user-attachments/assets/3f4c7f45-2bee-4695-a258-972eb26afe07" />
</p>

<br/>

### 관리자 대시보드
<p align="center">
  <img width="1115" height="892" alt="image" src="https://github.com/user-attachments/assets/7e49be9e-7925-4e6d-9877-618677ab93e0" />
</p>

<br/>

### 관리자 채팅
<p align="center">
  <img width="1847" height="935" alt="image" src="https://github.com/user-attachments/assets/45802dc5-63ea-4c6f-92d7-921d29d40c53" />
</p>

<br/>


<br/>


# Issue 사항

개발 과정에서 특히 공을 들였던 부분은 아래와 같습니다:

1. **내 상품 구매 정보를 각 판매자에게 다르게 전달**  
   - `HashMap`을 활용하여 각 판매자에게 적합한 구매 정보를 분리 전달하였습니다.  
   - 이를 통해 판매자별로 정보를 커스터마이징하고 처리 속도를 최적화할 수 있었습니다.

2. **장바구니 담기 로직 최적화**  
   - 사용자가 장바구니에 물품을 담을 때, 동일한 품목의 옵션이 이미 담겨 있다면 제외하여 출력하는 로직을 구현하였습니다.  
   - 중복 옵션을 제거함으로써 사용자 경험을 개선하고, 데이터 처리의 불필요한 중복을 방지했습니다.

3. **Spring JPA의 `Specification` 활용**  
   - Spring JPA의 `Specification` 기능을 사용하여 동적인 `WHERE` 조건절을 쉽게 생성하고 적용할 수 있었습니다.  
   - 복잡한 쿼리 로직도 간결하고 유지보수 가능한 형태로 구현할 수 있었습니다.


# 협업자료
발표 ppt 
https://www.miricanvas.com/v/142oczu
