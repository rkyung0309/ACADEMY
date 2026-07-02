모바일 보고치기/듣고치기 화면 보정 패치 - 2026-06-01

수정 파일
- assets/css/mobile-responsive.css
- intermediate.html
- exam.html
- index.html

적용 내용
1. 입문반/중급반/고급반/급수반 보고치기에서 모바일 원문 영역을 상단 sticky 형태로 고정했습니다.
2. 보고치기 입력창 높이를 모바일 화면 기준으로 줄여 원문과 입력창이 동시에 보이도록 조정했습니다.
3. 듣고치기 채점 버튼 영역을 하단 sticky로 고정하고, 버튼이 오른쪽으로 밀려 숨지 않도록 grid/full-width 처리했습니다.
4. 작은 화면(430px 이하)에서는 원문/입력창 높이와 버튼 배열을 추가로 압축했습니다.
5. CSS 캐시 방지를 위해 관련 HTML의 mobile-responsive.css 버전값을 v2로 변경했습니다.
