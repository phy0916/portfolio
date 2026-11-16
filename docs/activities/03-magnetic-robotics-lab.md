# 🧲 학부연구생 — 마그네틱 로보틱스랩

> 🧲 **학부연구생 (인턴) — 마그네틱 로보틱스 랩 (Magnetic Robotics Lab)**
>
> 겨울방학 학부연구생으로 자기장 구동 마이크로로봇 연구실에서 활동하며, 의료용 무선 자기 로봇의 구동·위치추정 분야 핵심 논문 5편을 정독하고 랩 세미나에서 논문 리뷰를 발표했습니다. "논문을 수식 단위로 읽고 남에게 설명하는" 연구 훈련을 처음 받은 경험입니다.

> 📷 **사진 자리** — 랩 세미나·연구실 사진을 넣어주세요.

## 📋 개요

| | |
|---|---|
| **활동** | 학부연구생(겨울방학 인턴) — 광운대 마그네틱 로보틱스 랩 |
| **연구 분야** | 자기장 기반 무선(untethered) 마이크로로봇의 구동·항법·위치추정 (의료 응용) |
| **주요 활동** | 핵심 논문 5편 정독·정리, 랩 세미나 논문 리뷰 발표 (04\_논문 리뷰) |

## 📚 공부한 것 — 정독한 논문 5편

1. **Expanded equations for torque and force on a cylindrical permanent magnet core in a large-gap magnetic suspension system** — 대공극 자기부상계에서 원통형 영구자석 코어에 걸리는 토크·힘의 확장 방정식 (자기 구동의 역학 기초)
2. **Magnetic navigation system with gradient and uniform saddle coils** — 혈관 내 마이크로로봇 무선 조작을 위한 gradient·uniform 새들 코일 항법 시스템
3. **Crawling microrobot actuated by a magnetic navigation system in tubular environments** — 관형 환경(혈관 등)에서 자기 항법으로 구동되는 크롤링 마이크로로봇
4. **Magnetic navigation system for the precise helical propulsion** (Jeon et al., 2012) — 나선 추진 정밀 제어
5. **A 5-D Localization Method for a Magnetically Manipulated Untethered Robot Using a 2-D Array of Hall-Effect Sensors** (Son, Yim, Sitti — IEEE) — **세미나 발표 논문**

## 🎤 세미나 발표 — 5-D Localization 논문 리뷰 (수식 레벨 정리)

IEEE 저자(Metin Sitti 그룹)의 논문을 23장 슬라이드로 정리해 발표했습니다. 제가 정리한 핵심 논리:

- **문제 정의** — 자기 캡슐 내시경(MACE)류 로봇은 구동용 강한 외부 자기장이 센서 어레이를 간섭해 기존 위치추정법이 실패하고, 내장 자기 센서 방식은 회전 구동만 가능하며 각도 정확도가 진단용으로 부족함
- **핵심 아이디어 ① 자기장 분리** — 센서 측정값 Bs = 외부 전자석 자기장 Be + 로봇 자기장 Bc 로 모델링하고, 전자석 자기장(dipole 방정식 모델)을 빼서 로봇의 순수 자기장을 분리
- **핵심 아이디어 ② 2차 방향 미분** — 자기장의 Laplacian 성질(전류·변화 전기장이 없을 때 ∇²B=0, Maxwell 방정식 기반)을 이용해 z방향 2차 미분으로 오차·노이즈를 추가 억제. 이때 센서 노드 간격 h와 격자 측정값 Bij로 이산 미분을 구성
- **신호 품질 지표** — Signal Quality Ratio(SQR)를 정의해, 2차 미분 방식(SQR\_L)이 단순 감산 방식(SQR\_B)보다 신호 대 잡음 우위임을 실험으로 검증
- **추정 알고리즘** — 측정 자기장과 모델 자기장의 오차를 Levenberg-Marquardt 최적화로 최소화해 위치 3 + 자세 2 (자기모멘트 회전축 제외) 총 5-DOF를 추정
- **시스템 구성** — 64개 홀센서 2-D 어레이(z방향 성분 측정), DAQ+멀티플렉서(3bit) 채널 제약, LabVIEW 기반 메인 알고리즘·GUI
- **한계 분석** — 50mm 이상 거리에서 SQR이 5dB 이하로 떨어져(노이즈·오차가 신호의 36% 이상) 유효 추정 범위가 제한됨 — Seff(유효 위치추정 범위) 개념으로 정리

## 🌱 배운 것

- 논문을 결론이 아니라 **가정→모델→수식→실험 검증** 순서로 해체해서 읽는 방법
- Maxwell 방정식·dipole 모델 같은 물리 기초가 실제 로봇 시스템 설계(센서 배치·필터링)로 이어지는 과정
- 이때 훈련한 "수식 레벨 논문 읽기"가 이후 캡스톤 역기구학 재구성과 KETI에서의 알고리즘 구현에 직접적인 밑거름이 됨

## 🧰 기술 스택

`자기 구동 마이크로로봇` `5-DOF Localization` `Hall-effect Sensor Array` `Levenberg-Marquardt` `Maxwell 방정식` `논문 리뷰·세미나 발표`
