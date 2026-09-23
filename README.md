# Project 302

대학생을 위한 공동구매·OTT 파티 매칭 웹 서비스입니다. 상품 및 그룹을 등록하고, 채팅과 일정 조율을 통해 거래를 진행할 수 있습니다.

## Tech stack

- Java 17, Spring Boot 3.2
- Spring Data JPA, QueryDSL, MySQL
- Spring Security, OAuth2, JWT
- Thymeleaf, JavaScript
- WebSocket/STOMP, Firebase Cloud Messaging
- AWS S3, SQS

## Run locally

1. Java 17과 MySQL을 준비합니다.
2. `src/main/resources/application-example.properties`를 복사해 `application.properties`를 만들고, 로컬 환경의 값으로 채웁니다.
3. Firebase Admin SDK 키 파일을 `src/main/resources/firebase/project302-firebase-key.json`에 둡니다. 이 파일은 Git에 포함되지 않습니다.
4. 아래 명령으로 실행합니다.

```bash
./gradlew bootRun
```

Windows에서는 `gradlew.bat bootRun`을 사용합니다.

## Secret handling

- `application.properties`, Firebase 서비스 계정 JSON, 인증서·키 파일은 Git에 올리지 않습니다.
- 이미 공개된 AWS 키, JWT secret, OAuth client secret 등은 즉시 폐기하고 새 값으로 교체합니다.
- 예시 설정 파일에는 실제 값 대신 빈 값 또는 설명만 둡니다.
