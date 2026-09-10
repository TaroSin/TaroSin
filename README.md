<div align="center">

![header](https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=10&height=160&text=TaroSin's%20GitHub&fontSize=45&animation=twinkling&fontAlign=68&fontAlignY=36)

### AI / ML Engineer

**LLM · Document AI · Recommendation System**

Why에서 출발해 How로 성과를 만드는 AI/ML 엔지니어입니다.

기술 자체보다 **문제 정의 · 성공 지표 · 운영 제약**을 먼저 정리하고,  
현재 문제에 가장 합리적인 방법을 선택해 End-to-End 시스템으로 연결하는 데 관심이 있습니다.

<br>

<a href="https://github.com/user-attachments/files/31997153/_.pdf">
  <img src="https://img.shields.io/badge/Resume-Download-4285F4?style=for-the-badge&logo=googledocs&logoColor=white"/>
</a>

<a href="https://github.com/user-attachments/files/31948323/_.pdf">
  <img src="https://img.shields.io/badge/Portfolio-Download-FF6B6B?style=for-the-badge&logo=readthedocs&logoColor=white"/>
</a>

</div>

## 💼 Experience

### ㈜아이씨티웨이
**AI Engineer · 정보기술연구소**  
`2025.10 ~ Present`

- 폐쇄망 환경의 **Spatial Text2SQL** 시스템 설계 및 개발
- 비정형 PDF를 구조화 데이터로 변환하는 **Document AI Parser** 구축
- LLM/VLM 모델링부터 Backend, GPU Inference, DevOps까지 End-to-End 개발

<br>

### ㈜제논
**AI Engineer Intern · DS**  
`2025.04 ~ 2025.06`

- **Flowise 기반 AI Agent** 설계 및 구축
- Nike 신발 불량 탐지 모델 개발 및 **데이터 수집·품질관리(DQ)**
- 응급실 특화 AI 기반 임상지원시스템 의료 데이터 분석/ML 모델링

---

## 🚀 Featured Projects

### 📄 Document Parser

표·체크박스·이미지·도면이 혼재된 비정형 PDF를  
**근거 추적 가능한 구조화 데이터로 변환하고 HITL 검수와 DB 적재까지 연결하는  
End-to-End Document AI Pipeline**

- OCR 직접 매핑과 문서 전체 일괄 추출 방식을 비교하고  
  **양식 판별 → 구조 판단 → 값 추출 → 검수** 단계로 파이프라인 분리
- 제목·표 특징을 활용한 **Section Ownership 판단 및 페이지 간 Carry-over** 구현
- 제목이 생략된 후속 표에서도 상위 분류를 유지하고 새로운 섹션 경계에서 잘못된 상속 방지
- 양식별 템플릿 기반 필드·표·체크박스 추출 및 값 정규화
- `page / block / bbox` 기반으로 원본 PDF와 추출 결과 간 Evidence 추적
- 의심 값의 근거와 오류 사유를 제공하는 **HITL Review UI** 및 수정 후 최종 출력 재생성
- 차단 이슈가 남은 문서의 DB 적재를 제한하는 검증 Workflow 구성

**Evaluation — 7 Templates / 200 Documents**

- Field Extraction F1: **96.8%**
- Carry-over Accuracy: **97.4%**
- Review Error Recall: **95.8%**
- 추가 수정 없이 적재 가능한 문서 비율: **81.5%**

`Chandra OCR` `Flask` `PostgreSQL` `ChromaDB` `LangChain` `vLLM` `Gemma 4` `Docker` `Rocky Linux` `Python`

<br>

### 🗺️ Spatial Text2SQL

폐쇄망 환경에서 SQL과 공간 함수에 익숙하지 않은 사용자도  
자연어로 공간 데이터를 조회할 수 있도록 구축한  
**PostGIS 특화 Text2SQL 및 SQL 실행 검증 Pipeline**

- **Gemma 4 31B**에 QLoRA 기반 Fine-tuning 적용
- 공간 함수·Join·Filter·Aggregation 중심의 PostGIS SQL 생성 패턴 학습
- ChromaDB 기반 Schema / RAG Context Retrieval 구성
- **Natural Language → SQL Generation → PostGIS Execution → Result** 파이프라인 구현
- 반경 검색, 최근접 탐색, Spatial Join, 조건 필터링, 행정구역 단위 집계 지원
- 단순 SQL 문자열 비교가 아니라 **실제 SQL 실행 결과를 기준으로 모델 품질 평가**

**Evaluation — 5 Query Types / 150 Queries**

- SQL Execution Success Rate: **94.7%**
- Execution Result Match Rate: **88.7%**

`PostgreSQL` `PostGIS` `Gemma 4` `QLoRA` `ChromaDB` `LangChain` `Ollama` `vLLM` `FastAPI` `Docker` `Python`

<br>

### 🎯 Enterprise-Freelancer Recommendation System

기업이 프로젝트에 적합한 프리랜서를 직접 검색하는 비효율을 줄이기 위해  
프로젝트 요구사항과 프리랜서 프로필을 활용한  
**Top-N Ranking 기반 추천 시스템**

- 데이터 수집·전처리부터 Feature Engineering, Ranking Model, API, 배포까지 End-to-End 구축
- 기업-프리랜서 매칭 문제를 **Top-N Ranking Problem**으로 재정의
- 범주형 프로필·프로젝트 Feature 기반 **CatBoost Ranking Model** 설계
- Upstage Embedding API로 프로젝트 설명을 Vectorize하여 콘텐츠 기반 Feature 추가
- FastAPI / Docker 기반 Recommendation API 배포
- Hugging Face Hub 기반 Model Version Management

**Performance**

- Recall@10: **0.3300 → 0.5603 (+69.8%)**
- Embedding Feature 추가 후: **0.5603 → 0.6138 (+9.55%)**

`CatBoost` `Upstage Embedding API` `Optuna` `Selenium` `FastAPI` `Docker` `Nginx` `Vercel` `Hugging Face Hub` `Python`

<br>

### 👟 Nike Shoe Defect Detection

Nike 협력 제조업체의 육안 검사 공정을 자동화하기 위해  
**YOLO Segmentation 기반 신발 불량 영역 탐지 시스템** 구축

- 인도네시아 현지 공장 파견을 통해 육안 검사 기준 분석 및 불량 이미지 수집·QC 수행
- CVAT Polygon Annotation을 YOLO Segmentation 학습 포맷으로 변환
- Polygon → Segmentation Mask 변환 및 제품 영역 기준 Background Removal
- 이미지를 4분할하여 작은 결함의 학습·추론 성능 개선
- 분할 이미지 추론 결과를 원본 좌표계로 복원
- Contour 기반 Defect Matching을 적용해 Instance-level 정합성 평가

**Performance — 7 Defect Classes**

- Good / Defect Accuracy: **97.4%**
- Defect Classification Accuracy: **88.12%**

`YOLO Segmentation` `PyTorch` `OpenCV` `SAM` `CVAT` `Python`

---

<div align="center">

## 💻 Skills

### Languages

<img src="https://img.shields.io/badge/Python-3776AB?style=flat-square&logo=Python&logoColor=white"/>
<img src="https://img.shields.io/badge/C++-00599C?style=flat-square&logo=cplusplus&logoColor=white"/>
<img src="https://img.shields.io/badge/C-A8B9CC?style=flat-square&logo=c&logoColor=black"/>

<br>

### ML / LLM

<img src="https://img.shields.io/badge/PyTorch-EE4C2C?style=flat-square&logo=PyTorch&logoColor=white"/>
<img src="https://img.shields.io/badge/scikit--learn-F7931E?style=flat-square&logo=scikitlearn&logoColor=white"/>
<img src="https://img.shields.io/badge/TensorFlow-FF6F00?style=flat-square&logo=TensorFlow&logoColor=white"/>
<img src="https://img.shields.io/badge/LangChain-1C3C3C?style=flat-square&logo=langchain&logoColor=white"/>
<img src="https://img.shields.io/badge/vLLM-6A5ACD?style=flat-square&logoColor=white"/>
<img src="https://img.shields.io/badge/Ollama-000000?style=flat-square&logo=ollama&logoColor=white"/>
<img src="https://img.shields.io/badge/Flowise-3B82F6?style=flat-square&logoColor=white"/>

<br>

### Backend / Database

<img src="https://img.shields.io/badge/FastAPI-009688?style=flat-square&logo=FastAPI&logoColor=white"/>
<img src="https://img.shields.io/badge/Flask-000000?style=flat-square&logo=Flask&logoColor=white"/>
<img src="https://img.shields.io/badge/PostgreSQL-4169E1?style=flat-square&logo=PostgreSQL&logoColor=white"/>
<img src="https://img.shields.io/badge/PostGIS-336791?style=flat-square&logo=PostgreSQL&logoColor=white"/>
<img src="https://img.shields.io/badge/MySQL-4479A1?style=flat-square&logo=MySQL&logoColor=white"/>
<img src="https://img.shields.io/badge/ChromaDB-FF6446?style=flat-square&logoColor=white"/>

<br>

### MLOps / Workflow

<img src="https://img.shields.io/badge/MLflow-0194E2?style=flat-square&logo=MLflow&logoColor=white"/>
<img src="https://img.shields.io/badge/Weights%20%26%20Biases-FFBE00?style=flat-square&logo=weightsandbiases&logoColor=black"/>
<img src="https://img.shields.io/badge/Apache%20Airflow-017CEE?style=flat-square&logo=ApacheAirflow&logoColor=white"/>

<br>

### Infra / DevOps

<img src="https://img.shields.io/badge/Docker-2496ED?style=flat-square&logo=Docker&logoColor=white"/>
<img src="https://img.shields.io/badge/Kubernetes-326CE5?style=flat-square&logo=Kubernetes&logoColor=white"/>
<img src="https://img.shields.io/badge/Linux-FCC624?style=flat-square&logo=Linux&logoColor=black"/>
<img src="https://img.shields.io/badge/NVIDIA%20CUDA-76B900?style=flat-square&logo=NVIDIA&logoColor=white"/>

<br>

### Tools

<img src="https://img.shields.io/badge/Git-F05032?style=flat-square&logo=Git&logoColor=white"/>
<img src="https://img.shields.io/badge/Jira-0052CC?style=flat-square&logo=Jira&logoColor=white"/>
<img src="https://img.shields.io/badge/Notion-000000?style=flat-square&logo=Notion&logoColor=white"/>

</div>

---

<div align="center">

## 🏆 Algorithm

[![Solved.ac Profile](http://mazassumnida.wtf/api/v2/generate_badge?boj=twokst)](https://solved.ac/twokst)

</div>
