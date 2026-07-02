소리자바 모바일 외장 키보드 입력 복구 패치 - 2026-06-01

수정 목적
- 모바일 가상키보드 차단 처리 후 블루투스/외장 키보드 입력까지 막히는 문제를 수정했습니다.

핵심 수정
- mobile-keyboard-blocker.js에서 readonly 처리 제거
- touchstart/pointerdown에서 preventDefault 사용 제거
- 입력창 focus 흐름 유지
- inputmode=none, virtualkeyboardpolicy=manual 중심으로 가상키보드만 억제
- 타자왕 king.js의 readonly/focus 강제 보정 제거
- 타자왕 문장 전환 스크롤 보정 및 입력 잔상 방지 로직은 유지

적용 방법
- 압축 해제 후 기존 프로젝트 루트에 그대로 덮어쓰기
- 배포 후 모바일 브라우저 캐시를 새로고침해서 확인

주의
- 외장 키보드 입력을 우선 보장하기 위해 readonly 방식은 사용하지 않습니다.
