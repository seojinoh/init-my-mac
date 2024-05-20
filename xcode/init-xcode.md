# Init Xcode

`Xcode`: macOS, iOS 등 소프트웨어 개발을 위한 Apple의 macOS용 IDE

## 설치

1. App Store에서 `Xcode` 검색 후 설치

## 라이선스 동의

1. 터미널에서 아래 스크립트를 실행하여 진행
   ```
   sudo xcodebuild -license
   ```
   - macOS 패스워드 입력을 요청할 수 있음
   - `agree` 입력을 요청할 수 있음

## 설치 확인

1. 터미널에서 아래 스크립트를 실행하여 확인
   ```
   xcodebuild -version
   ```
   기대 응답
   ```
   Xcode 15.3
   Build version 15E204a
   ```

## 트러블슈팅

### flutter doctor에서 발견된 이슈

#### 이슈 상황

1. 터미널에서 아래 스크립트를 실행했을 때 발생
   ```
   flutter doctor
   ```
   이슈 응답
   ```
   [✓] Flutter (Channel stable, 3.19.6, on macOS 14.4.1 23E224 darwin-arm64, locale en-KR)
   [✓] Android toolchain - develop for Android devices (Android SDK version 34.0.0)
   [!] Xcode - develop for iOS and macOS (Xcode 15.3)
       ✗ Unable to get list of installed Simulator runtimes.
   [✓] Chrome - develop for the web
   [✓] Android Studio (version 2023.3)
   [✓] IntelliJ IDEA Ultimate Edition (version 2023.1)
   [✓] Connected device (2 available)
   [✓] Network resources
   
   ! Doctor found issues in 1 category.
   ```

#### 이슈 조치

1. 터미널에서 아래 스크립트를 실행하여 iOS 시뮬레이터 런타임 설치
   ```
   xcodebuild -downloadPlatform iOS
   ```
   기대 응답
   ```
   Downloading iOS 17.4 Simulator (21E213): Done.
   ```
2. 터미널에서 아래 스크립트를 실행하여 이슈 조치 확인
   ```
   flutter doctor
   ```
   기대 응답
   ```
   Doctor summary (to see all details, run flutter doctor -v):
   [✓] Flutter (Channel stable, 3.19.6, on macOS 14.4.1 23E224 darwin-arm64, locale en-KR)
   [✓] Android toolchain - develop for Android devices (Android SDK version 34.0.0)
   [✓] Xcode - develop for iOS and macOS (Xcode 15.3)
   [✓] Chrome - develop for the web
   [✓] Android Studio (version 2023.3)
   [✓] IntelliJ IDEA Ultimate Edition (version 2023.1)
   [✓] Connected device (2 available)            
   [✓] Network resources
   
   • No issues found!
   ```