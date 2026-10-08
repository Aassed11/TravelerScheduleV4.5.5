# TRAVELER Schedule V4.0 — Firebase 로그인 / 클라우드 동기화

## 포함 기능
- Firebase Authentication 이메일/비밀번호 회원가입·로그인
- 비밀번호 재설정 메일
- 로그인 상태 유지
- Cloud Firestore 일정/체크리스트 저장
- 같은 계정으로 다른 휴대폰 로그인 시 클라우드 일정 내려받기
- 기존 Room 데이터 최초 로그인 시 cloudId 부여 후 클라우드 업로드
- Room 로컬 DB 유지 + Firestore 동기화
- 설정 화면: 계정 이메일, 동기화 상태, 지금 동기화, 로그아웃
- 일정/업무 추가·수정·완료·삭제 시 클라우드 반영
- Firestore 사용자 UID별 분리

## Firebase Console에서 반드시 할 일
1. Security > Authentication > Sign-in method > Email/Password 사용 설정
2. Firestore Database 생성
3. Firestore > Rules에 프로젝트의 `firestore.rules` 내용 적용 후 게시

## Firestore 구조
users/{uid}/schedules/{scheduleCloudId}
users/{uid}/schedules/{scheduleCloudId}/tasks/{taskCloudId}
users/{uid}/deletedSchedules/{scheduleCloudId}
users/{uid}/deletedTasks/{taskCloudId}

## google-services.json
`app/google-services.json`에 포함되어 있습니다.
패키지명은 `com.traveler.schedule`입니다.

## 버전
versionCode 13
versionName 4.0
