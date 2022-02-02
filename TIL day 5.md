# TIL day 5 

## cross_val_score 

- KFold 교차 검증을 간편하게 할 수 있는 사이킷런의 교차검증 API

- KFold 데이터 학습과 예측 프로세스
  1. 폴드 세트를 설정
  2. for 문을 통해 학습 및 테스트 데이터의 인덱스 추출
  3. 반복하면서 학습과 예측 수행하고 평가 결과 반환
  
- cross_val_score() → 한번에 수행 가능!!

- 실습 정리 [Tistorty블로그](https://jaydatum.tistory.com/136?category=999099)

  ## cross_val_score(estimator,X,y=None, scoring=None, cv=None, n_jobs=1, verbose=0, fit_params=None, pre_dispatch='2\*n_jobs')

  - estimator : classifier , regression 모델 (classifier : Stratified KFold 자동 적용)
  - X : feature dataset
  - y : label dataset
  - scoring : 평가지표
  - cv : number of cross validation
  - n_jobs : Number of jobs to run in parallel (병렬처리 갯수, -1:using all processors)
  - verbose : 수행 중 정보출력 (0:출력없음, 1:자세히, 2:함축적인 정보)
  - pre_dispatch : Controls the number of jobs that get dispatched during parallel execution
  - 실습정리 [Tistory블로그]https://jaydatum.tistory.com/137?category=999099)







## GridSearchCV

- GridSearch 개념 : 하이퍼 파라미터 튜닝을 위한 과정 -> 격자식으로 순차적으로 하이퍼 파라미터 대입

- CV 개념 : 데이터 편중으로 인한 과적합(overfitting) 방지를 위해 학습 데이터 셋을 학습/검증으로 나눔 -> 모의고사

- GridSearchCV : 교차검증 + 하이퍼 퍼라미터 튜닝

  - 하이퍼 파라미터 튜닝을 위한 그리드 서치와 교차평가(CV)를 한번에 할 수있는 Sklearn api
  - 지정한 하이퍼 파라미터를 순차적으로 입력하면서 최적의 파라미터를 도출할 수 있음
  - 그리드 서치 경우의 수 x CV 횟수 만큼의 학습과 평가가 이루어짐
  - 최적의 파라미터를 편리하게 찾을 수 있지만 수행시간이 상대적으로 오래걸림
  

  ## GridSearchCV(estimator, param_grid, scoring=None, refit=True, cv=None)

  - estimator : classifier, regressor, pipeline
  - param_grid : 그리드 서치로 튜닝할 하이퍼 파라미터를 딕셔너리 형태로 넣음
  - scoring : 평가지표
  - cv : 교차 검증을 위한 분할 데이터 셋의 수
  - refit : True 생성 시 최적의 하이퍼 파라미터 튜닝 후 입력된 estimator 객체를 해당 파라미터로 재학습

 