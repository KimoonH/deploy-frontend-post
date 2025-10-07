# 포스트 게시판 프론트엔드

React와 Material-UI를 사용한 간단한 포스트 게시판 프론트엔드 애플리케이션입니다.

## 🚀 시작하기

### 1. 프로젝트 클론 및 의존성 설치

```bash
# 1. 프로젝트 클론 (이미 클론했다면 생략)
git clone <repository-url>
cd deploy-frontend-post

# 2. Node.js 패키지 설치
npm install
```

### 2. 환경 변수 설정

프로젝트는 환경별로 다른 설정 파일을 사용합니다.

#### 개발 환경 설정

프로젝트 루트 디렉토리에 `.env.local` 파일을 생성하고 아래 내용을 추가하세요:

```env
# 개발 환경 API 서버 주소
VITE_API_BASE_URL=http://localhost:8080/api/v1
```

#### 프로덕션 환경 설정

프로젝트 루트 디렉토리에 `.env.production` 파일을 생성하고 아래 내용을 추가하세요:

```env
# 프로덕션 환경 API 서버 주소
VITE_API_BASE_URL=https://your-production-api-domain.com/api/v1
```

> **참고**: 프로덕션 환경에서는 `https://your-production-api-domain.com/api/v1`을 실제 서버 주소로 변경하세요.

### 3. 개발 서버 실행

```bash
npm run dev
```

브라우저에서 `http://localhost:5173`로 접속하면 애플리케이션을 확인할 수 있습니다.

## 📁 프로젝트 구조

```
src/
├── api/
│   └── postApi.jsx          # API 호출 함수들
├── components/
│   └── PostList.jsx         # 포스트 목록 컴포넌트
├── assets/
│   └── react.svg
├── App.jsx                  # 메인 App 컴포넌트
├── App.css                  # App 스타일
├── main.jsx                 # React 앱 진입점
└── index.css                # 전역 스타일
```

## 🛠️ 주요 기능

- **포스트 목록 조회**: 백엔드 API에서 포스트 데이터를 가져와 표시
- **Material-UI 디자인**: 깔끔하고 모던한 UI/UX
- **반응형 디자인**: 모바일과 데스크톱에서 모두 사용 가능

## 📋 사용 가능한 스크립트

```bash
# 개발 서버 실행 (자동으로 .env.local 사용)
npm run dev

# 프로덕션 빌드 (자동으로 .env.production 사용)
npm run build

```

## 🔧 기술 스택

- **React 19** - UI 라이브러리
- **Vite** - 빌드 도구 및 개발 서버
- **Material-UI (MUI)** - UI 컴포넌트 라이브러리
- **Axios** - HTTP 클라이언트
- **ESLint** - 코드 품질 도구

## ⚠️ 주의사항

1. **백엔드 서버 필수**: 이 프론트엔드는 백엔드 API 서버가 실행되어야 정상 작동합니다.
2. **환경 변수**:
   - 개발 환경: `.env.local` 파일의 `VITE_API_BASE_URL`을 개발 서버 주소에 맞게 설정하세요.
   - 프로덕션 환경: `.env.production` 파일의 `VITE_API_BASE_URL`을 프로덕션 서버 주소에 맞게 설정하세요.
3. **CORS 설정**: 백엔드에서 CORS 설정이 필요할 수 있습니다.

## 🐛 문제 해결

### 포스트가 로드되지 않을 때

1. 백엔드 서버가 실행 중인지 확인
2. 환경에 맞는 설정 파일이 올바른지 확인:
   - 개발: `.env.local` 파일의 `VITE_API_BASE_URL`
   - 프로덕션: `.env.production` 파일의 `VITE_API_BASE_URL`
3. 브라우저 개발자 도구 콘솔에서 에러 메시지 확인

### 개발 서버가 시작되지 않을 때

1. Node.js 버전 확인 (권장: v18 이상)
2. `npm install` 다시 실행
3. `node_modules` 폴더 삭제 후 `npm install` 재실행
