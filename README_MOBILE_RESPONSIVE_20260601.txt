모바일 화면 최적화 패치 - 2026-06-01

적용 방식
1. assets/css/mobile-responsive.css 신규 추가
2. 모든 주요 HTML 파일 head 영역에 아래 CSS 연결 추가
   <link rel="stylesheet" href="assets/css/mobile-responsive.css?v=20260601-mobile-v1">

주요 보정 내용
- 900px 이하 화면에서 본문 고정폭 제거
- 카드/패널/통계/대시보드/입력 영역 1열 전환
- 표 영역 가로 스크롤 처리
- textarea/input/button 모바일 폭 보정
- 모달/결과창/히스토리 화면 잘림 방지
- 모바일 사이드바와 본문 padding 충돌 보정

적용 방법
- 기존 프로젝트 폴더에 이 압축 파일의 내용을 그대로 덮어쓰기
- 신규 파일 assets/css/mobile-responsive.css가 반드시 같이 올라가야 함
