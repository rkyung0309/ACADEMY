AI 선생님 피드백 MVP 적용 안내
작성일: 2026-05-27

[이번 수정 범위]
1. /api/ai-feedback.js 추가
   - 브라우저에 OpenAI API 키를 노출하지 않기 위한 Vercel 서버리스 API입니다.
   - 로그인한 사용자의 학습 기록을 기준으로 AI 피드백 초안을 생성합니다.
   - OPENAI_VECTOR_STORE_ID가 있으면 OpenAI File Search 지식베이스를 함께 사용합니다.
   - 없으면 코드 안의 소리자바식 기본 지도 원칙으로 우선 작동합니다.

2. assets/js/learning-portal.js 수정
   - 마이페이지/연습 기록 영역에 'AI 피드백' 버튼을 추가했습니다.
   - AI 피드백 생성 후 마이페이지 > 피드백 탭에 표시합니다.
   - 기존 '피드백' 버튼은 '강사 신청'으로 유지했습니다.

3. assets/js/records.js 수정
   - 앞으로 저장되는 학습 기록에 원문/학생 입력 스냅샷을 함께 저장할 수 있게 했습니다.
   - AI가 단순 점수뿐 아니라 실제 입력 내용을 참고할 수 있게 하기 위한 수정입니다.

4. assets/css/learning-portal.css 수정
   - AI 피드백 카드와 버튼 배치 스타일을 추가했습니다.

5. sql/ai_feedback_mvp_20260527.sql 추가
   - practice_records에 스냅샷 컬럼 추가
   - ai_feedbacks 테이블 생성
   - 본인 조회/본인 저장 RLS 정책 생성

[적용 순서]
1. Supabase SQL Editor에서 아래 파일 내용을 실행합니다.
   sql/ai_feedback_mvp_20260527.sql

2. Vercel 환경변수에 아래 값을 추가합니다.
   필수:
   OPENAI_API_KEY

   권장:
   SUPABASE_URL
   SUPABASE_ANON_KEY
   OPENAI_FEEDBACK_MODEL

   선택:
   OPENAI_VECTOR_STORE_ID

3. GitHub에 수정 파일을 업로드하고 Vercel 재배포를 진행합니다.

4. 테스트 순서
   1) 학생 계정으로 로그인
   2) 연습실 또는 중급반 공부방에서 원문이 있는 자료로 채점/저장
   3) 마이페이지 > 학습 기록 이동
   4) 해당 기록의 'AI 피드백' 버튼 클릭
   5) 마이페이지 > 피드백 탭에 AI 피드백 카드가 생성되는지 확인

[중요]
- 기존에 저장된 practice_records에는 원문/학생 입력 스냅샷이 없습니다.
  따라서 기존 기록은 수치 기반 피드백만 가능합니다.
- 이번 수정 이후 새로 저장되는 기록부터 원문/학생 입력 스냅샷이 저장됩니다.
- AI 피드백은 최종 채점이 아니라 학습 보조용 초안입니다.
- API 키는 절대 assets/js, html, GitHub 파일 안에 넣지 말고 Vercel 환경변수에만 넣어야 합니다.

[다음 고도화 후보]
1. 관리자 화면에서 AI 피드백 초안 검수 후 공개 기능
2. 업로드한 수업자료 TXT를 OpenAI Vector Store에 등록하는 관리 기능
3. 과제 제출 파일 기반 AI 피드백
4. 학생별 피드백 이력 누적 분석
5. 피드백 비용/사용량 제한 기능
