<div align="center">
<img src="https://raw.githubusercontent.com/DeteCam/.github/main/profile/assets/logo.png" width="96" alt="DeteCam">

# DeteCam 문서

**Wi-Fi 송출형 초소형 카메라 탐지 및 위치 추정 시스템**의 원칙 · 시스템 명세 · 설계 · 조사 · 검증

</div>

이 저장소는 코드가 없는 문서 저장소입니다. 세 저장소([receiver](https://github.com/DeteCam/receiver) · [app](https://github.com/DeteCam/app) · [ai](https://github.com/DeteCam/ai))에 걸치는 내용을 여기에 둡니다. 저장소 하나에만 해당하는 문서(부품표, 조립 안내, 계산 코드)는 그 저장소에 있습니다.

![시스템 구성도](https://raw.githubusercontent.com/DeteCam/receiver/main/docs/images/%EC%84%A4%EA%B3%84%EB%8F%84_%EC%8B%9C%EC%8A%A4%ED%85%9C_%EA%B5%AC%EC%84%B1.png)

## 읽는 순서

| 순서 | 문서 | 내용 |
|---|---|---|
| 1 | [원칙](constitution.md) | 모든 저장소가 지키는 다섯 가지 원칙 |
| 2 | [시스템 명세 000](specs/000-system/spec.md) | 무엇을 만드는가, 어디까지 하는가, 얼마나 잘해야 하는가 |
| 3 | [시스템 설계서](design/시스템%20설계서.md) | 구성 요소, 동작 순서, 주고받는 것, 설계에서 고른 것 |
| 4 | [사전 검증 요약](verification/사전%20검증.md) | 부품을 사기 전에 확인한 것, 싼 것부터 사는 순서, 관문 1~5 를 사기 전에 판정 |
| 5 | [교실 전파 시뮬레이션](verification/교실%20전파%20시뮬레이션.md) | 40석 교실에서 카메라 자리를 찾을 수 있는가 |
| 6 | [숙소 방 계산](verification/숙소%20방%20계산.md) | 숙소 방에 숨긴 카메라의 자리를 찾을 수 있는가 |
| 7 | [유용성 근거](research/유용성%20근거.md) | 왜 필요한가: 통계, 사건, 기존 탐지기의 한계 |
| 8 | [비콘 검토](research/비콘%20검토.md) | 아무도 보고 있지 않은 핫스팟 카메라를 찾을 수 있나 |
| 9 | [전파 넓히기 검토](research/전파%20넓히기%20검토.md) | 카메라 → 폰 → AI → 이어폰의 사슬, LTE·5G·블루투스를 어디까지 잡을 수 있나 |
| 10 | [종합설계 요약 계획서](plan/종합설계%20요약%20계획서.md) | 학교 양식의 한 쪽짜리 계획서 ([PDF](plan/종합설계%20요약%20계획서.pdf)) |

수신기의 그림과 자세한 숫자: [설계도](https://github.com/DeteCam/receiver/blob/main/docs/%EC%84%A4%EA%B3%84%EB%8F%84.md) · [데모 환경](https://github.com/DeteCam/receiver/blob/main/docs/%EB%8D%B0%EB%AA%A8%20%ED%99%98%EA%B2%BD.md) · [설계 검토](https://github.com/DeteCam/receiver/blob/main/docs/%EC%84%A4%EA%B3%84%20%EA%B2%80%ED%86%A0.md)

## 폴더

```
constitution.md        프로젝트 원칙
specs/000-system/      시스템 전체 스펙 (spec → plan → tasks)
design/                시스템 설계서
research/              조사 노트 (필요성, 대상 카메라, 전파 넓히기)
verification/          검증 요약 (계산, 실험). 자세한 것은 receiver 저장소
plan/                  학교에 내는 계획서 (한 쪽 요약 계획서)
```

## 스펙 주도 개발 (SDD)

기능은 **스펙을 먼저 쓰고** 만듭니다. `spec.md`(무엇을·왜) → `plan.md`(어떻게) → `tasks.md`(할 일). 스펙 번호는 저장소마다 001 부터, 시스템 전체는 이 저장소의 000 입니다. 자세한 규칙은 [CONTRIBUTING](https://github.com/DeteCam/.github/blob/main/CONTRIBUTING.md).

| 저장소 | 스펙 |
|---|---|
| docs | [000 시스템](specs/000-system/spec.md) |
| receiver | [006 패널 수신기](https://github.com/DeteCam/receiver/tree/main/specs/006-panel-receiver) (지금 구조, 혼자 동작 포함) · [004 탐지](https://github.com/DeteCam/receiver/tree/main/specs/004-detection) · 001·002·003·005 는 돌판 수신기 때의 것이라 [receiver-legacy](https://github.com/DeteCam/receiver-legacy) 로 옮겼다 |
| app | [001 수신기 조종](https://github.com/DeteCam/app/tree/main/specs/001-receiver-control) · [002 AR 표시](https://github.com/DeteCam/app/tree/main/specs/002-ar-zone-display) |
| ai | [001 의심 점수](https://github.com/DeteCam/ai/tree/main/specs/001-suspicion-score) · [002 자리 모델](https://github.com/DeteCam/ai/tree/main/specs/002-position-model) |
