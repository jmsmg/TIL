# Machine Learning

## Supervised Learning

1. Regression
    - Linear Regression
      > 가장 적합한 Theta들의 set를 찾는 것이 목표
        > y(종속변수) = a(Weight)x + b(bias)
      - Simple Regression
        - 1개의 독립변수(x)가 1개의 종속변수(y)에 영향을 미칠 때

      - Multiple Regression
        - 2개 이상의 독립변수(x)가 1개의 종속변수(y)에 영향을 미칠 때
            - 변수들의 자릿수가 비슷해야함
              > Numeric column -> Min-Max Algorithm or Standardization  
              > Categorical column -> one-hot encoder  
            
      - Cost Function
        - MSE(Mean Squared Error Function) 

      - Gradient Descent(경사하강법)
        - MSE의 미분값을 구해 -(음수)가 나오면 theta(Weight)값을 오른쪽으로 이동(양수가 나오면 반대로)
        - 기울기 0까지 진행
        - Learning Rate(학습률, 보폭) 설정 
          > hyper-parameter : 인간이 설정해야하는 값
            > HPO(hyper parameter tuning)
          > error 값 = inf(infinite)
    - Polynomial

2. Decision Tree
3. Random forest
4. Classifcation
    - KNN
    - Trees
    - Logisitic Regression
    - Naive-Bays
    - SVM

## Unsupervised Learning

1. Clustering
    - K-means
    - Hierarchical Clustering
2. Dimensionality Reduction
    - PCA
    - t-SNE
3. Association analysis
    - Apriori
    - FP-Growth
4. Hidden Markov Model

## Reinforcement