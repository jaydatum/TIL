# TIL day 10

# 데이터 분석 boot camp 34일차

---

## 1. 고객별 연간 지출액 예측 실습(Linear regression)

- linear regression으로 E-Commerce 고객별 연간 지출액 예측
- sns.pairplot(data) : 상관관계 시각화
- 통계량 해석
1. R-squared : 모델의 설명력
   
    - 클수록 좋은 모델 (0.8이상이면 괜찮다고 본다.)
    - Adj. R-squared는 변수의 갯수까지 고려한 통계량으로 이게 더 중요

2. coefficient : 각 독립변수의 영향력 (회귀계수)
   
    - 특정 독립 변수의 결정계수가 클수록 독립변수의 변화에 종속 변수가 크게 영향 받음
    - 따라서 scale을 맞춘 다음 coef를 평가해야 한다.


3. P-value : 검증 결과의 신뢰도에 대한 기준
   
    - 0.05 이하면 통계적으로 유의미하다고 판단



## 2. 광고 반응률 예측(Logistic regression)

- 로지스틱 회귀의 이해와 도출 : 별도 포스팅 예정
- sns.displot(data) : 분포도 확인 → skewed/ curtosis 확인 : 스케일링 여부 파악
- 결측치 처리하기
1. 결측치가 있는 행 제거 : dropna 

   -> 결측치가 10% 미만인 경우

2. 결측치를 추정치로 채워넣기(평균값 등) : fillna
   -> 결측치가 20~30% 정도인 경우

3. 결측치가 있는 컬럼 제거 : drop
   -> 결측치가 한 컬럼에 70~80%인 경우

4. 그냥 두기
   -> 고의적인 정보 비공개인 경우

- 머신러닝 프로젝트 프로세스
1. 데이터 read_csv
2. 전처리 (불필요한 컬럼, 결측치 제거)
3. 시각화 (distplot, pairplot,..)
4. 데이터 컬럼 분리 (features, lable)
5. 학습, 테스트 데이터 분리 (train_test_split)
6. 학습 (fit) -> 모델
7. 예측(predict)
8. 모델 평가지표(metrics) 향상



## 3. 고객 이탈 예측 (KNN)

- KNN(K-Nearest Neighbor) 분류
  - k개의 이웃들과의 거리를 계산하여 더 가까운 쪽으로 분류하는 알고리즘 → 최적의 k갯수를 찾는 것이 핵심!
  - 별도 블로그 포스팅 예정
- scaling 복습 : standard, robust, minmax scaler

```python
from sklearn.preprocessing import StandardScaler, RobustScaler, MinMaxScaler
```

1. Standard Scaler : 정규분포화 / 데이터의 분포를 단순화
2. Robust Scaler : 정규분포화 / 이상치 영향을 최소화 (부드럽게 만들어줌)
3. Min-max Scaler : 0~1 사이 값 / 원래 데이터의 분포 특성 보전

- 분류알고리즘의 비교

  | KNN           | Logistic Regression            |
  | :------------ | ------------------------------ |
  | 비모수 모델   | 모수 모델(선형 관계 전제 필요) |
  | 속도 느림     | 속도 빠름                      |
  | 결과값만 제시 | R squred 등의 통계값도 제시    |



# 개인 공부

------

## 1. Toy project

- kaggle walmart 데이터셋으로 regression 공부
- [kaggle walmart dataset](https://www.kaggle.com/yasserh/walmart-dataset)
- 1차 시도 처참히 실패....

## 2. pandas 기초를 탄탄히

- ML 공부하는 시간보다 기초가 부실해서 프로젝트가 더 오래걸린다.
- 검색할 정도로 모르는 부분은 블로그에 별도 포스팅하기!

## 3. 영상 자료

[[카일데이] 요즘 데이터 분석가의 현실, 데이터 분석 직군의 세분화 트렌드](https://www.youtube.com/watch?v=mzOWMax9Sxc&list=WL&index=6&t=115s)
