2026-05-05 최종 통합본

- 예시 HTML의 정적 사용자/샘플 문구를 제거하고 원본 Supabase Auth, profiles, practice_records, notices, practice_materials 흐름에 연결했습니다.
- index.html: 로그인 진입점 유지, 로그인 후 실제 사용자명/프로필/연습기록/공지/피드백 현황 표시.
- study-room.html: 듣고치기/보고치기/퀘스트를 자료 선택→작성→채점/저장 흐름으로 재구성. practice_materials와 practice_records 연결. 기존 학습도구는 바로가기 영역으로 정리.
- study-coach.html: 기존 study-room.html 원본 기능을 보존한 백업형 학습 코치 페이지입니다.
- mypage.html: 요약/학습기록/피드백/오답노트/플랜설정 탭 구조. 실제 records 기반 표시.
- assets/css/learning-portal.css, assets/js/learning-portal.js 추가.

주의: 원본 프로젝트에 크레딧/피드백 전용 DB 테이블이 없어 해당 항목은 사용자별 localStorage로 보존되며, profiles에 credit_balance/credits/credit 필드가 있으면 그 값을 우선 표시합니다.
