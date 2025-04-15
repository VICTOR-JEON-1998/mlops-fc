# ⚽ mlops-fc – 축구선수 이적료 예측 MLOps 프로젝트

**MLOps 실전 포트폴리오 프로젝트**입니다.  
이 프로젝트는 축구 선수의 이적 데이터를 바탕으로,  
선수의 스탯과 커리어 정보를 활용해 **이적료를 예측하는 머신러닝 모델을 구축하고**,  
이를 **실험 추적 / 모델 서빙 / 자동화 / 배포 / 모니터링**까지 이어지는 **End-to-End MLOps 파이프라인**으로 구현하는 것을 목표로 합니다.

> 축구와 머신러닝, MLOps를 한 번에!

---

## 🎯 프로젝트 목표

- 선수 데이터 기반 이적료 예측 모델 학습 (scikit-learn)
- MLflow로 실험 추적 및 버전 관리
- FastAPI로 예측 API 서빙
- Docker로 컨테이너화 및 실행 환경 통제
- GitHub Actions로 retrain 및 자동화 구성
- (선택) Kubernetes 배포 및 Prometheus 모니터링 구성

---

## 📁 프로젝트 구조

```
mlops-fc/
│
├── data/                  # 원본 데이터 및 전처리 파일
├── notebooks/             # EDA 및 실험용 노트북
├── src/
│   ├── train.py           # 모델 학습 및 저장
│   ├── predict.py         # 예측 테스트 스크립트
│   └── inference_server/  # FastAPI 서버
│       └── main.py
│
├── mlflow/                # MLflow tracking 설정
├── docker/                # Dockerfile & 실행 스크립트
├── .github/workflows/     # GitHub Actions 자동화
├── monitoring/            # Prometheus, Grafana 설정 파일
└── README.md
```

---

## 🚀 실행 방법

1. 가상환경 설정 및 의존성 설치
```bash
python -m venv venv
source venv/bin/activate
pip install -r requirements.txt
```

2. 데이터 전처리 및 모델 학습
```bash
python src/train.py
```

3. 예측 테스트 (로컬)
```bash
python src/predict.py
```

4. FastAPI 서버 실행
```bash
uvicorn src.inference_server.main:app --reload
```

5. MLflow UI 실행
```bash
mlflow ui
# → http://localhost:5000 에서 실험 확인
```

---

## 🔗 연계 블로그 시리즈

> 이 프로젝트의 모든 구현 과정은 블로그 시리즈로 정리되어 있습니다.

📚 [티스토리 블로그: MLOps 실전 – 축구선수 이적료 예측 프로젝트](https://jeon-maker.tistory.com/)

---

## 🧠 사용 기술 스택

- Python, scikit-learn, pandas
- FastAPI, Docker, MLflow
- GitHub Actions
- (선택) Kubernetes, Prometheus, Grafana

---

## ✨ 기여 / 참고

이 프로젝트는 포트폴리오 및 MLOps 학습 목적으로 진행되었습니다.  
데이터는 Kaggle에서 수집되었으며, 실제 기업용 모델이 아닌 학습 목적의 구조입니다.

---

## 📫 Contact

> 문의 또는 피드백은 언제든 환영합니다!

```
Author: VICTOR 
Blog: [https://jeon-maker.tistory.com/]  
GitHub: [https://github.com/VICTOR-JEON-1998] 
```
