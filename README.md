# 메모 애플리케이션

React Native 스타일로 디자인된 모던한 메모 관리 웹 애플리케이션입니다. 간편한 메모 작성, 수정, 삭제 기능을 제공하며, 오프라인 환경에서도 사용 가능합니다.

![메모 애플리케이션 미리보기](screenshot.png)

## 주요 기능

### 기본 기능

- **메모 작성**: 제목과 내용으로 구성된 메모 생성
- **메모 목록 조회**: 생성된 모든 메모 확인
- **메모 수정**: 기존 메모의 제목과 내용 수정
- **메모 삭제**: 불필요한 메모 삭제
- **자동 날짜 기록**: 메모 생성 및 수정 시간 자동 기록

### 고급 기능

- **오프라인 저장**: localStorage를 활용하여 API 서버 연결 실패 시에도 데이터 유지
- **반응형 디자인**: 모바일 및 데스크탑 환경 모두 지원
- **직관적인 UI**: 아이콘과 애니메이션으로 사용자 경험 향상
- **모던한 디자인**: React Native 스타일의 카드 형태 UI
- **터치/클릭 상호작용**: 메모 항목 클릭 시 편집 모드로 전환

## 디자인 특징

- **카드 스타일 UI**: 각 섹션과 메모 항목은 그림자와 둥근 모서리를 가진 카드 형태
- **애니메이션 효과**: 요소 호버 시 위로 떠오르는 효과와 그림자 변화
- **아이콘 통합**: Font Awesome 아이콘을 활용하여 직관적인 UI 제공
- **색상 스키마**: 블루 계열의 주 색상과 악센트 색상 조합
- **깔끔한 타이포그래피**: 가독성을 높인 폰트 사이즈와 간격
- **반응형 레이아웃**: 화면 크기에 따라 최적화된 UI 자동 조정

## 기술 스택

### 프론트엔드

- **HTML5**: 웹 구조 정의
- **CSS3**: 모던한 스타일링, 변수 활용, 반응형 디자인
- **JavaScript (ES6+)**: 동적 기능 구현
- **Font Awesome**: 직관적인 아이콘 제공
- **LocalStorage API**: 오프라인 데이터 저장

### 백엔드 (선택적)

- **Node.js**: 서버 환경
- **Express**: REST API 구현
- **MySQL/Amazon RDS**: 데이터 영구 저장 (선택적)

## 구현 세부 사항

### 사용자 인터페이스

- **헤더**: 앱 타이틀과 아이콘
- **메모 작성 폼**: 제목과 내용 입력 폼
- **메모 수정 폼**: 기존 메모 수정 폼 (기본적으로 숨김 처리)
- **메모 목록**: 카드 형태로 표시되는 메모 항목들
- **반응형 버튼**: 저장, 수정, 삭제, 취소 등의 액션 버튼
- **푸터**: 저작권 정보

### 자바스크립트 기능

- **비동기 데이터 처리**: async/await를 활용한 API 통신
- **폴백 메커니즘**: API 연결 실패 시 localStorage로 전환
- **이벤트 위임**: 메모 항목의 동적 이벤트 처리
- **사용자 경험 개선**: 스무스 스크롤링, 입력 폼 관리
- **데이터 유효성 검사**: 빈 메모 방지를 위한 유효성 검사
- **HTML 이스케이프**: XSS 공격 방지를 위한 이스케이프 처리

### CSS 스타일링

- **CSS 변수**: 색상, 그림자, 모서리 반경 등 일관된 스타일 유지
- **Flexbox**: 유연한 레이아웃 구성
- **트랜지션/애니메이션**: 부드러운 시각적 효과
- **미디어 쿼리**: 다양한 화면 크기 대응

## 설치 및 실행 방법

### 프론트엔드만 실행 (오프라인 모드)

1. 저장소 클론 또는 다운로드
   ```
   git clone https://github.com/yourusername/memo-app.git
   cd memo-app
   ```
2. 웹 서버로 실행

   ```
   npx serve memo_app
   ```

   또는 VS Code의 Live Server 확장 프로그램으로 실행

3. 브라우저에서 확인
   ```
   http://localhost:5000
   ```

### 백엔드 연동 (선택사항)

1. 의존성 설치

   ```
   npm install
   ```

2. 환경 변수 설정 (RDS 연결 시)

   ```
   RDS_HOSTNAME=your-rds-endpoint.rds.amazonaws.com
   RDS_USERNAME=your-username
   RDS_PASSWORD=your-password
   RDS_DB_NAME=memodb
   RDS_PORT=3306
   ```

3. 백엔드 서버 실행

   ```
   npm start
   ```

4. 개발 모드 실행
   ```
   npm run dev
   ```

## 사용 방법

1. **메모 작성**

   - 제목과 내용 입력 후 '저장' 버튼 클릭
   - 메모가 목록에 추가됨

2. **메모 수정**

   - 목록에서 메모 클릭 또는 수정 버튼(연필 아이콘) 클릭
   - 내용 수정 후 '업데이트' 버튼 클릭

3. **메모 삭제**
   - 삭제 버튼(휴지통 아이콘) 클릭
   - 확인 메시지 후 삭제 진행

## 향후 개선 계획

- **검색 기능**: 메모 내 키워드 검색
- **카테고리 분류**: 메모 주제별 분류
- **마크다운 지원**: 서식이 있는 메모 작성
- **데이터 동기화**: 클라우드 저장 및 동기화
- **사용자 인증**: 개인화된 메모 관리
- **다크 모드**: 라이트/다크 테마 전환

## 라이선스

이 프로젝트는 MIT 라이선스 하에 배포됩니다.

## 제작자

DoSeon-Lee (doseon1226@gmail.com)
