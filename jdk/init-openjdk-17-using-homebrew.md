# Init OpenJDK 17 Using Homebrew

## 설치

1. 터미널에서 아래 스크립트를 실행하여 설치
   ```
   brew install openjdk@17
   ```
2. OpenJDK 17 설치 적용
   1. Zsh 설정 파일 수정
      ```
      vi ~/.zshrc
      ```
   2. openjdk17 alias 추가
      ```
      alias openjdk17='unset JAVA_HOME;export JAVA_HOME=/opt/homebrew/opt/openjdk@17;java -version'
      ```
   3. Zsh 설정 파일 수정 사항 적용
      ```
      source ~/.zshrc
      ```
   4. openjdk17 alias 실행
      ```
      openjdk17
      ```
      기대 응답
      ```
      openjdk version "17.0.11" 2024-04-16
      OpenJDK Runtime Environment Homebrew (build 17.0.11+0)
      OpenJDK 64-Bit Server VM Homebrew (build 17.0.11+0, mixed mode, sharing)
      ```
3. 터미널에서 아래 스크립트를 실행하여 확인
   ```
   java -version
   ```
   기대 응답
   ```
   openjdk version "17.0.11" 2024-04-16
   OpenJDK Runtime Environment Homebrew (build 17.0.11+0)
   OpenJDK 64-Bit Server VM Homebrew (build 17.0.11+0, mixed mode, sharing)
   ```