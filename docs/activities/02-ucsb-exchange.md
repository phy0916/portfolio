# 🌎 교환학생 — UCSB (Wafer Map 결함분류)

> 🌎 **미국 UCSB(University of California, Santa Barbara) 교환학생 — 2023 Fall Quarter (SAF 파견)**
>
> 4학년 2학기에 UCSB로 파견되어 대학원 연계 수준의 머신러닝 수업 2과목을 수강하며 CNN 기반 Wafer Map 결함 분류, 금속 표면 Crescent 결함 인식 프로젝트를 수행했습니다. 이 경험이 로봇 제어 중심이던 제 진로에 AI라는 두 번째 축을 만들어줬습니다.

> 📷 **사진 자리** — UCSB 캠퍼스·수업·친구들과의 사진을 넣어주세요.

## 📋 개요

| | |
|---|---|
| **기간·기관** | 2023 Fall Quarter · University of California, Santa Barbara (SAF 교환 프로그램) |
| **수강 과목** | Machine Learning · Machine Learning in Design & Test (ME 157A/272A) · Business and Personal Branding (PaCE) · Class Piano |
| **프로젝트** | CNN 기반 Wafer Map Classification · Crescent Shape Defect on Metallic Surface 분류 신경망 |

## 📚 공부한 것 — 과목별 학습 정리

### 1) Machine Learning (4학년 전공)

이론과 수학적 기초를 매주 과제(Jupyter Notebook)로 직접 구현하며 학습했습니다. 실제 수행한 과제·실습 커리큘럼:

- **확률·통계 기초** — 확률 이론(ProbTheory), Mean and Covariance 계산 실습
- **선형 모델** — Linear Regression을 Normal Equations(정규방정식)로 직접 유도·구현, Gradient Descent 구현 비교
- **최우추정(MLE)** — Linear Dynamic System 예제로 Matrix Exponentiation 기반 MLE 실습
- **차원 축소·분류** — SVD(특이값 분해) 실습, SVM과 PCA를 결합한 분류 예제, sklearn 모델 실습
- **신경망** — PyTorch로 NN Classifier 구현 (HW2\~HW9, Final 프로젝트까지 총 9회차 과제 수행)
- 벡터·행렬 해석으로 신경망이 작동하는 원리를 손으로 풀어보는 방식의 수업이라, "블랙박스가 아닌 수식으로 이해하는 ML"의 기반을 얻었습니다

### 2) Machine Learning in Design & Test (ME 157A/272A, 학부·대학원 합반)

제조·설계 관점에서 ML을 다루는 수업으로, IEA(Intelligent Engineering Analysis)의 과거·현재·미래, ML 접근법 분류(ML 101), CNN(lecture 10), LLM(lecture 11), Design & Test 방법론(lecture 12)을 학습했습니다. 수업 프로젝트로:

- **Wafer Map Classification** — 실제 반도체 공정 기반 Wafer Map 데이터로 결함 분포 패턴을 CNN으로 분류. 데이터 노이즈·클래스 불균형으로 초기 정확도가 낮았는데, 전처리·피처 구성을 재설계하고 학습 구조를 조정해 **분류 정확도 90% 이상** 달성
- **Crescent Shape Defect on Metallic Surface** — 금속 표면의 초승달형 결함을 구별하는 신경망을 팀 프로젝트로 구축, 다국적 팀원들과 협업
- 담당 교수와 수업 후에도 이메일로 안부를 주고받을 만큼 가깝게 교류하며, 질문 중심의 미국식 수업 문화를 최대한 활용

### 3) Business and Personal Branding (PaCE)

유럽권 학생들과의 팀 프로젝트·최종 발표가 있는 수업으로, 기술 외 영역에서 영어 프레젠테이션·협업을 훈련했습니다.

### 4) Class Piano

전공생 없는 소규모 피아노 수업 — 매 수업 개별 피드백을 받는 환경에서 취미(음악)를 학점과 함께 유지했습니다.

## 🌱 성장 경험

- 기숙사 다국적 룸메이트 환경, SAF 동기·일본인 친구들과의 서부 여행 등 이질적 문화 속 관계 맺기를 체득 — 이후 KETI에서 외국 장비사와 협업할 때의 기반이 됨
- REC CEN 테니스·서핑 수업 수강, 할로윈 등 현지 문화 참여
- SAF Alumni 공식 후기문 기고 (2024.01) — 후배들을 위한 준비 절차·수강 전략 정리
- 매달 생활양식보고서(9\~12월) 작성으로 경험을 기록·회고

## 🧰 기술 스택

`CNN` `PyTorch` `TensorFlow` `SVM·PCA` `SVD` `MLE` `Normal Equations` `Wafer Map` `데이터 전처리` `글로벌 협업`
