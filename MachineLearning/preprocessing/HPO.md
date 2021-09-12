# Hyper-parameter Optimization

## Bayesian 통계학 (사전확률 & 사후확률) vs 빈도주의 통계학 (Frequantist)

## 1. Grid-search 기법

```python
from sklearn.model_selection import GridSearchCV

# 아래 param_grid dict 의 C & gamma 에 후보 Hyper-params 값들을 리스트업합니다.
param_grid = {'C' : [0.1, 1, 10, 100, 1000], 
            'gamma' : [1, 0.1, 0.01, 0.001, 0.0001],
            'kernel' : ['rbf']}

# SVC()가 호출되면 SVC Class의 객체 변수가 만들어지고, 해당 객체 변수가 GridSearchCV
grid = GridSearchCV(SVC(), param_grid, refit=True, verbose=1)

# refit : 찾아진 가장 좋은 params로 estimator를 setting할 지 여부 (setting해줘야 곧바로 predict가 가능)
# verbose : 설명의 자세한 정도 (verbose를 3과 같이 바꿔보시면 더 자세하게 매 param set 마다의 결과를 확인할 수 있습니다.)

grid.fit(X_train_scaled, y_train)

print('The best parameters are ', grid.best_params_)

# model = SVC(C=10, gamma=0.01, kernel='rbf')
```
---
공부 더 필요함

## 2. Randomized-search 기법

## 3. Bayesian-search 기법