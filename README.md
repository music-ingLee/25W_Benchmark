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

### Phase 1: 기초 개념
- [ ] fMRI 원리와 BOLD 신호
- [ ] 뇌 영역 해부학 기초
- [ ] 감정 이론 (Basic vs. Dimensional)

### Phase 2: 분석 방법론
- [ ] Linear regression과 regularization
- [ ] Encoding vs. Decoding 프레임워크
- [ ] Cross-validation과 모델 평가

### Phase 3: 논문 심층 분석
- [ ] Figure별 상세 해석
- [ ] 통계 방법 이해
- [ ] 한계점과 후속 연구 방향

### Phase 4: Benchmark 구현
- [ ] 데이터 전처리
- [ ] 모델 구현
- [ ] 결과 재현 및 확장

## 진행 상황

- [x] Git repository 생성
- [x] Knowledge base 폴더 구조 구축
- [ ] 논문 정독 및 정리
- [ ] 연구 아이디어 도출
- [ ] 데이터 탐색 및 분석

---

*Connectome Lab | 2025 Winter*
