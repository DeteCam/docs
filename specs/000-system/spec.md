# 시스템 스펙 000: DeteCam 5.0 (Palm-12) 통합 시스템

## 1. 시스템 구성
- **수신기 3기 (`DeteCam/receiver`)**: `120 × 120 × 30.6 mm` 손바닥 크기 벽면 부착·직교 2축 스위블(`Pan ±30°`, `Tilt 0°/-15°/-25°`), `112×112 mm` 4층 통합 12+1소자 RF PCB + `Radxa ROCK 3A` (`VesperCSI` ARM64) + `Intel AX210NGW` + `AD8317` + 5 V 보조배터리 무선 구동.
- **알고리즘 (`DeteCam/ai`)**: 3단계 카메라 판별(`score.py`), `TriF v12` (`CM-RCLPA` + `C⁻¹` + `Capon` + `CV_f` + 10면 가상 거울 앵커 + `RAPS 90% AR`), 벽면 스위블 `AR-OPA` + `Auto-Verify`.
- **안드로이드 앱 (`DeteCam/app`)**: ARCore 10초 방 스캔 → 벽면 위치·클릭 각도 AR 안내 → ArUco 자동 좌표 등록 → 90% AR 구역 표시.

## 2. 시스템 경계
- **정밀 3D 위치**: 2.4 / 5 GHz Wi-Fi 송출 카메라 (전 채널 지원).
- **구역 경보**: LTE/5G 유심 카메라 (`AD8317×3` 교차 차감), BLE 카메라 (내장 Bluetooth 5.3).
- **범위 밖**: SD 단독 저장·전원 꺼진 카메라, 재밍, 패킷 복호화.
