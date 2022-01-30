# TIL day 4 

# 데이터 분석 Boot camp ML복습



- python ML perfect guide 챕터 정리
- 교차검증 : cross_val_score

**KFold 교차 검증을 간편하게 할 수있는 사이킷런의 교차검증 API**

KFold 데이터 학습과 예측 프로세스

1. 폴드 세트를 설정
2. for문을 통해 학습 및 테스트 데이터의 인덱스를 추출
3. 반복하면서 학습과 예측수행하고 평겨 결과 반환

cross_val_score() 를 쓰면 한번에 해결 가능하다. → 폴드 세트 추출, 학습 및 예측, 평가 과정들을 한번에 수행

```
from sklearn.model_selection import cross_val_score
```

**cross_val_score(estimator,X,y=None, scoring=None, cv=None, n_jobs=1, verbose=0, fit_params=None, pre_dispatch='2\*n_jobs')**

\- estimator : classifier , regression 모델 (classifier : Stratified KFold 자동 적용)
\- X : feature dataset
\- y : label dataset
\- scoring : 평가지표
\- cv : number of cross validation
\- n_jobs : Number of jobs to run in parallel (병렬처리 갯수, -1:using all processors)
\- verbose : 수행 중 정보출력 (0:출력없음, 1:자세히, 2:함축적인 정보)
\- pre_dispatch : Controls the number of jobs that get dispatched during parallel execution.

------