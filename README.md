# Sorizava Practice Platform

Supabase 회원가입제 전환용 정리본입니다.

## 포함된 핵심 파일

- `assets/js/supabase-client.js` : Supabase 연결
- `assets/js/auth.js` : 로그인/회원가입/승인상태 확인/로그아웃
- `assets/js/records.js` : 연습 기록 저장/마이페이지 조회
- `signup.html` : 회원가입
- `pending.html` : 승인 대기 화면
- `mypage.html` : 본인 연습 기록 조회
- `admin.html` : 관리자 회원 승인/공지 관리

## Supabase Project URL

`https://frqcxmkweccqvpmbxori.supabase.co`

## 주의

- 프론트에는 publishable key만 들어 있습니다.
- service_role/secret key는 절대 GitHub 또는 브라우저 코드에 넣으면 안 됩니다.
- Supabase RLS 정책이 먼저 적용되어 있어야 기록 저장과 회원 승인 구조가 안전하게 동작합니다.
