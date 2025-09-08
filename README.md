# 💻 1. 프로젝트 기획서

## 📄 1-1. 프로젝트 개요

- **프로젝트명:** Newphere 📰
- **진행 기간:**

  - 2025.07.18 ~ 2025.09.10

- **설명:**  
  뉴스 수집 및 검색 플랫폼의 주요 서비스(회원기능, 뉴스 크롤링, 툴팁, 개인화 추천, 뉴스레터, 스크랩, 뉴스 요약 등)를 MSA 아키텍처 기반으로 구현하고,  
  이후 CI/CD 및 클라우드 배포 환경까지 실제 서비스 운영 경험을 목표로 한 뉴스 플랫폼 프로젝트

## 👨‍💼 1-2. 팀원 구성

| 김지환                                                           | 박준서                                                           | 박창준                                                           | 유지은                                                           | 이채희                                                           |
| ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- | ---------------------------------------------------------------- |
| ![김지환](https://avatars.githubusercontent.com/u/106491547?v=4) | ![박준서](https://avatars.githubusercontent.com/u/106491548?v=4) | ![박창준](https://avatars.githubusercontent.com/u/106491549?v=4) | ![유지은](https://avatars.githubusercontent.com/u/123456789?v=4) | ![이채희](https://avatars.githubusercontent.com/u/106491551?v=4) |
| [GitHub](https://github.com/FerryLa)                             | [GitHub](https://github.com/Berry-mas)                           | [GitHub](https://github.com/changjunpark13)                      | [GitHub](https://github.com/yde222)                              | [GitHub](https://github.com/apocalcal)                           |

## 📅 1-3. 프로젝트 설명

본 프로젝트는 MSA 아키텍처 기반의 뉴스 검색 및 수집 플랫폼 프로젝트이다.
뉴스 서비스의 대표적인 기능인 회원기능, 뉴스 크롤링, 중복제거, 개인화 추천, 뉴스레터 발송 기능, 툴팁, 검색기능, 스크랩/컬렉션, 뉴스요약을 중심으로 구현했으며,
JWT 기반의 로그인 및 인증을 적용해 실제 서비스와 유사한 사용자 경험을 제공한다.
사용자는 개인화된 뉴스 추천, 뉴스레터 수신, 스크랩/컬렉션, 뉴스 요약 등 다양한 기능을 사용할 수 있다.
개발이 완료된 후에는 Jenkins, AWS 등의 DevOps 도구를 활용하여 자동화된 배포 환경을 구축했다.

## 🔄 1-4. 목표 및 범위

본 프로젝트의 목표는 뉴스 플랫폼의 주요 서비스 흐름과 핵심 기능을 MSA 구조에서 직접 구현하며,
실무에서 요구하는 "회원기능, 뉴스 크롤링, 중복제거, 개인화 추천, 뉴스레터 발송 기능, 툴팁, 검색기능, 스크랩/컬렉션, 뉴스요약" 등 개발을 직접 경험하는 데 있다.

또한 CI/CD, 클라우드(AWS) 환경에서의 자동화된 배포 파이프라인 구축 등
개발부터 배포까지 전 과정을 경험하고, 실제 서비스와 유사한 환경을 구축하는 것을 목표로 한다.

## 👤 1-5. 타겟 사용자

- **일반 사용자**
  : 뉴스를 탐색하고 개인화된 추천을 받으며, 스크랩/컬렉션 및 뉴스레터 수신 등 뉴스 서비스를 이용하는 고객

- **관리자**
  : 뉴스 승격, 통계 데이터, 사용자 관리 등 서비스 데이터와 콘텐츠를 관리하는 관리자 계정

## 🔢 1-6. 주요 기능 목록

- **회원가입 및 로그인**
  : 이메일 기반 회원가입/로그인, JWT 인증 적용
- **뉴스 크롤링 및 중복제거**
  : 네이버 뉴스 크롤링, Python 기반 SBERT 중복제거 시스템
- **개인화 뉴스 추천**
  : 사용자 선호도 기반 맞춤형 뉴스 추천 시스템
- **뉴스레터 발송**
  : 개인화된 뉴스레터 생성 및 이메일 발송
- **뉴스 스크랩 및 컬렉션**
  : 뉴스 스크랩, 컬렉션 생성 및 관리 기능
- **뉴스 분석 및 툴팁**
  : 어려운 단어 자동 분석 및 툴팁 제공
- **뉴스 신고 기능**
  : 부적절한 뉴스 신고 및 관리 기능
- **AI 요약**
  : OpenAI 기반 뉴스 요약 기능

## 📋 1-7. 담당 기능

| 담당자 | 서비스명 (`영문-service`)          | 주요 역할/설명                                                 |
| ------ | ---------------------------------- | -------------------------------------------------------------- |
| 김지환 | **AI 요약 (`flaskapi`)**           | Flask API 및 AI 요약 산출물 관리                               |
| 박준서 | **배포/크롤링/툴팁/추천/중복제거** | 배포 작업, 크롤링, 툴팁, 개인화 추천 로직, 중복제거            |
| 박창준 | **뉴스/스크랩/신고 서비스**        | 뉴스 서비스, 스크랩 기능, 신고 기능                            |
| 유지은 | **프론트엔드/뉴스레터/뉴스필터링**            | Next.js 기반 프론트엔드 개발, 뉴스레터 서비스, UI/UX 구현 ,개인화,트렌딩,검색/필터링 뉴스      |
| 이채희 | **회원/보안/인프라**               | 회원 기능, 보안 및 인프라, Config, Gateway, Discovery, Swagger |

## 🌐 1-8. MSA 식 구조

| 모듈명                   | 기능 역할                                                          | 담당자 |
| ------------------------ | ------------------------------------------------------------------ | ------ |
| **`news-service`**       | 뉴스 CRUD, 스크랩 기능, 신고 기능, 트렌딩 뉴스, 카테고리 관리      | 박창준 |
| **`user-service`**       | 회원가입/로그인, JWT 인증, 마이페이지, 읽기 이력, 사용자 정보 관리 | 이채희 |
| **`crawler-service`**    | 네이버 뉴스 크롤링, 파일서버 연동, 크롤링 데이터 관리              | 박준서 |
| **`newsletter-service`** | 개인화 뉴스레터 생성, 이메일 발송, 구독 관리                       | 유지은 |
| **`tooltip-service`**    | 뉴스 본문 NLP 분석, 어려운 단어 툴팁 제공, 단어 정의 관리          | 박준서 |
| **`dedup-service`**      | Python 기반 SBERT 중복제거, FastAPI 서비스                         | 박준서 |
| **`flaskapi`**           | OpenAI 기반 뉴스 요약, AI 기능 제공                                | 김지환 |
| **`gateway-service`**    | API Gateway, 라우팅, 인증, 로드밸런싱                              | 이채희 |
| **`discovery-service`**  | Eureka 서버, 서비스 등록/발견                                      | 이채희 |
| **`config-service`**     | 공통 환경설정, JWT 토큰 및 마이크로서비스 중앙 설정 관리           | 이채희 |

---

# 📚 2. Newphere 요구사항 정의서

## 📜 2-1. 프로젝트 개요

- **목표**: 사용자가 다양한 뉴스 정보를 쉽고 편리하게 조회·구독할 수 있는 개인화 뉴스 플랫폼 서비스 구현
- **구성**: MSA 기반
- **주요 기능**: 회원 관리, 뉴스 크롤링/중복제거, 개인화 추천, 뉴스레터, 스크랩/컬렉션, AI 요약 등

## 🔍 2-2. 사용자 영역 요구사항

### 🔐 2-3. 회원 관리

| TC ID | 기능 명                        | 목적/설명                      |
| ----- | ------------------------------ | ------------------------------ |
| US-01 | 회원 중복 체크                 | 중복 회원(이메일) 가입 차단    |
| US-02 | 회원가입 성공                  | 신규 회원 정상 가입            |
| US-03 | 회원탈퇴 성공                  | 회원 탈퇴 요청 정상 처리       |
| US-04 | 마이페이지 정보 조회           | 로그인한 사용자 정보 조회      |
| US-05 | 회원 정보 수정                 | 사용자가 자신의 정보 수정 가능 |
| US-06 | 회원정보 수정 전 비밀번호 확인 | 정보 수정 전 비밀번호 확인     |
| US-07 | 비밀번호 변경                  | 비밀번호 수정 정상 동작        |
| US-08 | 로그인 성공                    | 정상 로그인                    |
| US-09 | 토큰 재발급                    | accessToken 만료 시 재발급     |
| US-10 | 로그아웃                       | 정상 로그아웃 처리             |

---

### 📰 2-4. 뉴스 관리

| TC ID | 기능 명              | 목적/설명                |
| ----- | -------------------- | ------------------------ |
| NS-01 | 뉴스 전체 목록 조회  | 모든 뉴스 정상 조회      |
| NS-02 | 특정 뉴스 상세 조회  | 단일 뉴스 상세 정보 조회 |
| NS-03 | 뉴스 검색/필터링     | 조건 검색된 뉴스만 반환  |
| NS-04 | 카테고리별 뉴스 조회 | 카테고리별 뉴스만 조회   |
| NS-05 | 트렌딩 뉴스 조회     | 인기 뉴스 조회           |
| NS-06 | 개인화 뉴스 추천     | 사용자 맞춤 뉴스 추천    |
| NS-07 | 뉴스 조회수 증가     | 뉴스 조회 시 조회수 증가 |
| NS-08 | 뉴스 스크랩          | 뉴스 스크랩 기능         |
| NS-09 | 뉴스 신고            | 부적절한 뉴스 신고 기능  |
| NS-10 | 뉴스 요약            | AI 기반 뉴스 요약 기능   |

---

### 📌 2-5. 스크랩 및 컬렉션 관리

| TC ID | 기능 명            | 목적/설명                    |
| ----- | ------------------ | ---------------------------- |
| SC-01 | 뉴스 스크랩        | 관심 뉴스 스크랩 저장        |
| SC-02 | 스크랩 목록 조회   | 사용자 스크랩 뉴스 목록 조회 |
| SC-03 | 스크랩 해제        | 스크랩한 뉴스 해제           |
| SC-04 | 컬렉션 생성        | 뉴스 컬렉션 생성             |
| SC-05 | 컬렉션 관리        | 컬렉션 수정/삭제/조회        |
| SC-06 | 컬렉션에 뉴스 추가 | 컬렉션에 뉴스 추가/제거      |

---

### 📧 2-6. 뉴스레터 관리

| TC ID | 기능 명              | 목적/설명                 |
| ----- | -------------------- | ------------------------- |
| NL-01 | 뉴스레터 구독 등록   | 뉴스레터 구독 신청        |
| NL-02 | 뉴스레터 구독 해지   | 뉴스레터 구독 해지        |
| NL-03 | 개인화 뉴스레터 생성 | 사용자 맞춤 뉴스레터 생성 |
| NL-04 | 뉴스레터 이메일 발송 | 구독자에게 뉴스레터 발송  |
| NL-05 | 뉴스레터 미리보기    | 뉴스레터 내용 미리보기    |

---

### 🤖 2-7. AI 기능 관리

| TC ID | 기능 명        | 목적/설명                 |
| ----- | -------------- | ------------------------- |
| AI-01 | 뉴스 요약 생성 | OpenAI 기반 뉴스 요약     |
| AI-02 | 뉴스 본문 분석 | 어려운 단어 자동 분석     |
| AI-03 | 단어 툴팁 제공 | 어려운 단어 정의 툴팁     |
| AI-04 | 중복 뉴스 제거 | SBERT 기반 중복 뉴스 제거 |

---

## 🤝 2-8. 관리자 영역 요구사항

| TC ID | 기능 명              | 목적/설명                      |
| ----- | -------------------- | ------------------------------ |
| AD-01 | 관리자 로그인        | 관리자 계정 로그인             |
| AD-02 | 관리자 대시보드 조회 | 대시보드에 집계 정보 정상 조회 |
| AD-03 | 뉴스 승격 관리       | 크롤링된 뉴스를 승격하여 노출  |
| AD-04 | 뉴스 관리            | 뉴스 등록/수정/삭제 관리       |
| AD-05 | 사용자 관리          | 사용자 목록 조회 및 관리       |
| AD-06 | 통계 데이터 조회     | 서비스 이용 통계 조회          |
| AD-07 | 크롤링 관리          | 뉴스 크롤링 상태 및 설정 관리  |

---

# 📌 3. 세부 기능 설명

- [**`MSA 아키텍쳐 설계`**](https://www.notion.so/coffit23/MSA-215a02b1ffb1818d91fece9cc5192253)
- [**`웹 크롤러 및 수집 데이터`**](https://docs.google.com/document/d/1mkgBw0V15dasDCe4mlciuKx1zeHG7Hc5/edit)
- [**`API 명세서`**](https://docs.google.com/document/d/1NxqWpiikF3fV1PJUAb-ISNFM5NzjNZZC/edit#bookmark=id.53cc1fgmbu4v)
- [**`UI 테스트 케이스`**](https://docs.google.com/spreadsheets/d/1bhWdQKfI2ivGchVSLMq2QwAOm_TKZzRH/edit?gid=1536679567#gid=1536679567)
- [**`스토리보드`**](https://drive.google.com/drive/folders/1-EGTHDVHXlZCfiaTBf5pRU9s7Mmsmc47)
- [**`프롬프트 엔지니어링 설계서`**](https://docs.google.com/document/d/1NAWskTLEY75X5-YlqlhPQV7chCsTsKgAP9L9l3eI2Kc/edit?tab=t.0#heading=h.6tv6xuec6c9w)
- [**`인터페이스 설계서`**](https://docs.google.com/spreadsheets/d/1lqDinzAhGUfUX7_FWZeIxaGgFz9S08Bd/edit?usp=drive_web&ouid=104302817025522008655&rtpof=true)
- [**`프로젝트 테스트 결과서`**](https://drive.google.com/drive/folders/1bvNQKSayj9y3JubFmjt-lynXfpGELO75)
- [**`CI/CD 설계서`**](https://drive.google.com/drive/folders/1CBGAeIK7Cx7DLJ2mrUkX546weJZ6BpjD)
- [**`테스트 결과서`**](https://docs.google.com/spreadsheets/d/12fQDrjJet3mgjH2y7VdR6OhRPn0goZLoTigsx_pi_W4/edit?gid=0#gid=0)
- [**`테스트 케이스`**](https://docs.google.com/spreadsheets/d/13EvwtY9Xg2dPQmcyKJw0D-wzyc4WJ7Pr/edit?usp=drive_web&ouid=104302817025522008655&rtpof=true)

---

# 🛠 4. 기술 스택

## 🖥️ 4-1. 프론트엔드 기술 스택

| 항목                      | 사용 기술                                                                                                                                                                                                                                                                                                         |
| ------------------------- | ----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| **프론트엔드 언어**       | ![JavaScript](https://img.shields.io/badge/JAVASCRIPT-F7DF1E?style=for-the-badge&logo=javascript&logoColor=black) ![TypeScript](https://img.shields.io/badge/TYPESCRIPT-3178C6?style=for-the-badge&logo=typescript&logoColor=white)                                                                               |
| **프론트엔드 프레임워크** | ![Next.js](https://img.shields.io/badge/NEXT.JS-000000?style=for-the-badge&logo=next.js&logoColor=white) ![React](https://img.shields.io/badge/REACT-61DAFB?style=for-the-badge&logo=react&logoColor=black)                                                                                                       |
| **스타일링**              | ![Tailwind CSS](https://img.shields.io/badge/TAILWIND_CSS-38B2AC?style=for-the-badge&logo=tailwind-css&logoColor=white) ![CSS3](https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white)                                                                                           |
| **UI 컴포넌트**           | ![Shadcn/ui](https://img.shields.io/badge/SHADCN/UI-000000?style=for-the-badge&logo=shadcn&logoColor=white) ![Radix UI](https://img.shields.io/badge/RADIX_UI-161618?style=for-the-badge&logo=radix-ui&logoColor=white)                                                                                           |
| **상태 관리**             | ![React Context](https://img.shields.io/badge/REACT_CONTEXT-61DAFB?style=for-the-badge&logo=react&logoColor=black) ![Zustand](https://img.shields.io/badge/ZUSTAND-FF6B6B?style=for-the-badge&logo=zustand&logoColor=white)                                                                                       |
| **인증/소셜 로그인**      | ![Google OAuth](https://img.shields.io/badge/GOOGLE_OAUTH-4285F4?style=for-the-badge&logo=google&logoColor=white) ![Kakao Login](https://img.shields.io/badge/KAKAO_LOGIN-FFCD00?style=for-the-badge&logo=kakao&logoColor=black)                                                                                  |
| **공유 기능**             | ![Kakao Share](https://img.shields.io/badge/KAKAO_SHARE-FFCD00?style=for-the-badge&logo=kakao&logoColor=black)                                                                                                                                                                                                    |
| **개발 도구**             | ![ESLint](https://img.shields.io/badge/ESLINT-4B32C3?style=for-the-badge&logo=eslint&logoColor=white) ![Prettier](https://img.shields.io/badge/PRETTIER-F7B93E?style=for-the-badge&logo=prettier&logoColor=black) ![Vite](https://img.shields.io/badge/VITE-646CFF?style=for-the-badge&logo=vite&logoColor=white) |

## 🔧 4-2. 백엔드 기술 스택

| 항목                  | 사용 기술                                                                                                                                                                                                                                                                                                                                                                                                                            |
| --------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| **백엔드 언어**       | ![Java](https://img.shields.io/badge/JAVA-007396?style=for-the-badge&logo=java&logoColor=white) ![Python](https://img.shields.io/badge/PYTHON-3776AB?style=for-the-badge&logo=python&logoColor=white)                                                                                                                                                                                                                                |
| **백엔드 프레임워크** | ![Spring](https://img.shields.io/badge/SPRING-6DB33F?style=for-the-badge&logo=spring&logoColor=white) ![Spring Boot](https://img.shields.io/badge/SPRINGBOOT-6DB33F?style=for-the-badge&logo=springboot&logoColor=white) ![FastAPI](https://img.shields.io/badge/FASTAPI-009688?style=for-the-badge&logo=fastapi&logoColor=white) ![Flask](https://img.shields.io/badge/FLASK-000000?style=for-the-badge&logo=flask&logoColor=white) |
| **데이터베이스**      | ![MySQL](https://img.shields.io/badge/MYSQL-4479A1?style=for-the-badge&logo=mysql&logoColor=white)                                                                                                                                                                                                                                                                                                                                   |
| **AI/ML**             | ![OpenAI](https://img.shields.io/badge/OPENAI-412991?style=for-the-badge&logo=openai&logoColor=white) ![SBERT](https://img.shields.io/badge/SBERT-FF6B6B?style=for-the-badge&logo=sentence-transformers&logoColor=white)                                                                                                                                                                                                             |
| **협업/버전관리**     | ![GitHub](https://img.shields.io/badge/GITHUB-181717?style=for-the-badge&logo=github&logoColor=white) ![Git](https://img.shields.io/badge/GIT-F05032?style=for-the-badge&logo=git&logoColor=white)                                                                                                                                                                                                                                   |
| **배포/운영**         | ![Docker](https://img.shields.io/badge/DOCKER-2496ED?style=for-the-badge&logo=docker&logoColor=white) ![Kubernetes](https://img.shields.io/badge/KUBERNETES-326CE5?style=for-the-badge&logo=kubernetes&logoColor=white) ![Jenkins](https://img.shields.io/badge/JENKINS-D24939?style=for-the-badge&logo=jenkins&logoColor=white) ![AWS](https://img.shields.io/badge/AWS-232F3E?style=for-the-badge&logo=amazonaws&logoColor=white)  |

---

# 🏗️ 5. 프론트엔드 아키텍처 및 구조

## 📁 5-1. 프로젝트 구조

```
app/
├── (admin)/              # 관리자 페이지 그룹
│   ├── admin/            # 관리자 대시보드
│   └── newsletter/       # 뉴스레터 관리
├── (auth)/               # 인증 관련 페이지 그룹
│   ├── auth/             # 로그인/회원가입
│   ├── forgot-password/  # 비밀번호 찾기
│   ├── oauth/            # 소셜 로그인
│   └── reset-password/   # 비밀번호 재설정
├── (news)/               # 뉴스 관련 페이지 그룹
│   └── news/             # 뉴스 목록/상세
├── (newsletter)/         # 뉴스레터 관련 페이지 그룹
│   └── newsletter/       # 뉴스레터 구독/관리
├── (user)/               # 사용자 관련 페이지 그룹
│   ├── mypage/           # 마이페이지
│   └── user/             # 사용자 정보
├── api/                  # API 라우트
└── components/           # 공통 컴포넌트

components/
├── ui/                   # Shadcn/ui 기본 컴포넌트
├── header.jsx            # 헤더 컴포넌트
├── footer.jsx            # 푸터 컴포넌트
├── NewsCard.jsx          # 뉴스 카드 컴포넌트
├── NewsletterTemplate.jsx # 뉴스레터 템플릿
└── ...                   # 기타 공통 컴포넌트

contexts/
├── MypageContext.jsx     # 마이페이지 상태 관리
└── ScrapContext.jsx      # 스크랩 상태 관리

hooks/
├── useInterests.js       # 관심사 관리 훅
├── useKakaoShare.js      # 카카오 공유 훅
├── useNewsletter.js      # 뉴스레터 훅
└── useSummary.jsx        # AI 요약 훅
```

## 🎯 5-2. 프론트엔드 주요 기능

### 🔐 인증 및 사용자 관리

- **소셜 로그인**: Google OAuth, Kakao Login 연동
- **JWT 토큰 관리**: 자동 토큰 갱신 및 만료 처리
- **사용자 인증**: 보호된 라우트 및 권한 기반 접근 제어
- **마이페이지**: 사용자 정보 수정, 구독 관리, 스크랩 관리

### 📰 뉴스 관련 기능

- **뉴스 목록**: 카테고리별, 트렌딩 뉴스 표시
- **뉴스 상세**: 상세 정보, 관련 뉴스, AI 요약
- **뉴스 검색**: 실시간 검색 자동완성, 필터링
- **뉴스 스크랩**: 개별 스크랩 및 컬렉션 관리
- **뉴스 공유**: 카카오톡 공유 기능

### 📧 뉴스레터 기능

- **구독 관리**: 카테고리별 뉴스레터 구독/해지
- **뉴스레터 미리보기**: 이메일 발송 전 미리보기
- **개인화 설정**: 관심사 기반 뉴스레터 커스터마이징

### 🤖 AI 기능

- **뉴스 요약**: OpenAI 기반 뉴스 요약
- **툴팁**: 어려운 단어 자동 분석 및 툴팁 제공
- **관련 뉴스**: AI 기반 관련 뉴스 추천

### 🎨 UI/UX 특징

- **반응형 디자인**: 모바일, 태블릿, 데스크톱 대응
- **다크/라이트 모드**: 테마 전환 기능
- **접근성**: WCAG 가이드라인 준수
- **성능 최적화**: 이미지 지연 로딩, 코드 스플리팅

## 🔄 5-3. 상태 관리 구조

### Context API 활용

- **MypageContext**: 마이페이지 관련 상태 (구독, 스크랩, 설정)
- **ScrapContext**: 스크랩 및 컬렉션 상태 관리
- **ThemeProvider**: 다크/라이트 모드 테마 관리

### 커스텀 훅 패턴

- **useInterests**: 사용자 관심사 관리
- **useKakaoShare**: 카카오 공유 기능
- **useNewsletter**: 뉴스레터 구독 관리
- **useSummary**: AI 요약 기능

## 🌐 5-4. API 통신 구조

### API 라우트 (Next.js App Router)

```
app/api/
├── auth/                 # 인증 관련 API
├── news/                 # 뉴스 관련 API
├── newsletter/           # 뉴스레터 API
├── users/                # 사용자 API
└── weather/              # 날씨 API
```

### 서비스 레이어

- **newsService.js**: 뉴스 관련 API 호출
- **newsletterService.js**: 뉴스레터 관련 API 호출
- **api-utils.js**: 공통 API 유틸리티 함수

---

# 📝 6. 회고

### `김지환`

- **주요 역할** : AI 요약 (Flask API 및 산출물 관리)
- **느낀 점** :

### `박준서`

- **주요 역할** : 배포 작업, 크롤링, 툴팁, 개인화 추천 로직, 중복제거
- **느낀 점** :

### `박창준`

- **주요 역할** : 뉴스 서비스, 스크랩 기능, 신고 기능
- **느낀 점** :

### `유지은`

- **주요 역할** : 프론트엔드, 뉴스레터 서비스
- **느낀 점** :

### `이채희`

- **주요 역할** : 회원 기능, 보안 및 인프라, Config, Gateway, Discovery, Swagger
- **느낀 점** :
