DB 연동 검수/보완 내역

1. 실제 Supabase 연동 확인
- supabase-client.js: Supabase URL/key로 window.SORIZAVA_SUPABASE 생성
- auth.js: Supabase Auth 로그인, profiles 조회, 승인 RPC 호출
- records.js: practice_records 저장/조회
- learning-portal.js: notices, practice_materials, practice_records, feedback_requests, credit_ledger 연결

2. 보완한 항목
- practice_records 조회에 .eq('user_id', 현재 로그인 사용자 ID) 명시 추가
- 피드백 요청은 feedback_requests 테이블이 있으면 DB 저장/조회, 없으면 localStorage 임시 저장
- 크레딧 내역은 credit_ledger 테이블이 있으면 DB 조회, 없으면 localStorage 임시 표시

3. SQL
- sql/portal_optional_tables_20260505.sql 파일 포함
- Supabase SQL Editor에서 실행하면 피드백/크레딧도 DB 저장으로 전환됨

4. 남은 전제
- 기존 DB에 practice_records, practice_materials, profiles, notices 테이블과 승인 RPC가 있어야 함
- 실제 mp3/정답 원문은 practice_materials.content 또는 audio_url/sourceText 계열 필드에 있어야 함
