# TIL day 8

## 1. 파이썬 머신러닝 완벽 가이드

### 1. 3장 평가

- 정확도(Accuracy) 

  - 이진 분류 시 정확도 (accuracy) 가 최선의 평가 지표가 아닐 수 있음 → 타이타닉 생존 분류 실습 (성별로만 찍어도 정확도 잘나옴)
  - 주로 불균형한 분포를 데이터 셋에 부적합함

- 오차행렬(Confusion Matrix)

  - ![오차행렬]([../images/TIL day 8/confusionMatrxiUpdated.jpg](https://www.google.com/url?sa=i&url=https%3A%2F%2Fmanisha-sirsat.blogspot.com%2F2019%2F04%2Fconfusion-matrix.html&psig=AOvVaw1mMApC5b_XEwGFHYd2wRpp&ust=1643876336805000&source=images&cd=vfe&ved=0CAsQjRxqFwoTCPiU7NzK4PUCFQAAAAAdAAAAABAD))
  - 이진 분류의 예측 오류와 오류의 유형을 상세히 나타냄

- 정확도와 정밀도 : 데이터 셋의 예측 성능에 중점을 둔 평가지표

  - 정밀도(precision) : TP / (FP + TP) :positive로 예측한 대상 중 실제 값이 positive인 비율
  - 실제 negative 를 positive로 예측할 때 큰 손실이 발생하는 경우에 중요 (ex 스팸메일 분류)
  - 재현율 (recall/sensitivity) : TP / (FN+TP) : 실제 값이 positive인 대상 중 예측값이 positive인 비율
  - 실제 positive를 negative로 예측할 때 큰 손실이 발생하는 경우 (ex 암 진단, 금융 사기)

  