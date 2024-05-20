# Init Android Studio

## Android Studio 설치

1. [Android Studio 다운로드](https://developer.android.com/studio) 접속
2. `Download Android Studio` 클릭
3. 이용 약관 동의 후, 설치 환경에 맞게 Intel chip 또는 Apple chip을 선택하여 다운로드
4. 다운로드된 dmg 파일로 설치
5. `Android Studio`를 실행하여 확인

## Android Toolchain 설치

1. `Android Studio` 실행
2. `Settings` -> `Languages & Frameworks` -> `Android SDK` 클릭
3. `SDK Platforms` 클릭 후, 최신 버전 API 설치
   - e.g. Android 14.0 ("UpsideDownCake")
4. `SDK Tools` 클릭 후, `Android SDK Command-line Tools (latest)` 설치
5. 터미널에 아래 스크립트를 붙여넣어 모든 이용 약관에 동의
   ```
   flutter doctor --android-licenses
   ```
   기대 응답
   ```
   이상 생략
   
   All SDK package licenses accepted
   ```