# 💩 poopy-map (대똥여지도)

> **공중화장실 영역 전개 & AI 건강 분석 게이미피케이션 플랫폼**

![License](https://img.shields.io/badge/license-MIT-green)
![Version](https://img.shields.io/badge/version-0.1.0-blue)
![Status](https://img.shields.io/badge/status-MVP%20Development-orange)

## 📋 프로젝트 개요
**poopy-map** 은 단순한 공중화장실 찾기 서비스를 넘어, 사용자 참여형 경쟁 시스템과 AI 기반 건강 분석을 결합한 **헬스케어 게이미피케이션 서비스** 구축.

- **핵심 가치** : 재미(Fun), 건강(Health), 공공성(Public)
- **차별점** : '영역 전개(점령)' 개념의 게임 요소 도입 및 프라이버시가 보장된 AI 배변 분석
- **데이터 원칙** : 공공데이터(공중화장실)만을 활용하여 신뢰성 확보 및 사유지 이슈 배제

---

## 🚀 주요 기능

### 1. 🗺️ 지도 및 탐험 (Map & Exploration)
- **영역 전개** : 사용자가 방문 및 평가한 화장실 위치에 고유 마커 표시 및 영토 점령 시각화
- **똥그라미** : 활동 반경 데이터를 기반으로 나만의 영역 지도 생성
- **길찾기** : Kakao Maps API 연동을 통한 최단 경로 및 이동 시간 안내

### 2. 🎮 게이미피케이션 (Gamification)
- **계급 시스템** : 활동량에 따라 **소변인 → 중변인 → 대변인** 등급 승급
- **업적 및 뱃지** :
  - `싱글똥` (혼자 방문 체크인)
  - `쾌변왕` (건강 점수 상위 10%)
  - `똥믈리에` (상세 평가 50회 이상 작성)
- **경쟁 시스템** : 지역별/전국별 포인트 랭킹 제공

### 3. 🩺 AI 건강 분석 (Health Analysis)
- **변역(Poostlation)** : 촬영된 배변 이미지를 AI가 분석하여 브리스톨 대변 척도 및 건강 상태 판별
- **Privacy First** : **촬영 이미지는 서버에 저장되지 않으며 분석 즉시 메모리에서 소멸 (Zero Data Retention)**
- **리포트** : 월간/연간 배변 주기 및 건강 변화 추이 리포트 생성

### 4. 📝 똥믈리에 평가 (Evaluation)
- **필수 체크** : 청결도, 휴지 구비 여부, 비데 유무, 수압 상태
- **편의 시설** : 기저귀 교환대, 파우더룸, 장애인 전용 시설 정보 공유

---

## 🛠 기술 스택 (Tech Stack)

| 구분 | 기술 (Stack) | 비고 |
| :--- | :--- | :--- |
| **Client** | React Native / Flutter (TBD) | 크로스 플랫폼 앱 개발 |
| **Server** | Node.js / Python (FastAPI) | REST API 및 AI 모델 서빙 |
| **AI/ML** | TensorFlow / PyTorch | 이미지 분류(Classification) 모델 |
| **Database** | PostgreSQL, Redis | 위치 데이터(PostGIS), 세션 관리 |
| **Infra** | AWS / GCP | 클라우드 인프라 구축 |
| **External API** | Kakao Maps API, 공공데이터포털 | 지도 및 공중화장실 데이터 |

---

## 🔒 개인정보 처리 방침 (Privacy Policy)
본 프로젝트는 사용자의 민감 정보(건강 데이터) 보호를 최우선 가치로 삼음.

1. **이미지 미저장 (No Image Storage)**
   - AI 분석을 위해 촬영된 이미지는 분석 완료 즉시 휘발성 메모리에서 영구 삭제
   - 서버 스토리지에 원본 이미지를 절대 저장하지 않음

2. **데이터 익명화 (Anonymization)**
   - 분석 결과(텍스트 데이터)는 개인 식별 정보와 분리하여 암호화 저장
   - 통계 목적으로 활용 시 철저한 비식별화 처리 수행

3. **공공 데이터 준수 (Public Data Compliance)**
   - 사유지 화장실 정보는 수집하지 않으며, 공공 데이터 포털의 라이선스 규정을 준수

---

## 👥 팀원 (Team FlowCycle)

| 이름 | 역할 (Role) | 담당 업무 | GitHub |
| :--- | :--- | :--- | :--- |
| **cj** | PM / Planning | 제품 기획, UX/UI 설계, 요구사항 정의 | [@O_CJ](https://github.com/cjoh0407-ctrl) |
| **jh** | Data Engineer | 공공데이터 수집/전처리, 라이선스 검토 | [@studio](https://github.com/jhyeon9185) |
| **hy** | AI / Security | 건강 분석 모델 개발, 보안 아키텍처 설계 | [@gHaO](https://github.com/hayohio-bit) |
| **yj** | Core Dev | 지도 API 연동, LBS 로직 구현, 성능 최적화 | [@Jaden](https://github.com/every-git) |

---

## 📂 디렉토리 구조 (Directory Structure)

```bash
poopy-map/
├── .github/          # GitHub Action 및 Issue Template
├── client/           # 모바일 어플리케이션 소스코드
├── server/           # 백엔드 API 서버 소스코드
├── ai-engine/        # [하영] AI 건강 분석 모델 및 전처리 로직
├── data/             # [종현] 공공데이터셋 및 크롤링 스크립트
├── docs/             # 기획서, 회의록, API 명세서
└── README.md         # 프로젝트 메인 설명서
```

---

## ⚡ 시작하기 (Getting Started)
**사전 요구사항 (Prerequisites)**
- Node.js 18.0.0+

- Python 3.9+

- PostgreSQL 14+

**설치 및 실행 (Installation)**
  **1. Repository Clone**
  
  ```Bash
  git clone [https://github.com/organization/poopy-map.git](https://github.com/organization/poopy-map.git)
  ```
  
  **2. Client Setup**
  ```Bash
  cd client
  npm install
  npm run start
  ```
  
  **3. Server Setup**
  ```Bash
  cd server
  pip install -r requirements.txt
  uvicorn main:app --reload
  ```

---

## 📜 License
This project is licensed under the MIT License - see the [LICENSE](https://www.google.com/search?q=LICENSE) file for details.

Data License : 공공누리 제1유형 (출처표시) 준수
