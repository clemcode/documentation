---
aliases:
- /ko/synthetics/explorer/search
description: 실행된 CI 작업의 배치를 검사하고 실패한 테스트 결과의 문제를 해결합니다.
further_reading:
- link: /continuous_testing/explorer
  tag: 설명서
  text: 신서틱 모니터링 및 연속 테스트 탐색기에 대해 알아보기
kind: 설명서
title: 검색 테스트 배치
---

## 개요

오른쪽 상단의 드롭다운 메뉴에서 시간 프레임을 선택한 후, [신서틱 모니터링 및 연속 테스트 탐색기][1]에서 **CI 배치** 이벤트 유형을 클릭하여 CI 작업 배치를 검색할 수 있습니다.

패싯을 사용하여 다음 작업을 수행할 수 있습니다.

- CI 파이프라인에서 실행 중인 최신 테스트 배치를 확인합니다.
- CI 배치를 집계하고 CI 파이프라인에 추가할 테스트 ID를 식별합니다.
- 차단 상태별로 테스트 실행 실패 횟수를 비교합니다.

## 패싯 탐색하기

왼쪽 패싯 패널에 배치 검색에 사용할 수 있는 여러 패싯이 표시됩니다. 검색 쿼리를 사용자 지정하려면 **배치**로 시작하는 패싯 목록을 클릭하세요.

### 배치 속성

**배치** 패싯을 사용하면 배치의 속성을 필터링할 수 있습니다.

| 패싯            | 설명                                                 |
|------------------|-------------------------------------------------------------|
| `Summary Status` | 배치 상태: `Passed`, `Failed`, `In Progress`. |
| `Duration`       | 배치의 전체 처리 시간입니다.                          |
| `ID`             | 배치 ID입니다.                                               |

### CI 속성

**CI** 패싯을 사용하면 배치의 CI 관련 속성을 필터링할 수 있습니다.

| 패싯          | 설명                                 |
|----------------|---------------------------------------------|
| `CI Provider`  | 배치와 연관된 CI 공급자입니다.  |
| `Job Name`     | 배치와 연관된 작업 이름입니다.     |
| `Job URL`      | 배치와 연관된 작업 URL입니다.      |
| `Pipeline ID`  | 배치와 연관된 파이프라인 ID입니다.  |
| `Pipeline Name` | 배치와 연관된 파이프라인 또는 리포지토리 이름입니다. |
| `Pipeline Number` | 배치와 연관된 파이프라인 또는 빌드 넘버입니다. |
| `Pipeline URL` | 배치와 연관된 파이프라인 URL입니다. |
| `Stage Name`   | 배치와 연관된 스테이지 이름입니다.   |

### 테스트 결과 속성

**테스트 결과** 패싯을 사용하면 실행한 테스트 결과 속성을 필터링할 수 있습니다.

| 패싯            | 설명                                                                                             |
|------------------|---------------------------------------------------------------------------------------------------------|
| <code>실행&nbsp;규칙</code> | 배치의 테스트 결과와 연관된 실행 규칙입니다: `Blocking`, `Non Blocking`, `Skipped`. |
| `Fast Retries`   | 배치의 테스트 결과와 연관된 빠른 재시도 횟수입니다.                                |
| `Location`       | 배치의 테스트 결과와 연관된 위치입니다.                                              |
| `Test ID`        | 배치의 테스트 결과와 연관된 테스트 ID입니다.                                               |
| `Test Name`      | 배치의 테스트 결과와 연관된 테스트 이름입니다.                                             |

### Git 속성

**Git** 패싯을 사용하면 배치의 Git 관련 속성을 필터링할 수 있습니다.

| 패싯       | 설명                               |
|-------------|-------------------------------------------|
| `Author Email` | 커밋 작성자의 이메일 주소입니다. |
| `Branch`    | 배치와 연관된 브랜치입니다.     |
| `Commit SHA`| 배치와 연관된 커밋 SHA입니다. |
| `Repository URL`| 배치와 연관된 Git 리포지토리 URL입니다. |
| `Tag`       | 배치와 연관된 Git 태그입니다.    |

지난 하루 동안 실행된 CI 작업 배치를 필터링하려면 `@ci.provider.name:github`와 같은 검색 쿼리를 생성하고 시간 범위를 `1d`로 설정합니다.

CI 배치에 대한 더 자세한 정보는 [검색 신택스][2]를 참조하시기 바랍니다.

## 참고 자료

{{< partial name="whats-next/whats-next.html" >}}

[1]: https://app.datadoghq.com/synthetics/explorer/
[2]: /ko/continuous_testing/explorer/search_syntax