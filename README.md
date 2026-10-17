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

## 검사 기준 (PR 병합 조건)
- 커밋: `type: subject` (subject 50자 이하, 끝 특수문자 없음, 본문은 불릿)
- 테스트 커버리지 80% 이상
- SonarCloud Major 이슈 0
- 네이버 핵데이 Java 컨벤션 (checkstyle)
