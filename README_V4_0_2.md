# TRAVELER Schedule V4.0.2

변경사항
- 로그인/회원가입 화면에 `Google로 계속하기` 추가
- Firebase Credential Manager 기반 Google 로그인 연결
- 출발일/귀국일 날짜필드 클릭 시 달력 팝업이 안정적으로 열리도록 터치 영역 수정
- GitHub Actions에서도 Google OAuth SHA-1이 매번 바뀌지 않도록 고정 CI debug keystore 적용

## Google 로그인 1회 설정
Firebase Console > 프로젝트 설정 > 일반 > 내 앱 > Android 앱에서 아래 SHA-1을 등록하세요.

`70:C4:2F:7E:18:35:CE:8F:41:EB:E5:E5:7E:3E:34:1F:E3:D2:7B:E7`

그 다음 Firebase에서 `google-services.json`을 다시 다운로드하여 `app/google-services.json`을 새 파일로 교체하세요.
Google 제공업체는 Authentication > 로그인 방법에서 사용 설정되어 있어야 합니다.

주의: app/ci-debug.keystore는 GitHub Actions의 디버그 APK 테스트용입니다. Play Store 출시용 서명키로 사용하지 마세요.
