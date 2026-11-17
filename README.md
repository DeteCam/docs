<div align="center">
<img src="https://raw.githubusercontent.com/DeteCam/.github/main/profile/assets/logo.png" width="96" alt="DeteCam">

# DeteCam 문서

**Wi-Fi 송출형 초소형 카메라 탐지 및 위치 추정 시스템**의 원칙 · 시스템 명세 · 설계 · 조사 · 검증

</div>

이 저장소는 코드가 없는 문서 저장소입니다. 세 저장소([receiver](https://github.com/DeteCam/receiver) · [app](https://github.com/DeteCam/app) · [ai](https://github.com/DeteCam/ai))에 걸치는 내용을 여기에 둡니다. 저장소 하나에만 해당하는 문서는 그 저장소의 `docs/` 와 `specs/` 에 있습니다.

## 읽는 순서

| 순서 | 문서 | 내용 |
|---|---|---|
| 1 | [원칙](constitution.md) | 모든 저장소가 지키는 다섯 가지 원칙 |
| 2 | [시스템 명세 000](specs/000-system/spec.md) | 무엇을 만드는가, 어디까지 하는가, 얼마나 잘해야 하는가 |
| 3 | [시스템 설계서](design/시스템%20설계서.md) | 구성 요소, 주고받는 것, 동작 순서 |
| 4 | [교실 전파 시뮬레이션](verification/교실%20전파%20시뮬레이션.md) | 40명 교실에서 카메라 자리를 찾을 수 있는가 (전파 경로 계산) |
| 5 | [유용성 근거](research/유용성%20근거.md) | 왜 필요한가: 통계, 사건, 기존 탐지기의 한계 |
| 6 | [비콘 검토](research/비콘%20검토.md) | 아무도 보고 있지 않은 핫스팟 카메라를 찾을 수 있나 |

## 폴더

```
constitution.md        프로젝트 원칙
specs/000-system/      시스템 전체 스펙 (spec → plan → tasks)
design/                시스템 설계서
research/              조사 노트 (필요성, 관련 연구, 대상 카메라)
verification/          검증 결과 (시뮬레이션, 실험)
```

## 스펙 주도 개발 (SDD)

기능은 **스펙을 먼저 쓰고** 만듭니다. `spec.md`(무엇을·왜) → `plan.md`(어떻게) → `tasks.md`(할 일). 스펙 번호는 저장소마다 001 부터, 시스템 전체는 이 저장소의 000 입니다. 자세한 규칙은 [CONTRIBUTING](https://github.com/DeteCam/.github/blob/main/CONTRIBUTING.md).

| 저장소 | 스펙 |
|---|---|
| docs | [000 시스템](specs/000-system/spec.md) |
| receiver | [001 방향 찾기](https://github.com/DeteCam/receiver/tree/main/specs/001-direction-finding) · [002 위치 추정](https://github.com/DeteCam/receiver/tree/main/specs/002-position-estimation) · [003 기구](https://github.com/DeteCam/receiver/tree/main/specs/003-mechanics) · [004 탐지](https://github.com/DeteCam/receiver/tree/main/specs/004-detection) · [005 혼자 동작](https://github.com/DeteCam/receiver/tree/main/specs/005-standalone-control) |
| app | [001 수신기 조종](https://github.com/DeteCam/app/tree/main/specs/001-receiver-control) · [002 AR 표시](https://github.com/DeteCam/app/tree/main/specs/002-ar-zone-display) |
| ai | [001 의심 점수](https://github.com/DeteCam/ai/tree/main/specs/001-suspicion-score) · [002 곡선 읽기](https://github.com/DeteCam/ai/tree/main/specs/002-curve-reader) |
