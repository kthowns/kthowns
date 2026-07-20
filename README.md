<div align="center">

## 🛠 Tech Stack & GitHub Stats

| Category | Technologies | GitHub Stats |
| :---: | :---: | :---: |
| **Languages** | <img src="https://img.shields.io/badge/Java-007396?style=flat&logo=Java&logoColor=white"> <img src="https://img.shields.io/badge/Kotlin-7F52FF?style=flat&logo=Kotlin&logoColor=white"> <img src="https://img.shields.io/badge/JavaScript-F7DF1E?style=flat&logo=JavaScript&logoColor=black"> |![Top Langs](https://github-readme-stats.shion.dev/api/top-langs/?username=kthowns&layout=compact&theme=radical) |
| **Backend** | <img src="https://img.shields.io/badge/Spring_Boot-6DB33F?style=flat&logo=SpringBoot&logoColor=white"> <img src="https://img.shields.io/badge/JSP-007396?style=flat&logo=Java&logoColor=white"> <img src="https://img.shields.io/badge/Flask-000000?style=flat&logo=Flask&logoColor=white"> | **Infrastructure** <br> <img src="https://img.shields.io/badge/Docker-2496ED?style=flat&logo=Docker&logoColor=white"> <img src="https://img.shields.io/badge/Linux-FCC624?style=flat&logo=Linux&logoColor=black"> <img src="https://img.shields.io/badge/AWS-232F3E?style=flat&logo=amazon-aws&logoColor=white"> <img src="https://img.shields.io/badge/Azure-0078D4?style=flat&logo=microsoft-azure&logoColor=white"> |
| **Database** | <img src="https://img.shields.io/badge/MySQL-4479A1?style=flat&logo=MySQL&logoColor=white"> <img src="https://img.shields.io/badge/PgSQL-336791?style=flat&logo=postgresql&logoColor=white"> <img src="https://img.shields.io/badge/Redis-DC382D?style=flat&logo=Redis&logoColor=white"> | **Frontend/App** <br> <img src="https://img.shields.io/badge/Flutter-02569B?style=flat&logo=Flutter&logoColor=white"> <img src="https://img.shields.io/badge/React-61DAFB?style=flat&logo=React&logoColor=black"> |

</div>

---

## Introduce
### **협업에 진심입니다**
- 다수의 해커톤과 팀 단위 프로젝트에서 협업을 주도한 경험이 있습니다.
- 팀의 분위기에 맞는 가장 적절한 협업 툴을 정의하고 효율적인 소통을 이끌어내고자 합니다.

### **학습을 망설이지 않습니다**
- 익숙한 기술에 얽매이기 보다는 더 적절하고 표준적인 기술 도입을 망설이지 않습니다.
- 또한, 담당 포지션 이외의 작업이 필요하다면 곧바로 학습하고 기여하고자 노력합니다.

---

## 📂 Projects

### 1. 개인 프로젝트 - Mobidic
**Whisper 모델 기반의 AI 영어 단어장 크로스플랫폼 앱**
* **관련 링크:** [[Google Play]](https://play.google.com/store/apps/details?id=com.kthowns.mobidic&pcampaignid=web_share) | [[웹 배포 링크]](https://mobidic.kthowns.cloud) | [[Git Repo]](https://github.com/kthowns/mobidic-be)
* **개발 기간:** 2024.04 ~ 진행 중
* **팀 구성:** 1인 프로젝트 / 기획, 디자인, 백엔드 API 설계/구현, 앱 개발, 서버 및 인프라 관리 담당
* **주요 기술 스택** : Spring Boot 3.5.x, MySQL, Redis, QueryDSL, Docker, AWS, Flutter, Python (Whisper STT)
> * 발음 평가를 위한 로컬 모델 연동(Whisper STT) 및 Redis 장애 극복을 위한 Fallback 메커니즘 설계
> * Redis 일회용(One-time) UUID 토큰 검증 메커니즘을 통한 퀴즈 어뷰징 방지 및 기밀성 보장
> * QueryDSL DTO Projection을 통한 복잡한 통계 집계 최적화 (2N+1 쿼리 해결)
> * 모놀리식에서 실무형 헥사고날 아키텍처(Hexagonal Architecture)로의 전환 및 멀티 모듈 설계
> * DDD(도메인 주도 설계) 기반의 도메인 모델 불변성 확보 및 표준 컴포넌트(Reader-Appender-Updater-Remover-Validator) 패턴 확립

### 2. 팀 스파르타 Java 심화 과정 - Ordering Service API
**Gemini API 기반 AI 상품 설명 및 리뷰 자동 답글 기능을 갖춘 배달 커머스 백엔드 플랫폼**
* **관련 링크:** [[Swagger API 명세]](https://order.kthowns.cloud/api/api-docs) | [[Git Repo]](https://github.com/sparta-ordering-10TEAM/ordering-be)
* **개발 기간:** 2026.07 (2주)
* **팀 구성:** 5인 프로젝트 / 리뷰 및 AI 도메인 개발, GitHub 레포지토리 관리, Nginx HTTPS 기반 서버 배포 및 CI/CD 구축 담당
* **주요 기술 스택** : Spring Boot 3.5.x, PostgreSQL 17, Docker, Nginx, GitHub Actions, Gemini API (RestClient)
> * 외부 AI API 호출을 트랜잭션 외부로 격리하는 파사드(Facade) 아키텍처 설계를 통한 DB 커넥션 점유 단축 및 API 지연 시간 75% 이상 개선
> * 공통 프롬프트 보안 가드레일(COMMON_GUARDRAILS) 설계를 통한 AI 프롬프트 인젝션(Prompt Injection) 방어 및 서비스 안전성 확보
> * 중복 리뷰 방지를 위한 주문 테이블 비관적 락(Pessimistic Lock)을 배제하고 DB 고유 제약 조건을 활용한 예외 파싱 핸들링으로 락 병목 오버헤드 해소
> * 음식점 평균 평점 반정규화 및 JPA @Modifying 서브쿼리 벌크 갱신 방식을 도입하여 동시성 문제를 방어하고 실시간 평점 집계 조회 N+1 문제 해결
> * GitHub Actions, Docker 및 docker-compose 환경을 구축하여 빌드, 이미지 푸시, 서버 원격 배포 프로세스를 자동화한 CI/CD 파이프라인 수립

---

## 🎲 Hackathons & Experience
* **[2025 충남톤]** – 환경 친화적 로컬 관광 지도 애플리케이션, **EcoNavi** | **Backend Engineer** [[Link to Repo]](https://github.com/kthowns/econavi-app) 
* **[2025 구름 딥다이브 해커톤 ]** – 지속적인 돌봄과 헬스케어를 위한 모바일 애플리케이션, **Wecare** | **Backend Engineer** [[Link to Repo]](https://github.com/kthowns/wecare-app) 
* **[구름톤 in 판교]** – 컴퓨터 & 개발 커뮤니티 웹 플랫폼 | **Full-stack Developer** [[Link to Repo]](https://github.com/kthowns/joribhaejo-web) 
* **[2025 구름톤 univ 시즌톤]** – 개인화 청년 맞춤형 커리어 가이드 크로스플랫폼 애플리케이션, **Future-Finder** | **Frontend Engineer** [[Link to Repo]](https://github.com/kthowns/2025_SEASONTHON_TEAM_85_FE)

---

## 🎖 Awards

* **[구름 DeepDive 풀스택 개발자 과정 4회차]** – 최종 팀프로젝트 **우수상** (Feb 2026)
* **[대경권 대학생 프로그래밍 대회]** – **동상** (July 2023)
* **[대구 정보보호경진대회 개인전]** – **우수상** (Dec 2017)
* **[경북 지방 기능경기대회]** – IT Network System 종목 **은메달** (Apr 2017)
---
