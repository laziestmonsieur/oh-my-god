# 전보 셀프체크 배포 사이트 v1

목표 흐름:

QR 코드 → 이 사이트 → Android APK / iPhone TestFlight(App Store) / 웹 버전

## 1. 현재 바로 되는 것
- `index.html` : 배포 랜딩 페이지
- `web/index.html` : 설치 없이 바로 사용할 수 있는 웹 버전
- 기기 감지 후 Android / iPhone 안내 변경

## 2. Android APK 연결
1. 서명된 배포용 APK를 `downloads/전보_셀프체크.apk` 같은 이름으로 넣습니다.
2. `config.js`의 `androidApkUrl`을 예: `./downloads/전보_셀프체크.apk` 로 바꿉니다.
3. 사용자는 사이트에서 APK를 내려받아 설치합니다.

## 3. iPhone 연결
일반 웹사이트에서 IPA를 직접 배포하는 대신 TestFlight 또는 App Store 링크를 연결합니다.
- TestFlight 공개 링크가 있으면 `config.js`의 `iosTestFlightUrl`에 입력
- 정식 App Store 주소가 있으면 `iosAppStoreUrl`에 입력

## 4. 사이트 공개
이 폴더 전체를 HTTPS 호스팅에 업로드합니다.
예: GitHub Pages, Cloudflare Pages, Netlify, 사내 웹서버 등.

공개 주소 예:
`https://example.com/transfer-check/`

## 5. QR 코드
사이트 공개 주소가 결정되면 그 URL을 QR 코드로 만들면 됩니다.
QR 하나로 Android와 iPhone 모두 같은 사이트에 들어옵니다.

최종 공개 URL을 ChatGPT에 보내면 QR PNG/SVG를 생성할 수 있습니다.
