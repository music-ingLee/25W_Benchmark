# Horikawa et al., 2020 Benchmark Project

**Connectome Lab 2025W 인턴십 프로젝트**

## 프로젝트 개요

감정(emotion)의 신경 표상(neural representation)을 연구한 Horikawa et al. (2020) 논문을 기반으로 한 벤치마크 프로젝트입니다.

### 핵심 연구 질문
> "감정은 뇌에서 어떻게 표상되는가?"

## 논문 정보

- **제목**: The Neural Representation of Visually Evoked Emotion Is High-Dimensional, Categorical, and Distributed across Transmodal Brain Regions
- **저자**: Tomoyasu Horikawa, Alan S. Cowen, Dacher Keltner, Yukiyasu Kamitani
- **저널**: iScience (Cell Press), 2020
- **DOI**: [10.1016/j.isci.2020.101060](https://doi.org/10.1016/j.isci.2020.101060)

## 폴더 구조

```
25W_Benchmark/
├── README.md              # 프로젝트 소개
├── CLAUDE.md              # AI 멘토 설정
│
├── literature/            # 논문 분석
│   └── horikawa2020.md
│
├── concepts/              # 개념 학습 노트
│   ├── fmri_basics.md
│   ├── emotion_theories.md
│   └── encoding_decoding.md
│
├── data/                  # 데이터
│   ├── raw/               # 원본 데이터
│   └── processed/         # 전처리된 데이터
│
├── code/                  # 구현 코드
│   ├── exploration/       # 데이터 탐색
│   └── models/            # 모델 구현
│
└── plans/                 # 연구 계획
    ├── benchmark_plan.md
    └── analysis_plan.md
```

## 데이터 설명

| 파일 | 설명 |
|------|------|
| `category_data.csv` | 34개 감정 카테고리 데이터 |
| `dimension_data.csv` | 14개 정서 차원 데이터 |
| `category_dimension_feature_data.csv/json` | 통합 데이터 |
| `Horikawa_features_top_1_info.csv` | 주요 피처 정보 |
| `feature.tar.gz` | 전체 피처 데이터 (압축) |

## 학습 로드맵

### Phase 1: 정서과학 (Affective Science) 기초
- [ ] 감정 이론: Basic Emotion vs. Dimensional vs. Constructionist
- [ ] Valence-Arousal 모델과 그 한계
- [ ] 34개 감정 카테고리의 의미와 선정 근거 (Cowen & Keltner, 2017)
- [ ] 감정의 신경 기반: 편도체, 전전두엽, Default Mode Network

### Phase 2: 통계학 기초 → 심화
- [ ] **기초**: 평균, 분산, 상관계수, p-value의 의미
- [ ] **회귀분석**: Linear regression이란? (예측 vs 설명)
- [ ] **정규화**: Ridge/Lasso regression - 왜 필요한가?
- [ ] **모델 평가**: Train/Test split, Cross-validation, 과적합
- [ ] **다변량 분석**: 고차원 데이터 다루기, 차원의 저주
- [ ] **비모수 검정**: Permutation test의 원리

### Phase 3: 머신러닝 / 딥러닝 (ML/DL)
- [ ] **ML 기초**: Supervised vs. Unsupervised learning
- [ ] **분류 vs 회귀**: 언제 어떤 걸 쓰는가?
- [ ] **신경망 기초**: Perceptron → MLP → CNN
- [ ] **딥러닝 실습**: PyTorch 기초, 간단한 모델 구현
- [ ] **뇌 데이터에 DL 적용**: 3D CNN, Graph Neural Network 소개

### Phase 4: 논문 심층 분석
- [ ] Figure별 상세 해석 ✅ (진행 중)
- [ ] 방법론 깊이 이해: encoding/decoding 프레임워크
- [ ] 통계적 유의성 검정 방법
- [ ] 한계점과 후속 연구 방향

### Phase 5: Benchmark 구현 (실습)

**목표**: 논문의 분석을 직접 재현하고 개선하기

#### Step 1: 데이터 탐색
- [ ] CSV 파일 로드 및 구조 파악
- [ ] 감정 점수 분포 시각화
- [ ] 결측치/이상치 확인

#### Step 2: 논문 재현 (Ridge Regression)
- [ ] Encoding 모델 구현: 감정 점수 → 뇌 활동 예측
- [ ] Decoding 모델 구현: 뇌 활동 → 감정 점수 예측
- [ ] Cross-validation으로 성능 평가
- [ ] 논문 Figure와 결과 비교

#### Step 3: 확장 (ML/DL 적용)
- [ ] 딥러닝 모델로 encoding/decoding 시도
- [ ] 카테고리 vs 차원 모델 성능 비교
- [ ] 새로운 분석 아이디어 적용

## 진행 상황

- [x] Git repository 생성
- [x] Knowledge base 폴더 구조 구축
- [x] 논문 정독 및 Figure별 분석
- [x] 연구 아이디어 및 한계점 문서화
- [ ] Phase 1-3 개념 학습
- [ ] 데이터 탐색 및 시각화
- [ ] Benchmark 구현

---

*Connectome Lab | 2025 Winter*
