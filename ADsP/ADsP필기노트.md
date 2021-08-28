# ADsP

## 1. 데이터의 이해
### 1. 데이터 유형
  - 정성적 데이터 : 회사매출 증가 (문자형태)
  - 정량적 데이터 : 나이, 몸무게, 주가 (수치, 도형, 기호)

---

### 2. 암묵지와 형식지의 상호작용
  - Socialization(공통화)
  - Externalization(표출화)
  - Combination(연결화)
  - Internalization(내면화)

---

### 3. DIKW pyramid
  - Wisdom(지혜)
  - Knoledge(지식)
  - Information(정보)
  - Data(데이터)

---

## 2. 데이터 분석 기획

### 1. 분석방법론
- Waterfall Model
  - 순차적으로 진행하는 방법(기존 IT의 SW개발 방식)
- Prototype Model
  - 일부분만 만듬 -> 다시 요구사항 분석 -> 다시 개발
- Spiral Model
  - 반복을 통한 점증 개발(체계적이지 못함)

---

### 1. KDD 분석방법론  
1. Data Selection
    - 비즈니스 도메인에 대한 프로젝트 목표 설정이 선행 되어야함
    - 원시 데이터에서 필요한 데이터만 추출하는 단계  

2. Preprocessing
    - Outlier, Missing Value, Noise 처리  

3. Transformation
    - dimensionality reduction(차원 축소)
    - Splitting Data(데이터 분리)

4. Data Mining
    - 기법 선택, 알고리즘 적용
    - 전처리와 변환 프로레서 추가 실행하여 최적의 결과 산출

5. Interpretation/Evaluation
    - 목적과 일치하는지, 지식 업무에 활용
  
6. CRISP-DM 방법론

7. 빅데이터 분석 방법론

## 3. 데이터 분석

### 1. 기초분석 및 데이터 관리
1. 데이터 마이닝
    - 대용량 데이터에서 의미있는 패턴을 파악하거나 예측하여 의사결정에 활용

2. 분석목적
    - 예측
      - 분류규칙(회귀분석, 판별분석, 신경망, 의사결정나무)
    
    - 설명
      - 연관규칙(동시발생매트릭스)
      - 연속규칙(동시발생매트릭스)
      - 데이터 군집화(K-Means Clustering)

3. 기초분석 및 데이터 관리
    1. **데이터 EDA(탐색적 자료분석)**

    2. **결측값**
      - 결측값 인식
        - NA, 9999999, ' ', Unknown 등
        - 결측값 자체가 의미 있는 경우가 있음
          > 인구통계데이터(아주 부자, 아주 가난한 경우 정보 미기입 등) 

      - 결측값 처리방법
        - 단순대치법
          - Completes ananlysis
            > 결측값 삭제 
          - 평균 대치법(Mean Imputation)
            - 비조건부 평균대치법 : 관측데이터의 평균으로 대치
            - 조건부 평균대치법 : 회귀분석을 활용한 대치법

          - 단순확률 대치법(Single Stochastic Imputation)
            > 평균대치법에서 추정량 표준 오차의 과소 추정문제 보완(Hot-deck 방법, nearest neighbor 방법)

        - 다중 대치법(Multiple Imputation)
          - 단순대치법을 한번하지 않고 m번 대치를 통해 m개의 가상적 완전 자료를 만드는 방법
      
      > 결측값의 경우 Bad Data는 삭제 필요
    
    3. **이상치(Outlier)**
      - Outlier 인식
        - ESD(Extreme Studentized Deviation)
        - 기하평균 - 2.5 * 표준편차 < Data < 기하평균 + 2.5 * 표준편차
        - 사분위수 이용하여 제거(Box flot이용)
          > 이상값 정의 Q1 - 1.5(Q3-Q1)< Data < Q3 + 1.5(Q3-Q1)를 벗어난 데이터

      - 극단값 절단
        - 기하평균을 이용한 제거
          > geo_mean(기하평균)

        - 하단, 상단 % 이용한 제거
          > 10% (상하위 5% 절단)
      
      - 극단값 조정 방법
        - 상한값과 하한값을 벗어나는 값들을 하한, 상한값으로 바꾸어 활용하는 방법
---

## 기출문제 및 알아야할 것

1. 데이터 이해

2. 데이터 분석기획
    1. 분석주체유형 (4가지)  
    2. 데이터유형(정형, 비정형)  
    3. 상향식,하향식(아래 방법론과 연동)  
    4. 방법론(빅데이터, CRISP-DM, KDD) 3가지  
    5. 비즈니스모델 캔버스 