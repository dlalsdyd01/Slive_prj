# SLIVE — AI 한국 수어 인식 시스템

> MediaPipe & TensorFlow.js 기반 실시간 한국 수어 인식·번역 웹 애플리케이션

![JavaScript](https://img.shields.io/badge/JavaScript-F7DF1E?style=flat-square&logo=javascript&logoColor=black)
![Python](https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=python&logoColor=white)
![Flask](https://img.shields.io/badge/Flask-000000?style=flat-square&logo=flask&logoColor=white)
![TensorFlow](https://img.shields.io/badge/TensorFlow.js-FF6F00?style=flat-square&logo=tensorflow&logoColor=white)
![MediaPipe](https://img.shields.io/badge/MediaPipe-0097A7?style=flat-square&logo=google&logoColor=white)

---
## 개발 배경

> 대한민국 청각장애인 수는 약 **40만 명**.  
> 하지만 수어를 이해하는 비장애인은 극소수입니다.

SLIVE는 이 **소통의 단절을 기술로 연결**하고자 시작된 프로젝트입니다.

별도의 앱 설치 없이, 웹브라우저 하나만으로 수어를 인식하고 번역할 수 있는  
**접근성 높은 시스템**을 목표로 했습니다.  

  

- 🤝 **MediaPipe + TensorFlow.js** — 서버 없이 브라우저에서 실시간 추론 가능
- 📊 **4가지 CNN 아키텍처 비교** — Baseline · ResNet · DenseNet · EfficientNet
- 🏆 **리더보드 시스템** — 모델 성능을 객관적으로 비교·검증

## 프로젝트 소개

SLIVE는 웹캠으로 한국 수어 제스처를 실시간으로 인식하고 번역하는 AI 시스템입니다.  
브라우저에서 직접 모델을 학습하고, 4가지 CNN 아키텍처의 성능을 비교할 수 있는 리더보드 기능을 제공합니다.

---

## 주요 기능

### 기본 시스템 (`ksl_project/`)
- **실시간 수어 인식** — 웹캠 + MediaPipe Hands로 손 랜드마크 실시간 추출
- **브라우저 내 학습** — TensorFlow.js를 활용한 클라이언트 사이드 모델 학습
- **통합 워크스페이스** — 데이터 수집, 학습, 인식을 하나의 대시보드에서 관리

### 모델 비교 시스템 (`model_comparison/`)
- **4가지 CNN 모델 비교** — Baseline / ResNet / DenseNet / EfficientNet 성능 비교
- **리더보드** — 모델별 정확도·손실 실시간 시각화
- **데이터 수집기** — 수어 제스처 학습 데이터 수집 도구

---

## 기술 스택

| 분류 | 기술 |
|------|------|
| Frontend | HTML / CSS / JavaScript |
| Backend | Python, Flask |
| AI / ML | TensorFlow.js, MediaPipe Hands |
| 모델 | Baseline CNN, ResNet, DenseNet, EfficientNet |
| 시각화 | Chart.js |

## 프로젝트 구조

```
SLIVE_prj3.1.2/
├── ksl_project Up/          # 기본 수어 인식 시스템 (포트 5000)
│   ├── app_flask.py         # Flask 백엔드
│   ├── templates/
│   │   └── workspace.html   # 통합 워크스페이스
│   ├── static/              # CSS, JS
│   ├── trained-model/       # 저장된 모델
│   └── data/                # 학습 데이터
│
└── model_comparison/        # 모델 비교 시스템 (포트 5001)
    ├── app_comparison.py    # Flask 백엔드
    ├── models/
    │   ├── baseline.py
    │   ├── resnet.py
    │   ├── densenet.py
    │   └── efficientnet.py
    ├── templates/
    ├── static/js/
    ├── data/
    ├── results/
    └── trained_models/
```
