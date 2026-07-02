AI 선생님 피드백 고도화 적용 안내 (2026-05-31)

1. 먼저 Supabase SQL Editor에서 아래 파일을 실행하세요.
   - sql/ai_feedback_premium_20260531.sql

2. Vercel 환경변수 확인
   - OPENAI_API_KEY 필수
   - OPENAI_FEEDBACK_MODEL 선택, 기본값 gpt-4.1-mini
   - SUPABASE_URL / SUPABASE_ANON_KEY는 기존 값 사용 가능
   - OPENAI_VECTOR_STORE_ID가 있으면 기존 학원 피드백 자료를 참고합니다.

3. 추가된 기능
   - 공부방 입력창에서 학생에게 보이지 않는 AI 분석용 입력 흐름 로그 저장
   - 글자 입력 지연, 백스페이스, 붙여넣기, 후반부 지연 패턴 저장
   - 약어 대상 구간의 지연/오류/약어 표시 ON-OFF 상태 저장
   - 파일별 AI 피드백 고도화
   - 오늘 전체 AI 피드백 생성
   - 최근 7일 성장 분석 피드백 생성
   - 맞춤 연습문장과 1분 약점 교정 원고 생성

4. 수정/추가 파일
   - assets/js/intermediate.js
   - assets/js/records.js
   - assets/js/learning-portal.js
   - assets/css/mypage-redesign.css
   - mypage.html
   - intermediate.html
   - index.html
   - api/_ai-feedback-core.js
   - api/ai-feedback.js
   - api/ai-daily-feedback.js
   - api/ai-growth-feedback.js
   - sql/ai_feedback_premium_20260531.sql

5. 주의
   - 입력 흐름 원시 로그는 학생 화면에 표시하지 않습니다.
   - 학생에게는 AI가 가공한 피드백만 노출됩니다.
   - SQL을 먼저 실행하지 않으면 입력 로그 테이블 저장은 실패하고, 피드백 품질이 제한됩니다.
