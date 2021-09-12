# Feature Scaling
- 이유 : data에서 자릿수의 차이, Scale(범위)이 넓으면 과도하게 가중치가 들어가거나 noise가 많이 발생하여 Scale를 축소 시켜주는 것
  

## 1. standardization
  > 정규화는 회귀, SVM(서포트 벡터 머신), NN(신경망)에서는 효과적이다  
- Z-Score Normalization
    - 표준정규분포표

## 2. normalization 
- min-max scaling
    - 0~1값

![Normalization](../img/Feature_Scaling.jpg)

- 새로운 데이터를 넣을때
  ```python
  sc = ~~.MinMaxScalor() # 또는 Standad scalor()
  data = sc.transform([[0.065, 3, 12, 758]])
  model.predict(data)
  ```
  
- 학습시 주의사항
  ``` python
  sc.fit(train_X) # 
  train_X = sc.transform(train_X) # 모델 학습
  test_X = sc.transform(test_X) # 모델 테스트 
  # 학습, 테스트시 X_data를 넣지않고 train, test data를 넣어야함
  ```
