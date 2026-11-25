# 오늘의메모 (Android)

메모 · 날씨 · 할일 · 달력 · 기념일 · 가계부를 한 앱에서.

- 빌드: `oneul-memo` 브랜치에 푸시하면 GitHub Actions가 `apk/OneulMemo.apk`와 Release를 만듭니다.
- 구조: `app/src/main/assets/index.html`(화면·기능) + `MainActivity.java`(WebView 래퍼, 저장·공유·백업 브리지)
- 데이터: 폰 안(localStorage + SharedPreferences 이중 저장). 날씨·미세먼지는 Open-Meteo(키 불필요).
- 서명키 `app/oneulmemo.keystore`는 사이드로드용입니다. Play 스토어 배포 시에는 별도 키를 만들어 GitHub Secrets로 옮기세요.
