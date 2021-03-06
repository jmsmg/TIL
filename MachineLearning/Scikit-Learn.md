# Scikit-Learn

1. 순서
    ``` python
    # 1. 데이터셋 불러오기
    sklearn.datasets.load_[data]()
    
    # 2. Train/Test set으로 데이터 나누기
    sklearn.model_selection.train_test_split(X,Y,test_size)
    
    # 3. 모델 객체 (Model Instance) 생성
    model = sklearn.linear_model.LinearRegression() # 괄호 안 내용은 Hyper prameter
            sklearn.linear_model.LogisticRegression()
            sklearn.neighbors.KNeighborsClassifier(n_neighbors)
            sklearn.cluster.KMeans(n_clusters)
            sklearn.decomposition.PCA(n_components)
            sklearn.svm.SVC(kernel, C, gamma)
    
    # 4. 모델 학습시키기(Model fitting)
    model.fit(train_X, train_Y)

     # y = a x + b
    print('Coefficients : ', model.coef_) # a값
    print('Intercept : ', model.intercept_) # b값
    
    # 5. 모델로 새로운 데이터 예측하기 (Predict on test data)
    - model.predict(test_X)
    - model.predict_proba(test_X)

    # sklearn.metrics.mean_squared_error(predict_Y, test_Y)
    # sklearn.metrics.accuracy_score(predicted_Y, test_Y)
    # sklearn.metrics.precision_score
    # sklearn.metrics.recall_score
    # sklearn.metrics.r2_score
    ```

   - 입력데이터의 자릿수, Traing data의 자릿수, Test data의 자릿수 확인해서 under fitting인지 over fitting인지 구분

2. ROC curve 시각화
    ```python
    from sklean.metrics import roc_curve, auc
    
    # fpr = x, tpr = y, _ = Threshold
    fpr, tpr, _ = roc_curve(y_ture=y_test, y_score=pred_test[:,1])

    roc_auc = auc(fpr, tpr)
    ```


엑셀 -> 전처리 -> numpy array로 변환 -> scikit learn으로 돌림