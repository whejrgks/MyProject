# 기술 스택 (Technology Stack)

## 개요

본 프로젝트에서 사용하는 기술 스택 및 각 계층별 기술 선택 이유를 정리한 문서입니다.

---

## 기술 스택 테이블

| 계층 (Layer) | 사용 기술 (Used Technology) | 설명 (Description) |
|-------------|---------------------------|-------------------|
| **프론트엔드 (UI)** | React | 빠른 프로토타입 또는 완성형 웹 인터페이스 |
| **백엔드 (API)** | FastAPI | 비동기 고성능 Python 웹 프레임워크 |
| **데이터베이스** | PostgreSQL | 안정적이고 ORM 기반의 DB 설계 |
| **인증/세션** | FastAPI Users, OAuth2 | 로그인, JWT 인증 |
| **테스트** | pytest | 단위/통합 테스트 |
| **문서화** | Swagger / ReDoc (FastAPI 자동 문서) | API 자동 문서 생성 |
| **배포/환경** | Render | 백엔드, DB, 프론트 통합 실행 환경 구성 |

---

## 상세 설명

### 프론트엔드 (Frontend)

**React**
- 빠른 프로토타입 개발 가능
- 컴포넌트 기반 재사용 가능한 UI 구성
- 풍부한 생태계와 커뮤니티 지원
- 고객용 QR 메뉴판 및 관리자 페이지 모두 구현 가능

### 백엔드 (Backend)

**FastAPI**
- 비동기 처리로 고성능 API 제공
- 자동 API 문서 생성 (Swagger/ReDoc)
- Python 기반으로 빠른 개발 가능
- 타입 힌팅 지원으로 안정적인 코드 작성

### 데이터베이스 (Database)

**PostgreSQL**
- 안정적이고 신뢰성 높은 관계형 데이터베이스
- ORM (SQLAlchemy 등) 기반 설계로 유지보수 용이
- 복잡한 쿼리 및 트랜잭션 처리 지원
- 확장성과 성능 최적화 가능

### 인증/세션 (Authentication/Session)

**FastAPI Users, OAuth2**
- FastAPI Users: 사용자 관리 및 인증 기능 제공
- OAuth2: 표준 인증 프로토콜
- JWT 토큰 기반 인증으로 확장 가능한 보안 구조
- 관리자 페이지 접근 제어

### 테스트 (Testing)

**pytest**
- Python 표준 테스트 프레임워크
- 단위 테스트 및 통합 테스트 작성
- Fixture를 통한 테스트 데이터 관리
- 커버리지 리포트 생성 가능

### 문서화 (Documentation)

**Swagger / ReDoc**
- FastAPI 자동 생성 API 문서
- Swagger UI: 인터랙티브 API 테스트 환경
- ReDoc: 읽기 쉬운 API 문서 형식
- API 엔드포인트 자동 문서화

### 배포/환경 (Deployment/Environment)

**Render**
- 백엔드, 데이터베이스, 프론트엔드 통합 실행 환경
- 간편한 배포 및 관리
- 자동 스케일링 지원
- CI/CD 파이프라인 구성 가능

---

## 아키텍처 다이어그램

```
┌─────────────────┐
│   React (UI)    │  ← 고객용 QR 메뉴판 / 관리자 페이지
└────────┬────────┘
         │
         │ HTTP/HTTPS
         │
┌────────▼────────┐
│  FastAPI (API)  │  ← 비동기 고성능 백엔드
└────────┬────────┘
         │
         │ ORM (SQLAlchemy)
         │
┌────────▼────────┐
│  PostgreSQL     │  ← 데이터베이스
└─────────────────┘

[인증] FastAPI Users + OAuth2 + JWT
[테스트] pytest
[문서화] Swagger / ReDoc
[배포] Render
```

---

## 개발 환경 설정

### 필수 요구사항

- Python 3.9+
- Node.js 16+
- PostgreSQL 12+

### 주요 패키지

**Backend (Python)**
- fastapi
- fastapi-users
- sqlalchemy
- psycopg2 (PostgreSQL adapter)
- pytest
- uvicorn

**Frontend (JavaScript)**
- react
- react-dom
- react-router-dom

---

## 참고 사항

- 모든 기술 스택은 프로젝트 요구사항에 맞게 선택되었습니다.
- 향후 확장 시에도 현재 아키텍처를 기반으로 확장 가능합니다.
- 각 기술의 최신 버전 및 보안 업데이트를 정기적으로 확인해야 합니다.

