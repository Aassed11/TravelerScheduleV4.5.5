# TRAVELER Schedule V4.0.1 build fix

GitHub Actions 오류 원인:
- Firebase BoM 34.19.0이 firebase-auth 24.2.0을 선택함
- firebase-auth 24.2.0은 Kotlin metadata 2.3.0으로 컴파일됨
- 프로젝트 Kotlin 2.1.20 컴파일러는 metadata 2.1.0까지 기대하여 compileDebugKotlin에서 실패

수정:
- Firebase BoM을 34.19.0 -> 33.16.0으로 고정
- 이 BoM은 firebase-auth 23.2.1 세대를 사용하므로 기존 Kotlin 2.1.20 / AGP 8.7.3 / Gradle 8.9 조합을 유지할 수 있음
- 로그인/Firestore 코드 변경 없음
