# Horikawa et al. (2020) 논의 및 한계점 요약

> **논문**: The Neural Representation of Visually Evoked Emotion Is High-Dimensional, Categorical, and Distributed across Transmodal Brain Regions
> **저널**: iScience (Cell Press), 2020

---

## 1. 주요 연구 의의 (Discussion)

### 1.1 감정의 분산적 표상 확인

> "Emotions were represented not by simple one-to-one mappings between particular emotions and brain regions (e.g., fear and the amygdala) but by more complex configurations across multiple networks" (p.14)

**핵심 발견**:
- 특정 감정 ↔ 특정 뇌 영역의 1:1 매핑이 아님
- 여러 네트워크에 걸친 복잡한 구성으로 표상됨
- 개인 간 일관성 있음 (5명 모두 유사한 패턴)

**이론적 함의**:
- 국소화(localization) 관점과 분산 표상(distributed representation) 관점 간의 오래된 논쟁을 조화시킴
- 국소 병변이 특정 감정 행동에 영향을 미칠 수 있는 이유 설명: 네트워크의 허브(hub)가 손상되면 해당 감정 처리에 차질

---

### 1.2 Default Mode Network의 다중 모드

> "The default mode network can in this way be considered to have not just one mode but many modes of activity corresponding to different emotions" (p.14)

**핵심 발견**:
- DMN은 단일 "기본 모드"가 아니라 **감정별로 다른 활동 모드**를 가짐
- 각 감정마다 DMN 내 하위 영역들의 관여 정도가 다름

**비유**:
```
전통적 관점:  DMN = "쉬는 상태"의 단일 네트워크
새로운 관점:  DMN = "다중 감정 모드"를 가진 복합 네트워크
              - fear 모드
              - joy 모드
              - awe 모드
              - ...
```

---

### 1.3 카테고리 > 차원 (전뇌에서)

> "Emotion categories reliably capture neural representations that are more specific than those captured by a wide range of affective dimensions throughout the brain" (p.14)

**핵심 발견**:
- 피질 + 피질하 영역 모두에서 카테고리 모델이 우세
- 370개 영역 중 368개에서 카테고리 모델 승리
- Amygdala도 예외 아님

**이론적 함의**:
- Dimensional theory (valence-arousal)보다 Categorical theory가 신경 수준에서 더 잘 맞음
- Cowen & Keltner (2017) 행동 연구 결과와 수렴

---

### 1.4 고차원 카테고리 공간

> "These results point to a high-dimensional, categorical space in the neural representation of emotion" (p.15)

**핵심 개념**:
```
저차원 (2D):     valence × arousal
고차원 (27-34D): 27개 이상의 구별되는 감정 카테고리

→ 뇌는 고차원 공간에서 감정을 표상함
```

**증거 요약**:
1. Decoding: 31/34 카테고리가 유의미하게 디코딩됨
2. Encoding: 카테고리 모델이 차원 모델보다 더 많은 복셀 활동 설명
3. Clustering: 비지도 학습에서 카테고리별 클러스터 형성

---

### 1.5 감정 표상의 피질 계층 구조

> "A gradual representational shift along the unimodal-transmodal gradient from visual to semantic to emotion information" (p.15)

**Principal Gradient 상의 위치**:
```
Unimodal ←────────────────────────────────→ Transmodal
(1차 감각)                                   (고차 연합)
    │                                            │
    V1, V2       MT, LO, STS       DMN, mPFC, TPJ│
    (Visual)     (Semantic)        (Emotion)     │
```

**함의**:
- 감정 처리는 높은 수준의 **정보 통합**과 **특징 추상화**를 필요로 함
- Transmodal 영역이 감정 표상의 핵심 허브

---

### 1.6 실용적 응용 가능성

> "Decoders trained for perceived emotions may generalize to emotional states that occur spontaneously during dreams and mind wandering, with potential clinical applications" (p.15-16)

**잠재적 응용**:
- 꿈이나 mind wandering 중 자발적 감정 상태 디코딩
- 정서 장애 진단/모니터링
- 뉴로마케팅 (제품 평가)
- 뉴로피드백 치료

---

### 1.7 풍부한 자극의 중요성

> "As the field of affective science moves forward, the present study reveals how a more extensive analysis of whole-brain responses to a much richer and more extensive set of experimental conditions... can yield more definitive results" (p.16)

**방법론적 교훈**:
- 기존 연구: 좁은 범위의 자극, 소수의 감정
- 본 연구: 2,185개 비디오, 34개 카테고리
- **결론**: 풍부한 자극 세트가 더 결정적인 결과를 도출

---

## 2. 저자들이 인정한 한계점 (Limitations)

### 2.1 감정 레이블이 피험자 본인 것이 아님

> "The emotion ratings we used were averages from multiple raters and not from the subjects of our fMRI experiment" (p.16)

**문제점**:
```
크라우드 워커 (온라인 평정자)
        ↓
  감정 레이블 생성
        ↓
fMRI 피험자 5명의 뇌 활동과 매칭

→ 평정자의 느낌 ≠ fMRI 피험자의 실제 느낌일 수 있음
```

**영향**:
- 개인차 반영 어려움 (문화, 인구통계, 성격)
- 감정 표상의 개인 변산성 과소추정 가능

**저자의 대응**:
> "Future studies might uncover more robust neural representations by incorporating these variables"

---

### 2.2 1인칭 vs 3인칭 감정 혼재

> "The confounding of first-person and third-person emotions... The brain regions in which the category model outperformed the visual object and semantic models (e.g., IPL, VMPFC) overlapped with brain regions that have been implicated in a 'theory of mind network'" (p.16-17)

**문제점**:
```
비디오 내용: 타인이 감정을 표현하는 장면
피험자 반응: ?
  - 본인이 느끼는 감정? (1인칭)
  - 타인의 감정을 추론? (3인칭 / Theory of Mind)

→ 두 과정이 혼재되어 분리 불가능
```

**증거**:
- 감정 모델이 우세한 영역 (IPL, VMPFC) = Theory of Mind 네트워크와 중첩

**해결 방안**:
> "Future experiments are needed to dissociate these phenomena using more carefully designed experiments, perhaps including psychophysiological measures indicative of first-person emotional experience"

---

### 2.3 시선 추적 없음

> "As we allowed the subjects to freely view presented video stimuli, differential gaze patterns for each emotional experience might have some influence on our brain data" (p.17)

**문제점**:
```
자유 시청 조건
  → 감정마다 다른 시선 패턴?
  → 시선 패턴이 뇌 데이터에 영향?
```

**완화 요인**:
> "Although the neural representation of gaze is known to be highly localized in specific brain regions"

시선 표상은 특정 영역에 국소화되어 있어서, 분산된 감정 표상과는 구별 가능할 수 있음

---

### 2.4 단일 자극 제시 (반복 측정 없음)

> "Because each stimulus was presented only once, we were unable to estimate the proportion of systematic variance in voxel responses that was left unexplained by our models" (p.15-16)

**문제점**:
```
일반적인 encoding 연구: 자극 반복 제시 → noise ceiling 추정
본 연구: 각 자극 1회만 제시 → noise ceiling 추정 불가
```

**왜 반복하지 않았나?**
> "Responses to emotional stimuli are likely to change with repeated exposure to the stimuli, given that many emotional responses (e.g., surprise) can be affected by past exposure and expectations"

- surprise 같은 감정은 반복 노출 시 변함
- 감정의 본질적 특성상 반복 측정이 부적절

**완화 요인**:
> "The model prediction accuracies we observed were moderately high by fMRI standards"

---

## 3. 추가로 고려할 수 있는 한계점 (논문에 명시되지 않음)

### 3.1 피험자 수 (5명)

**문제점**:
- 통계적 검정력 제한
- 개인차 일반화 주의 필요
- 집단 수준 추론에 한계

**완화 요인**:
- 5명 모두에서 일관된 패턴 관찰
- 대신 많은 자극(2,181개)으로 피험자 내 변산성 확보

---

### 3.2 생태학적 타당성

**문제점**:
```
fMRI 스캐너 안에서 비디오 시청
  ≠ 실제 삶에서의 감정 경험

- 소음, 좁은 공간, 움직임 제한
- 수동적 시청 vs 능동적 상호작용
```

---

### 3.3 시간 해상도

**문제점**:
```
fMRI의 시간 해상도: ~2초 (TR)
감정의 시간 스케일: 밀리초~초

→ 빠른 감정 변화 포착 어려움
→ 5-10초 비디오 전체를 평균화
```

---

### 3.4 문화적 제한

**문제점**:
```
34개 감정 카테고리 = 영어권 감정 분류
- 다른 문화의 고유 감정 개념 누락 가능
- 예: 한국어 "정", 일본어 "amae" 등
```

---

### 3.5 자극 양식의 제한

> "These stimuli are still only visual in nature" (p.16)

**문제점**:
- 시각 자극만 사용 (청각 없음)
- 실제 감정 경험은 다중 감각적

**저자의 제안**:
> "Future studies could build on this work by including auditory content, content with personal significance to the subject... or tasks that include behavioral involvement of the subject"

---

## 4. 요약 표

### 저자가 인정한 한계점

| 한계점 | 핵심 문제 | 영향 | 해결 방안 |
|:------|:---------|:----|:---------|
| 레이블 출처 | 평정자 ≠ 피험자 | 개인차 반영 부족 | 개인별 레이블링 |
| 1인칭/3인칭 혼재 | ToM과 구분 불가 | 감정 vs 추론 혼재 | 생리 지표 추가 |
| 시선 추적 없음 | 시선 패턴 통제 안 됨 | 시선 효과 혼입 가능 | Eye-tracking |
| 단일 제시 | noise ceiling 불가 | 설명력 상한 불명 | (감정 특성상 어려움) |

### 추가 고려 가능한 한계점

| 한계점 | 핵심 문제 |
|:------|:---------|
| 피험자 수 | 5명으로 일반화 제한 |
| 생태학적 타당성 | 스캐너 환경 ≠ 실제 |
| 시간 해상도 | 빠른 변화 포착 불가 |
| 문화적 제한 | 영어권 감정만 반영 |
| 양식 제한 | 시각만 (청각 없음) |

---

## 5. Cowen 2017과의 연결

### 수렴하는 증거

```
┌─────────────────────────────────────────────────────────┐
│                    Cowen 2017                           │
│  데이터: Self-report (주관적 보고)                       │
│  결론: 고차원 카테고리 > 저차원 차원 + 연속적 그라디언트   │
└─────────────────────────────────────────────────────────┘
                          ↓
              같은 자극, 같은 분류 체계
                          ↓
┌─────────────────────────────────────────────────────────┐
│                   Horikawa 2020                         │
│  데이터: fMRI (뇌 활동)                                  │
│  결론: 고차원 카테고리 > 저차원 차원 + 연속적 그라디언트   │
└─────────────────────────────────────────────────────────┘

→ Self-report와 Neural representation에서 동일한 패턴!
→ "언어적 습관" 가설 기각
→ 카테고리 구조가 신경 수준에서 실재
```

---

*마지막 업데이트: 2026-01-04*
*타당성 검토 완료*
