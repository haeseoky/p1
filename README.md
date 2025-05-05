# 안드로이드 웹 브라우저 애플리케이션

이 프로젝트는 Android와 Kotlin을 사용하여 구현된 간단한 웹 브라우저 애플리케이션입니다. WebView를 기반으로 웹 페이지를 표시하고, 다양한 기능을 제공합니다.

## 주요 기능

- 웹 페이지 탐색 및 URL 입력
- 주요 포털 사이트(Google, Naver, Daum) 바로가기
- 전화 걸기 기능
- SMS 전송 기능
- 이메일 전송 기능
- 현재 웹 페이지 공유 기능
- 기본 브라우저로 현재 URL 열기 기능
- 뒤로 가기 기능 지원

## 기술 스택

- Kotlin 1.3.0
- Android SDK 28 (Android 9 Pie)
- Anko 라이브러리 0.10.7
- WebView를 활용한 웹 페이지 렌더링
- Intent를 활용한 다양한 액션 처리

## 프로젝트 구조

```
app/
├── src/
│   ├── main/
│   │   ├── java/hs/falcontag/mywebbrowser/
│   │   │   └── MainActivity.kt     - 메인 액티비티 구현
│   │   ├── res/
│   │   │   ├── layout/
│   │   │   │   └── activity_main.xml  - 메인 화면 레이아웃
│   │   │   ├── menu/
│   │   │   │   ├── main.xml        - 메인 메뉴 정의
│   │   │   │   └── context.xml     - 컨텍스트 메뉴 정의
│   │   │   └── ...
│   │   └── AndroidManifest.xml     - 애플리케이션 매니페스트
│   └── ...
└── build.gradle                    - 애플리케이션 빌드 스크립트
```

## 구현 세부 사항

### 기본 기능

- WebView를 사용하여 웹 페이지 렌더링
- JavaScript 활성화 설정
- 주소 입력창에서 URL 입력 후 검색 가능
- 시스템 뒤로 가기 버튼 처리로 이전 페이지로 이동 가능

### 메뉴 기능

- 옵션 메뉴: 주요 포털 사이트로 이동, 전화 걸기, SMS 전송, 이메일 전송
- 컨텍스트 메뉴: 현재 페이지 공유, 기본 브라우저로 열기

### Anko 라이브러리 활용

- 간편한 Intent 처리 (전화 걸기, SMS 전송, 이메일 전송, 공유 등)
- Kotlin 확장 함수를 활용한 간결한 코드 작성

## 시작하기

### 필수 조건

- Android Studio 3.2 이상
- JDK 8 이상
- Android SDK 19 이상 (minSdkVersion 19)

### 설치 및 실행

1. 프로젝트 클론:
   ```bash
   git clone https://github.com/haeseoky/p1.git
   ```

2. Android Studio에서 프로젝트 열기

3. Gradle 동기화

4. 애플리케이션 실행 (에뮬레이터 또는 실제 기기)

## 주의 사항

- 인터넷 권한이 필요합니다 (AndroidManifest.xml에 `<uses-permission android:name="android.permission.INTERNET" />` 권한 추가됨)
- HTTP 연결을 위해 `android:usesCleartextTraffic="true"` 설정이 추가되어 있습니다 (프로덕션 환경에서는 보안 연결 사용 권장)

## 향후 개선 사항

- 북마크 기능 추가
- 다운로드 기능 구현
- 히스토리 기능 추가
- 탭 브라우징 지원
- 다크 모드 지원
