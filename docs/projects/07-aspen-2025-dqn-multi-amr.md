# 📄 ASPEN 2025 — DQN 기반 다중 AMR 경로계획

> 📄 **Deep Q-Network Approach to Path Planning and Scheduling of Multiple AMRs in Semiconductor Manufacturing (ASPEN 2025)**
>
> 반도체 제조 환경에서 다중 AMR의 경로계획·작업 스케줄링을 DQN 강화학습으로 최적화한 연구입니다. KETI 지능로보틱스연구센터에서 수행해 ASPEN 2025 국제학술대회(대만)에서 발표했습니다.

> 📷 **사진 자리** — 발표 현장 사진, 시뮬레이션 맵, 성과 그래프를 넣어주세요.

## 📋 개요

| | |
|---|---|
| **유형** | 국제학술대회 발표 (ASPEN 2025, 대만) · 국외출장 |
| **수행기관** | KETI 지능로보틱스연구센터 (Intelligent Robotics Research Center) |
| **키워드** | Deep Q-Network, Reinforcement Learning, Path Planning, Multi-AMR, Semiconductor Manufacturing |
| **연계 과제** | 첨단로봇 과제(AOI 무인화)의 다중 AMR 경로 최적화 연구를 학술 성과로 발전 |

## 🎯 연구 배경 — 왜 이 연구를 했나

반도체 제조에는 sawing·bonding·packaging 등 수많은 자동화 장비가 있고, 높은 처리량을 유지하려면 효율적인 자재 이송이 필수입니다. AMR 도입은 늘고 있지만 **혼잡하고 동적인 생산 환경에서 다수 AMR의 경로와 작업 순서를 조율하는 문제**는 여전히 난제입니다. 기존 방법(A<i>, CBS, ORCA, MILP 등 그래프 탐색·최적화·규칙 기반)은 환경이 바뀔 때마다 재계획이 필요하고 로봇 수가 늘수록 계산량이 급증합니다. 반면 DQN 기반 방법은 학습 후 추론 비용이 낮고, 학습된 정책으로 실시간 대응이 가능하며, 분산 정책으로 확장성이 좋다는 점에 착안해 DQN 기반 다중 AMR 경로계획·스케줄링 프레임워크</i>\*를 제안했습니다.

## 🎬 실험 시나리오

그리드 맵 위에 PCB 공급대(SUP), 장비 4대(M), 완성품 배출대(SINK)를 배치하고 AMR 3대가 협력하는 시나리오입니다.

1. 로봇이 SUP에서 PCB를 픽업
2. 각 로봇이 장비로 이동해 PCB 투입 → 장비 가공(40 스텝)
3. 가공 완료 시 로봇이 PCB를 회수해 SINK 컨베이어에 안착
4. 목표: 최대 3,000 스텝 안에 10개 제품 완성

**보상 설계** — 스텝당 -0.05(시간 패널티) · 회전/정지 -0.05 · 올바른 Pick +10 / 잘못된 Pick -3 · Place +10 · SINK 완료 +300

## 🛠️ 제안 방법

- **네트워크 구조** — Double DQN + Dueling Network. 상태 벡터 입력 → FC 3층(ReLU) → 7개 행동의 Q값 출력. AMR별 독립 V/A 스트림으로 타깃 네트워크 갱신
- **학습 안정화 3기법**
    - Action Masking — 이동 불가 방향을 출력에서 배제해 무의미한 학습 제거·안정성 향상
    - Curriculum Learning — 로봇 1대 환경에서 시작해 단계적으로 로봇 수를 늘려 학습 안정성 확보
    - Safe Greedy Rollout — 학습된 정책의 실제 rollout 시 충돌 위험 행동을 마스크로 제한해 안전하게 탐색
- **하이퍼파라미터** — lr 3e-4(단계별 조정) · Adam(weight\_decay 1e-5) · γ 0.995 · τ 1e-3 · batch 256 · replay buffer 300,000 · warm-up 1,000 스텝 · 5단계 학습 · 총 2,000 에피소드

## 📈 결과

- **성공률: Double DQN > DQN > Q-learning** — Double DQN이 600 에피소드 기준 **성공률 90% 이상** 달성
- **평균 보상: Double DQN 최고** — 학습 후반 오버슈팅 거의 없이 최고 평균 보상 유지
- **충돌 횟수: Q-learning > DQN > Double DQN** — 심층 신경망 기반 Q함수 근사가 복잡한 다중 AMR 환경을 효과적으로 모델링함을 입증

## 🔭 한계 및 후속 연구

학습 시간, 급격히 커지는 상태공간, 로봇별 독립 학습이라는 한계를 확인했고, 이를 극복하기 위한 **Multi-Agent DQN(MADQN)** 연구의 필요성을 제시했습니다. 또한 실제 PCB 제조 시스템 기반 디지털트윈을 추가 구축해 다양한 환경에서 DQN 활용 연구를 이어갈 계획을 발표했습니다.

## 📎 산출물

- ASPEN 2025 발표자료 (DQN v1\~v4) · AOI 관련 발표자료(ASPEN PPT\_AOI 제출용) 제작 참여
- 첨단로봇 과제 연차보고서의 DQN 실험 파트로 연구 내용 반영

## 🧰 기술 스택

`DQN · Double DQN · Dueling` `강화학습` `Action Masking` `Curriculum Learning` `다중 AMR` `경로계획·스케줄링` `반도체 물류`
