# 포모도로 타이머 🍅

> FastAPI + React를 기반으로 한 향상된 포모도로 타이머 앱. Docker Compose로 간편하게 배포하세요!

## 특징 ✨

- 🕒 **클래식 포모도로 기법**: 25분 작업, 5분 휴식 패턴
- 📊 **통계 및 진행률 추적**: 일일/주간/월간 생산성 분석
- 🔔 **실시간 알림**: 타이머 종료 시 자동 알림
- 🏷️ **작업 카테고리 관리**: 프로젝트별 시간 분류
- 🌐 **한글 완벽 지원**: 한국어 UI/UX 최적화
- 🐟 **Docker Compose 배포**: 한 번에 모든 서비스 실행

## 시스템 요구사항

- Docker 20.10 이상
- Docker Compose 1.29 이상
- 포트 3000 (Frontend), 8000 (Backend) 사용 가능

## 빠른 시작 🚀

### 1. 저장소 클론

```bash
git clone https://github.com/eentost/pomodoro-timer.git
cd pomodoro-timer
```

### 2. Docker Compose로 실행

```bash
docker-compose up -d
```

### 3. 브라우저에서 접속

- Frontend: http://localhost:3000
- Backend API: http://localhost:8000
- API 문서: http://localhost:8000/docs

## 프로젝트 구조

```
pomodoro-timer/
├── backend/              # FastAPI 백엔드
│   ├── app/
│   │   ├── main.py        # 메인 애플리케이션
│   │   ├── models.py      # 데이터모델
│   │   └── routes.py      # API 라우팅
│   ├── Dockerfile
│   └── requirements.txt
├── frontend/             # React 프론트엔드
│   ├── public/
│   ├── src/
│   │   ├── components/    # React 컴포넌트
│   │   ├── App.js
│   │   └── index.js
│   ├── Dockerfile
│   └── package.json
└── docker-compose.yml   # Docker Compose 설정
```

## 주요 기능

### 타이머 기능
- 25분 집중 타이머
- 5분 짧은 휴식
- 15분 긴 휴식 (4포모도로마다)
- 일시정지/재개/리셋 기능

### 통계 기능
- 일일 완료한 포모도로 횟수
- 카테고리별 시간 분포
- 주간/월간 생산성 그래프

### 작업 관리
- 작업 목록 추가/수정/삭제
- 카테고리 분류
- 진행 상황 추적

## 기술 스택

### Backend
- **FastAPI**: 고성능 Python 웹 프레임워크
- **SQLite**: 경량 데이터베이스
- **Pydantic**: 데이터 검증

### Frontend
- **React**: 컴포넌트 기반 UI 라이브러리
- **Axios**: HTTP 클라이언트
- **Recharts**: 데이터 시각화

### DevOps
- **Docker**: 컨테이너화
- **Docker Compose**: 멀티 컨테이너 오케스트레이션

## 환경 변수 설정

`docker-compose.yml`에서 환경 변수를 수정할 수 있습니다:

```yaml
environment:
  - WORK_DURATION=25  # 작업 시간 (분)
  - SHORT_BREAK=5     # 짧은 휴식 (분)
  - LONG_BREAK=15     # 긴 휴식 (분)
```

## 개발 모드

개발 모드로 실행하려면:

```bash
# Backend
cd backend
pip install -r requirements.txt
uvicorn app.main:app --reload

# Frontend (새 터미널)
cd frontend
npm install
npm start
```

## 기여하기

1. Fork the Project
2. Create your Feature Branch (`git checkout -b feature/AmazingFeature`)
3. Commit your Changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the Branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 라이센스

MIT License - 자세한 내용은 LICENSE 파일을 참조하세요.

## 연락처

이슈나 기능 제안은 GitHub Issues를 사용해주세요!

---

⭐️ 프로젝트가 마음에 들었다면 Star를 눌러주세요!
