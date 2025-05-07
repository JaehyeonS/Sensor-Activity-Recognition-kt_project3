# 📱 스마트폰 센서 기반 행동 인식 AI 모델

## 📌 프로젝트 개요

스마트폰 및 웨어러블 디바이스에서 수집된 센서 데이터를 활용하여  
사용자의 **행동(정적/동적 상태)**을 분류하고, 세부적으로 6가지 활동 유형으로 인식하는 **AI 기반 행동 추론 시스템**입니다.

---

## 🎯 주요 목표

- **가속도, 자이로스코프 등** 다양한 센서 데이터를 활용
- 총 **561개의 feature**로부터 특징 추출
- 2단계 분류 구조 도입:
  - **1단계**: 정적(0) / 동적(1) 상태 분류
  - **2단계**: 각 상태별로 3가지 세부 행동 분류 (총 6가지)

---

## 🧠 분류 구조
[모델 1] → 정적(0) vs 동적(1)<br>
  ├── [모델 2-1] → Laying, Sitting, Standing<br>
  └── [모델 2-2] → Walking, Walking-Up, Walking-Down

---

## 🧾 인식 가능한 행동 목록

| 상태 유형 | 세부 행동 |
|-----------|-----------|
| 정적 상태 | Laying, Sitting, Standing |
| 동적 상태 | Walking, Walking-Up, Walking-Down |

---

## 🛠️ 적용 기술

| 항목        | 내용 |
|-------------|------|
| Language    | Python |
| Dataset     | [UCI HAR Dataset](https://archive.ics.uci.edu/ml/datasets/human+activity+recognition+using+smartphones) |
| Framework   | Keras, TensorFlow |
| Feature 수  | 561개 |
| IDE         | Google Colab, VS Code |

---

## 🧬 전체 처리 흐름

1. **센서 데이터 수집**  
   - 가속도, 자이로, Wi-Fi, 사운드 등

2. **특징 추출 (Feature Engineering)**  
   - 시간 영역: 평균, 분산, 상관계수, SMA 등  
   - 주파수 영역: FFT, 에너지, 엔트로피 등

3. **1단계 분류**  
   - 정적 상태 vs 동적 상태 분류

4. **2단계 분류**  
   - 상태별 세부 행동 분류

5. **행동 추론 결과 출력**

---
<!--
## ▶️ 실행 방법

```bash
# 필수 패키지 설치
pip install tensorflow keras pandas numpy scikit-learn

# 모델 학습
python train_model.py

# 예측 실행
python predict.py --input data/sample.csv
-->

