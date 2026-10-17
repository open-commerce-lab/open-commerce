# Open-Commerce Study

C4-ComeTrue의 [Opener-Market 과제](assignment/opener-market.md)를 각자 구현하고 서로 리뷰하는 스터디 레포입니다.
(원문 출처: https://github.com/C4-ComeTrue/c4-cometrue-assignment)

## 참가자
| 이름 | 대표 브랜치 |
|---|---|
| chooh1010 | [chooh1010](../../tree/chooh1010) |

## 진행 규칙
- 각자 대표 브랜치(GitHub 아이디)를 만들고, Step마다 `feature/{대표 브랜치}_stepN` 브랜치에서 작업합니다.
- PR은 `대표 브랜치 ← Step 브랜치`. 다른 참가자 1명 이상 승인 필수, 리뷰어는 참가자 전원 지정 권장.
- 포크하지 말고 이 레포에 직접 브랜치를 올립니다(포크 PR에는 SonarCloud 토큰이 전달되지 않음).
- 클론 후 `git config core.hooksPath .githooks` 한 번 실행.
- 설계와 성능 목표는 공통 [서비스 규모 가정](docs/scale-assumptions.md)을 기준으로 합니다.

## 검사 기준 (PR 병합 조건)
- 커밋: `type: subject` (subject 50자 이하, 끝 특수문자 없음, 제목과 본문 사이 빈 줄, 본문은 줄마다 불릿, 한 줄 72자 이하 권장)
- 테스트 커버리지 80% 이상
- SonarCloud Major 이슈 0
- 네이버 핵데이 Java 컨벤션 (checkstyle)

## 프로젝트 설정
레포 루트에 Spring Boot(Gradle, Java 21) 프로젝트를 만들고, `build.gradle`에 아래 두 가지를 추가합니다.
커버리지·checkstyle·SonarCloud 설정은 `main`의 [`gradle/quality.gradle`](gradle/quality.gradle)에서 공통으로 관리합니다.

```groovy
plugins {
    // ... Spring Boot 기본 플러그인
    id 'org.sonarqube' version '7.5.0.8588'
}

apply from: 'gradle/quality.gradle'
```

- `./gradlew build`에 테스트, checkstyle(경고 0개), 라인 커버리지 80% 검증이 포함됩니다.
- 공통 설정이 바뀌면 `main`을 대표 브랜치에 병합해 반영합니다.
