# 한 해 뒤의 나에게

GitHub Pages 앱 주소: https://eunyool10.github.io/one-year-diary/

Google 로그인과 여러 기기 간 동기화를 활성화하려면 다음 설정이 필요합니다.

1. [Firebase Console](https://console.firebase.google.com/)에서 새 프로젝트를 만들고 웹 앱을 추가합니다.
2. Project settings의 앱 설정에서 웹 앱 SDK 설정값을 복사해 `firebase-config.js`의 `apiKey`, `authDomain`, `projectId`, `appId`에 입력합니다. 이 파일의 웹 설정값은 클라이언트 공개값이며 서비스 계정 비밀키를 넣으면 안 됩니다.
3. Authentication에서 Google 제공자를 켭니다. 승인된 도메인에 `eunyool10.github.io`를 추가합니다.
4. Firestore Database를 만들고 Rules 탭에 `firestore.rules` 내용을 게시합니다.
5. 수정된 `firebase-config.js`를 이 저장소의 main 브랜치에 커밋합니다.

Firestore 규칙은 문장 본문을 별도 문서에 보관하고, 서버 시간이 공개 예정일에 도달하기 전에는 본문 읽기를 거부합니다. 기록과 계정은 사용자 UID 경로로 분리됩니다. 프로젝트를 만들기 전까지 로그인 버튼은 비활성화되어 있습니다.
