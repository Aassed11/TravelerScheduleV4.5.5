# V3.6 재점검

- V3.5의 Room DB 구조/기존 데이터 유지
- versionCode 9 / versionName 3.6 확인
- AppWidgetProvider 2종 Manifest 등록 확인
- 월간 위젯 42개 날짜 셀 ID와 XML ID 대조
- 날짜별 ScheduleEntity 기간 포함 로직 연결 확인
- 국가·지역(location) 표시 연결 확인
- 날짜 터치 -> MainActivity selectedDate 전달 확인
- 일정 존재 날짜 -> 날짜 일정 요약 팝업 연결 확인
- 일정 없는 날짜 -> 선택 날짜가 들어간 새 일정 창 연결 확인
- 다가오는 일정 -> scheduleId 상세 화면 연결 확인
- 일정 추가/수정/삭제 -> WidgetUpdateHelper 호출 확인
- 위젯 이전달/다음달/오늘 버튼 연결 확인
- AndroidManifest 및 res XML 파싱 확인
- Kotlin 소스 파서 단계에서 별도의 `expecting` 구문 오류가 없음을 확인(Android/AndroidX 클래스패스가 없는 로컬 kotlinc에서는 unresolved reference가 발생하므로 실제 APK 컴파일은 GitHub Actions에서 최종 확인 필요)
