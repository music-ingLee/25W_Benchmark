# Horikawa et al., 2020 Benchmark Project

## 학습자 프로필
- **전공**: 심리학 학부생
- **역할**: 연구소 인턴 (2025W 학기 시작)
- **학습 스타일**:
  - 집요하게 파고드는 방식 선호
  - 파인만 방식 (Feynman Technique) 학습 요청
  - 풍부한 예시와 직관적 설명 선호
  - 기초적인 질문도 환영

## 교수자 역할
- Computational neuroscience 전문가로서 멘토링
- 복잡한 개념을 일상적 비유로 설명
- 수학적 개념은 직관부터 시작해서 점진적으로 깊이 들어가기
- 질문을 장려하고, "왜?"를 반복적으로 탐구

---

## 논문 개요: Horikawa et al., 2020

**제목**: The Neural Representation of Visually Evoked Emotion Is High-Dimensional, Categorical, and Distributed across Transmodal Brain Regions

**저널**: iScience (Cell Press), 2020년 5월

**저자**: Tomoyasu Horikawa, Alan S. Cowen, Dacher Keltner, Yukiyasu Kamitani

### 핵심 연구 질문
> "감정(emotion)은 뇌에서 어떻게 표상(represent)되는가?"

### 실험 설계
- **자극**: 2,185개의 감정 유발 비디오 (무음)
- **피험자**: 5명 (whole-brain fMRI 측정)
- **레이블링**: 크라우드 워커들이 각 비디오에 대해 평가
  - 34개 감정 카테고리 (예: joy, fear, disgust, amusement...)
  - 14개 정서 차원 (예: valence, arousal...)

### 분석 방법 (3가지 접근)

#### 1. Neural Decoding (디코딩)
- 뇌 활동 패턴 → 감정 점수 예측
- "이 뇌 활동을 보면, 피험자가 어떤 감정을 느끼고 있는지 알 수 있는가?"

#### 2. Voxel-wise Encoding (인코딩)
- 감정 점수 → 개별 복셀 활동 예측
- "특정 감정이 뇌의 어디에서 어떻게 활성화되는가?"

#### 3. Unsupervised Modeling (비지도 학습)
- UMAP, k-means clustering
- "뇌 활동 패턴들이 어떤 구조로 분포하는가?"

### 주요 발견 (Key Findings)

#### Finding 1: 감정은 여러 뇌 영역에 분산 표상됨
- 특정 감정 ↔ 특정 뇌 영역의 1:1 매핑이 아님
- 여러 영역의 네트워크가 각 감정을 표상
- 개인 간 일관성 있음 (피험자 5명 모두에서 유사한 패턴)

#### Finding 2: 카테고리 > 차원
- **감정 카테고리 모델**이 **정서 차원 모델**(valence, arousal)보다 뇌 활동을 더 잘 설명
- 거의 모든 뇌 영역에서 카테고리 모델 승리 (368/370 영역)
- 피질하 영역(amygdala 포함)에서도 마찬가지

#### Finding 3: 감정 표상은 transmodal 영역에 집중
- Visual → Semantic → Emotion 순으로 처리 계층 존재
- 감정 정보는 **transmodal regions** (default mode network 포함)에서 주로 인코딩
- Principal Gradient (PG) 분석으로 확인

#### Finding 4: 클러스터 구조 with 연속적 그라디언트
- 뇌 활동 패턴이 감정 카테고리별 클러스터 형성
- 관련된 감정들(예: fear-horror) 사이에는 연속적 그라디언트 존재

### 논문의 이론적 의의
1. **High-dimensional emotion space** 이론 지지
2. Basic emotion theory vs. Dimensional theory 논쟁에서 카테고리 접근 지지
3. 감정의 분산적(distributed) 신경 표상 확인

---

## 핵심 개념 용어집

### fMRI 관련
- **Voxel**: 3D 픽셀, fMRI의 최소 측정 단위
- **BOLD signal**: 뇌 활동의 간접 지표 (혈류 변화)
- **HCP360 parcellation**: 뇌를 360개 영역으로 나눈 지도

### 분석 방법 관련
- **Decoding**: 뇌 → 행동/자극 예측 (brain reading)
- **Encoding**: 자극 → 뇌 활동 예측 (brain modeling)
- **Cross-validation**: 과적합 방지를 위한 검증 방법
- **Regularized regression**: Ridge/Lasso 등 정규화된 회귀

### 감정 이론 관련
- **Basic emotion theory**: 기본 감정(6개 등)이 별개로 존재
- **Dimensional theory**: valence-arousal 2차원으로 감정 설명
- **Constructionist theory**: 감정은 더 기본적인 요소들의 조합

### 뇌 영역 관련
- **Transmodal regions**: 여러 감각 양식의 정보가 통합되는 영역
- **Default mode network**: 휴식 상태에서 활성화되는 네트워크
- **Principal Gradient**: 피질의 기능적 계층 구조를 나타내는 축

---

## 데이터 파일 목록
- `Horikawa et al., 2020...pdf`: 본 논문
- `horikawa_sm.pdf`: Supplementary Materials
- `category_data.csv`: 카테고리 관련 데이터
- `dimension_data.csv`: 차원 관련 데이터
- `category_dimension_feature_data.csv/json`: 통합 데이터
- `Horikawa_features_top_1_info.csv`: 주요 피처 정보
- `fMRI Experimental Protocol and Paradigm.pdf`: 실험 프로토콜
- `feature.tar.gz`: 피처 데이터 압축 파일

---

## 학습 로드맵 (제안)

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

---

*마지막 업데이트: 2026-01-02*
