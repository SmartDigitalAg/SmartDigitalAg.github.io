---
layout: default
title: "KSAE AX-Water Challenge 2025 대상 수상"
date: 2025-10-29
categories: news
summary: "농업용 저수지 수위 및 다출처 데이터를 활용한 저수지 운영 인공지능 모델 개발로 KSAE AX-Water Challenge 2025 대상(농림축산식품부 장관상)을 수상했습니다."
views: 0
comments: 0
likes: 0
nav: post
image: /assets/img/news/농공 AI 대상 사진.jpg
---

## KSAE AX-Water Challenge 2025 대상 수상 🏆

### 🎉 수상 내역
- **대회명**: KSAE AX-Water Challenge 2025 (Transforming Agricultural Water Management through AI)
- **수상**: 대상 (농림축산식품부 장관상, 상금 100만원)
- **수상팀**: Team SDA (정재영¹, 석승원¹, 장은수²)
- **지도교수**: 전북대학교 스마트팜학과 정재영 교수
- **시상일**: 2025년 10월 29일

<img src="/assets/img/news/농공 AI 대상 사진.jpg" alt="KSAE AX-Water Challenge 2025 대상 수상" style="max-width: 800px; width: 100%; height: auto; display: block; margin: 20px auto;">

### 📊 연구 주제

**농업용 저수지 수위 및 다출처 데이터를 활용한 저수지 운영 인공지능 모델 개발**

기후변화로 인한 집중호우와 가뭄의 빈도가 증가하면서 농업용 저수지의 효율적 관리가 중요해지고 있습니다. 본 연구는 LSTM과 GRU 딥러닝 모델을 활용하여 저수지 수위를 예측하고, 실시간 의사결정을 지원하는 웹 대시보드 서비스를 개발했습니다.

### 🔬 주요 연구 내용

**1. 파이프라인**
- **이상치 탐지 및 특성 공학**: 저수지 수위 데이터의 이상치를 탐지하고 Prophet을 통한 결측치 보정
- **시계열 담라짓 모델 학습**: JavaServer를 활용한 데이터 전처리 및 모델 학습 자동화
- **웹 대시보드 서비스**: Docker 기반 배포를 통한 실시간 모니터링 시스템 구축

**2. 모델 학습**
- **LSTM & GRU 모델 적용**: 저수지 수위 예측을 위한 순환신경망 모델 개발
- **성능 평가**: 
  - LSTM 모델 MAE 0.0505~0.0961m, RMSE 0.1309~0.0961m
  - GRU 모델 MAE 0.2772~0.0618m, RMSE 0.2977~0.0836m
- **Attention 메커니즘**: 시계열 특징 추출 및 정밀도 향상

**3. 데이터 전처리**
- Z-score 기반 이상치 탐지 및 제거
- Prophet을 활용한 결측치 보정 (RMSE 0.8m 이내)
- 저수율, 저수량, 강수량 등 다출처 데이터 통합

**4. 웹 대시보드 서비스**
- 실시간 저수지 수위 예측 모니터링
- 모델 구동 결과를 웹에서 시각화
- Feature별 기여도 분석 (SHAP 적용)
- 농업용수 공급 최적화를 위한 의사결정 지원

### 📋 연구 포스터

<img src="/assets/img/news/농공AI_포스터.png" alt="KSAE AX-Water Challenge 2025 연구 포스터" style="max-width: 900px; width: 100%; height: auto; display: block; margin: 20px auto;">

### 💡 연구 성과

본 연구는 LSTM과 GRU 모델을 활용하여 실시간 저수지 수위 예측 모델을 개발했습니다. 특히:
- 입력 변수 최적화를 통한 예측 정확도 향상
- Attention 메커니즘을 통한 모델 해석 가능성 확보
- 실시간 기상 예측 데이터와 저수지 수위 데이터를 연계하여 예측 성능 개선
- 현장 실무자나 수자원 관리 기관이 쉽게 활용할 수 있는 웹 대시보드 서비스 제공

### 🎯 의의

이번 수상은 AI 기술을 활용한 스마트 농업 용수 관리 시스템의 가능성을 입증한 성과입니다. 기후변화 시대에 농업 용수의 효율적 관리를 위한 실용적 솔루션을 제시했다는 점에서 높은 평가를 받았습니다.


*Smart Digital Agriculture Lab, Department of Smart Farm, Jeonbuk National University*