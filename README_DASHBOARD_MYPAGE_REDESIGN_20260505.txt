대시보드/마이페이지 선택 집중 개편본 - 2026-05-05

작업 기준
- 예시 HTML을 그대로 붙이지 않고, 기존 원본 프로젝트 구조와 Supabase 연동 구조 위에서 대시보드와 마이페이지 UI만 재설계했습니다.
- 기존 로그인/승인, 사이드바, Supabase Auth, profiles, practice_records, practice_materials, notices, feedback_requests/credit_ledger fallback 구조는 유지했습니다.

대시보드 역할
- 오늘 바로 실행할 학습 진입점 중심으로 축소했습니다.
- 계정/상세 관리 기능은 제거하고, 사용자 요약만 우측 패널에 작게 배치했습니다.
- 주요 영역: 오늘의 학습 Hero, 바로가기 4개, 핵심 지표, 최근 7일 흐름, 피드백 요약, 최근 기록.

마이페이지 역할
- 대시보드와 중복되지 않도록 관리형 콘솔로 분리했습니다.
- 좌측 로컬 메뉴를 추가해 요약/학습 기록/피드백/오답노트/계정·크레딧을 명확히 분리했습니다.
- 상세 테이블과 피드백 신청/조회는 마이페이지에서 처리하도록 배치했습니다.

주요 변경 파일
- index.html
- mypage.html
- assets/css/learning-portal.css
- assets/js/learning-portal.js

검수
- learning-portal.js 문법 검사 통과
- records.js 문법 검사 통과
- 대시보드/마이페이지 내 정적 예시 사용자명/예시 날짜 제거 확인
- 기존 DB 조회/저장 함수 호출 구조 유지 확인
