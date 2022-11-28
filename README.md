# **⭐ Starry Night : 멀기만 했던 별들과 가까워 지는 밤**

![Logo](/uploads/af48a2b9e7a57bb61e8ab3d76f3dba4f/KakaoTalk_20221121_011112771.png)

## **[Starry Night 링크](https://starry-night.kr/)**

## **[UCC 링크 - 소개 영상 보기](https://www.youtube.com/watch?v=eVtlH42FHsQ)**

---

## 📖 주제

실시간 천체 위치를 반영한 PC + VR 기반 멀티플레잉 **플라네타리움** + 별자리 신화들을 바탕으로 한 **3D 게임** + 웹 기반 **다락방 꾸미기**

---

## 📅 **프로젝트 진행 기간**

2022.10.10(월) ~ 2022.11.20(일) [****42****일간 진행] - SSAFY 7기 2학기 자율프로젝트

---

## 🤔 기획 배경

- **빛 공해**
    - 대한민국은 빛 공해 세계 2위, 국토의 89.4%가 빛 공해 지역입니다.
    - 별 관측을 위해 장소, 시간, 환경, 장비 등 조건을 갖추지 않으면 별을 보기 힘든 시대가 되었습니다.
    - 별과 멀어진 현대 도시인들을 위해 별과 가까워 질 수 있는 서비스를 기획하게 되었습니다.

- **별과 별자리에 대한 관심**
    - 별과 별자리에 대해 잘 알지 못하는 사람들을 위해 별자리 설화 및 실시간으로 이동하는 별의 정보들을 제공하는 교육적인 컨텐츠를 기획하게 되었습니다.

- **활용성**
    - 우주과학에 대한 관심 증대
    - 실시간 별 관측 오픈소스 배포를 통한 다양한 외부 컨텐츠 개발에 기여
    - 학교, 과학관 등 교육적 체험 컨텐츠를 제공
    

---

## 🥌 서비스 특징

- **실시간 별 관측**
    - 별의 정보
        - **적경**, **적위**, **시등급**, **색깔**이 포함된 별 데이터를 제공
        - 시등급으로 별의 크기 지정 & 실제 별의 색깔 반영
        
    - 위치에 따른 밤하늘 변경
        - **15**개의 도시에서 별과 별자리를 보여줌
        - 현재 시간을 **해당 지역의 시간**으로 변경
        - 지역의 **위도**, **경도**, **시간**으로 천구의 회전량 계산
        - 회전량 만큼 천구 회전
        - → 지구의 자전에 따라서 실시간으로 회전하는 별 구현
        
- **밤하늘 보기**
    - 맵
        - 모닥불, 풀, 텐트 등 다양한 오브젝트들 및 풀벌레 소리, 모닥불 소리, 다양한 백색소음을 사용하여 현장에서 별을 보는 느낌을 제공
    - 사용자들끼리 즐길 수 있는 **불꽃놀이**, **스타 찾기** 컨텐츠 제공
        - 스타 찾기: 아이템을 먹어 특수 능력(점프 강화, 스피드 강화, 거대화, 밝게 빛나는 효과)를 발휘
    - 사용자간 **텍스트 채팅**, **음성 채팅** 기능 제공
    - **멀티플레이** 제공
    - **VR**(Oculus quest 2(VR 기기)를 통해 밤하늘 보기를 플레이 가능)
    - **Blender**를 통해 모델링한 오브젝트 구현
    
- **신화 게임**
    - 5개의 별자리 스토리
        - 사자자리, 처녀자리, 페르세우스자리, 카시오페아자리, 거문고자리
        - 한 스토리당 플레이 타임 **10분**을 기준으로 함
        
    - 스토리마다 제공되는 미니 게임
        - 사물과 상호작용, 미로 탈출, 공포 게임, 전투, 점프맵 등 다양한 **미니게임**을 통해 스토리 각각의 개성을 주어 지루하지 않는 플레이 제공
        
    - 10개의 다양한 맵
        - asset을 사용후 리모델링을 통해 **사용자의 이동거리를 고려**
        - 시간에 따른 skybox 변화, 날씨 환경에 따른 맵 오브젝트 변화를 주어 맵들에 **각기 다른 성격**을 담아냄
        - **성능 저하를 고려**하여 collider 설정을 mesh → box 로 변경
        - 탈출을 해야하는 넓은 미로 맵의 경우 난이도와 플레이 타임을 조절하기 위해 미니맵을 제공
    
    - 22개의 퀘스트
        - 별자리 설화를 퀘스트의 내용에 담아 사용자가 주인공을 돕는 서브 주인공으로 플레이
    
    - 별(재화)
        - 추가 컨텐츠 다락방을 꾸밀 수 있는 재화를 맵 곳곳에 숨겨 **맵을 탐방할 수 있는 요소**를 추가
    
    - 사운드
        - 배경, 캐릭터, 전투 및 각종 오브젝트에 대한 사운드 제공
        - 자연스러운 연출을 위하여 **애니메이션 사이에 event 함수를 생성**하여 사운드를 부여
    
    - 시야
        - 일반적인 맵은 **3인칭**, 미로가 동반된 공포게임의 경우 몰입감을 위하여 시야가 제한된 **1인칭** 제공
    
    - 애니메이션
        - NPC
            - 플레이어를 따라가는 NPC를 **navmeshagent**를 사용하여 구현
        - 적
            - Idle, Patrol, Chase, Attack 상태로 나누어 플레이어와의 기본적인 전투를 구현

- **다락방**
    - 게임에서 획득한 별(재화)을 통해 가구를 구매하여 자신만의 다락방을 꾸미기 가능
    - **유성타기**를 통하여 다른 사용자들의 다락방을 구경 가능

---

## 📝 **주요 기능**

### 회원 관리

- 카카오, 구글 **소셜로그인** 제공
- 닉네임 변경 가능

### 메인페이지

- 제공하는 기능을 한 눈에 볼 수 있게 페이지 단위로 설명을 제공
- 백그라운드에 신화 게임의 별자리들을 그려 그 위에 획득한 별들을 빛나게 만들어 **게임의 진행 사항을 한눈에 표시**

### 책 펼치기

- **별 보러 가기**를 통해 신화 게임 플레이
- **신화 읽기**를 통해 별자리 신화에 대한 자세한 이야기 및 정보 제공
- **튜토리얼**을 제공하여 게임에서 필요한 조작법 및 가이드 제공

### 밤하늘 보기

- **멀티플레이**를 제공(PC & VR)
- (**PC, VR) 버전**을 다운로드하여 밤하늘 보기를 플레이 가능
- **튜토리얼**을 통해 게임 다운로드, 컨텐츠 소개, 조작 방법을 상세히 제공

### 방 꾸미기

- 현재 가지고 있는 가구들을 이용하여 다락방을 꾸밀 수 있는 기능 제공
- **Drag & Drop**을 통한 편리한 배치, 가구 회전 기능 제공
- **유성타기**를 통해 다른 무작위 사용자의 방을 구경할 수 있음

### 상점가기

- 신화 게임 속 획득한 별들을 이용하여 **180**가지 이상의 가구를 구매 가능

---

## ⌨️ **주요 기술**

**Backend**

- IntelliJ IDE 2022.1.3(Ultimate Edition) 11.0.15 + 10-b2043.56 amd64
- Spring Security
- Query DSL
- Swagger
- Hibernate
- JWT
- SpringBoot

**Frontend**

- Node.js
- React 18.2.0
- Recoil 0.7.5
- Tailwind CSS
- TypeScript

**Unity**

- Unity 2021.3.11f
- Photon Unity Networking 2.41
- XR Interaction Tool Kit

**CI/CD**

- AWS EC2 Ubuntu 20.04 LTS
- Jenkins 2.361.3
- NGINX 1.23.2
- SSL 인증서
- MySQL
- gabia

---

## 🔧 **협업 툴**

- GitLab
- Notion
- JIRA
- MatterMost
- Webex
- Discord
- Gather Town

---

## 🏗️ **프로젝트 파일 구조**

### BE

```sql
backend
├─gradle
│  └─wrapper
└─src
    ├─main
    │  ├─java
    │  │  └─starrynight
    │  │      ├─api
    │  │      │  ├─controller
    │  │      │  ├─dto
    │  │      │  │  ├─game
    │  │      │  │  ├─member
    │  │      │  │  ├─room
    │  │      │  │  └─store
    │  │      │  └─service
    │  │      ├─config
    │  │      │  ├─auth
    │  │      │  ├─jwt
    │  │      │  ├─querydsl
    │  │      │  └─swagger
    │  │      ├─db
    │  │      │  ├─entity
    │  │      │  └─repository
    │  │      ├─enums
    │  │      ├─exception
    │  │      └─interceptor
    │  └─resources
    └─test
        └─java
            └─starrynight
```

### **FE**

```sql
.
├── public
│   ├── Build
│   │   ├── cassiopeia
│   │   ├── leo
│   │   ├── lyra
│   │   ├── perseus
│   │   └── virgo
│   ├── Download
│   └── assets
│       ├── constellation
│       ├── furniture
│       ├── main
│       ├── others
│       ├── team
│       ├── thumbnail
│       └── tutorial
└── src
    ├── api
    ├── components
    │   ├── book
    │   ├── myroom
    │   ├── navbar
    │   └── tutorial
    ├── pages
    ├── recoil
    │   └── member
    └── utils
```

---

## 👥 **팀원 역할**

### BackEnd

### FrontEnd

### 👩🏻‍💻 신슬기 - 팀장, Game

### 👩🏻‍💻 안지영 - Web, VR

### 👨🏻‍💻 황승주 - VR, DevOps

### 👩🏻‍💻 채송지 - Web, Design

### 👨🏻‍💻 박희조 - Game, UCC

### 👨🏻‍💻 박종민 - Game

---

## **✔ 프로젝트 산출물**

[시연 시나리오](https://www.notion.so/b20030b30ee5453c9da5d9f8cd680049)

[**ERD**](https://www.notion.so/ERD-711741c69a0b48f8a5774769dcd526d7)

[아키텍쳐](https://www.notion.so/e1ed17e0f777440aaa3a4abb82d7c978)

[포팅 매뉴얼](https://www.notion.so/210edda704c04d9d80a3f8f4bba2ea44)

[기능 명세서](https://www.notion.so/0491e225bf074ffdb1cabafae64bf87b)

[와이어프레임](https://www.notion.so/8090b799c29c4699b08e2c4ac326dcc4)

---

## 🖥️ **서비스 화면**

### 메인페이지

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/a72e7d46-96d8-4bda-a472-2acf71f4fa05/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/322bcff3-ab80-4570-ba63-fcdfba22269e/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/6f75e50c-47d6-456b-b5d4-32b147e04c96/Untitled.png)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b1c65afd-905f-431e-a2e6-2f448a5239fd/Untitled.png)

![quest](/uploads/52a36915c33dcefcf7f4acf6cde67729/quest.gif)

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/55323fbb-cce3-4e8f-9d81-f567e3ff2f7a/Untitled.png)

- Starry Night에서 제공하는 서비스들을 한눈에 볼 수 있습니다.

### 로그인

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1c7a8e50-e374-448f-b71c-e9c61141aa73/Untitled.png)

- 카카오 & 구글 소셜 로그인을 제공

### 다락방

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/7e663cab-b60d-4bf3-8d05-13ec3813ef83/Untitled.png)

- 메인 서비스 3가지를 이용할 수 있음
    - **신화 게임**
    - **밤하늘 보기**
    - **방 꾸미기**

![other-room.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/8ff0c9ae-5175-4418-8095-165622082edc/other-room.gif)

- **유성 타기** - 다른 사용자들의 다락방을 구경할 수 있음

### 책 펼치기

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/abed8528-96e4-424b-a763-625fbb0b9e29/Untitled.png)

- 책 펼치기 - 신화 게임들을 플레이할 수 있는 공간

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/b90ea3d0-eada-4b76-be10-ea0cac1865f6/Untitled.png)

- 신화 읽기 - 클리어한 신화 게임의 별자리에 대한 정보들을 제공

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/36dce1fa-336d-48c0-b982-d1c6c6794787/Untitled.png)

- 튜토리얼 - 신화 게임의 조작법을 설명하는 게임 가이드

### 신화 게임

![virgo.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c2c114a1-00ca-4692-a49a-81ecd8388bd7/virgo.gif)

- 처녀자리 - 물체와 상호작용

![quest.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/77bae4c7-57a5-4cbb-a370-0b499a808734/quest.gif)

- 별자리 신화 관련 퀘스트

![lion.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/eef1124c-c226-4a2f-b9e2-406764f03770/lion.gif)

- 사자자리 - 미니게임(전투)

![perseus.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/881c8224-77c0-4208-86b6-1881a47c5b1f/perseus.gif)

- 페르세우스자리 - 미니게임(공포게임)

![cassiopeia.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/0bc6dc8b-1b83-4927-9a7c-89917d194fd3/cassiopeia.gif)

- 카시오페이아자리 - 미니게임(미로)

![lyra.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/efb284ac-1bba-4a7a-ae8a-bb635387c2c9/lyra.gif)

- 거문고자리 - 미니게임(점프맵)

### 밤하늘 보기

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/cda5d8af-e39b-4a29-9069-ee05271e0373/Untitled.png)

- PC로 별 보기 / VR로 별 보기 - 2가지 모드로 플레이 가능

![Untitled](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/22a8ec70-d495-4476-b4ba-736b1ee2a3de/Untitled.png)

- 튜토리얼 - (다운로드, 컨텐츠 소개, 조작 방법)에 관련된 정보를 사용자에게 제공)

![firework.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/78068fff-623a-4cda-9fdb-9fa6bc4f07ac/firework.gif)

- 불꽃 놀이

![star-item.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/1c2d700d-822a-4cfc-a6e8-6aabf35df9b8/star-item.gif)

- 스타(아이템) 획득을 통한 특수능력 부여

![change-star.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/40ef00e2-f7de-4efa-abf9-a3bb8e134b45/change-star.gif)

- 도시 변경으로 별자리 위치 변경

![star-information.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/5c8a9b86-b40e-42a3-9439-2ad6fe22da0e/star-information.gif)

- 별을 클릭하여 별의 자세한 정보 확인

### 상점 가기

![shop-buy.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/42ef3352-45cc-485f-bb99-de51117fa66c/shop-buy.gif)

- 신화 게임에서 얻은 재화로 방을 꾸밀 수 있는 아이템을 구매 가능

### 방 꾸미기

![change-room.gif](https://s3-us-west-2.amazonaws.com/secure.notion-static.com/c3a831a2-30f5-417f-a22d-a148c982273a/change-room.gif)

- 구매한 가구를 이용하여 자신의 다락방을 꾸밀 수 있습니다.
