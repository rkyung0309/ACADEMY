AI 선생님 피드백방 분리 수정본

적용 파일:
- index.html
- mypage.html
- ai-teacher.html
- assets/css/ai-teacher-dashboard.css
- assets/js/learning-portal.js

수정 내용:
1. 대시보드 첫 화면의 큰 AI 분석 영역을 제거하고, 작은 진입 카드만 남겼습니다.
2. 사이드바 홈 메뉴에 'AI 선생님 피드백방' 메뉴를 추가/정리했습니다.
3. 마이페이지 학습요약에 있던 유료 AI 선생님 분석 카드를 제거했습니다.
4. AI 분석 생성 버튼과 분석 결과 목록을 ai-teacher.html 전용 페이지로 이동했습니다.
5. 기존 AI 피드백 API, 일일 피드백, 성장 분석, 파일별 AI 피드백 로직은 유지했습니다.
6. Supabase SQL은 다시 실행할 필요 없습니다.
